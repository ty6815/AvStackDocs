> 通常来说，RTSP提供UDP方式发送RTP流。当然，发送流媒体时，UDP往往是更好的选择。

###下面是使用UDP时的一些问题：

1. UDP协议上的RTSP/RTP需要打开许多UDP端口（每一路流媒体都需要2个UDP端口，一个用于接收数据，一个用于接收控制信息）；

2. 当因特网上的路由器没有打开这些端口的时候，第一点将会存在问题；

3. 中间网络路由器很容易就过滤或者忽略掉UDP数据包；

4. UDP是不可靠传输协议，媒体包在因特网上传输时会面临着丢包。

**如果在TCP传输协议上承载RTSP/RTP将解决这些问题**

1. RTSP/RTP的控制命令和数据都通过一个端口，即RTSP的端口（默认为554），进行交互。

2. TCP协议提供可靠的流传输。

3. TCP包更容易穿透中间网络路由器。

###在TCP传输协议上承载RTSP/RTP也不是完美的，同样存在一些问题：


1. 由于二元交织，会使得RTP包封包和解包的过程变得更加复杂。

2. TCP是可靠的传输协议，但正是因为如此，会导致在实时流媒体中的延时。
3.  使用TCP传输协议承载RTSP/RTP需要花更多的功夫。

接下来让我们来了解一下怎么使用TCP承载RTSP/RTP。


##TCP承载RTSP/RTP

当使用TCP协议承载RTSP/RTP时，所有的命令和媒体数据都将通过RTSP端口，通常是554，进行发送。同时，数据将经过二元交织格式化之后才能发送。

**接下来我们将描述使用TCP承载RTSP/RTP的主要要素：**

SETUP

要使用TCP连接，RTSP客户端需要在SETUP阶段请求TCP连接。SETUP命令中应该包括如下格式的Transport：
`
Transport: RTP/AVP/TCP;interleaved=0-1`

上述Transport将告诉服务端使用TCP协议发送媒体数据，并且使用信道 0 和 1 对流数据以及控制信息进行交织。详细说来，使用偶数信道作为数据传输信道，使用奇数信道作为控制信道（数据信道 + 1）。所以，如果你设定数据信道为 0 ，那控制信道应该是 0 + 1 = 1。


下面是一个rtsp客户端请求 通过rtp over tcp方式建立连接报文；

![这里写图片描述](http://img.blog.csdn.net/20160810151550718)

SETUP之后，RTP数据将通过用来发送RTSP命令的TCP Socket进行发送。RTP数据将以如下格式进行封装：

	| magic number | channel number | data length | data  |magic number - 
	
	magic number：   RTP数据标识符，"$" 一个字节
	channel number： 信道数字 - 1个字节，用来指示信道
	data length ：   数据长度 - 2个字节，用来指示插入数据长度
	data ：          数据 - ，比如说RTP包，总长度与上面的数据长度相同

RTP，RTCP数据和RTSP数据共享TCP数据通道，所以必须有一个标识来区别三种数据。

RTP和RTCP数据会以$符号＋1个字节的通道编号＋2个字节的数据长度，共4个字节的前缀开始，RTSP数据是没有前缀数据的。RTP数据和RTCP数据的区别在于第二个字节的通道编号，

 下面给出一个 RTP OVER TCP 方式数据头结构定义 4oct


	    typedef struct rtsp_interleaved
		{ 
 			unsigned int magic : 8;// $
		    unsigned int channel : 8; //0-1
		    unsigned int rtp_len : 16;
	    }RILF;


下面给出一个完整的交互过程：

####（1）  OPTIONS 客户端向服务器询问有哪些方法可以使用**

```
OPTIONS rtsp://222.201.145.236/slamtv60.264 RTSP/1.0
CSeq: 2
User-Agent: LibVLC/1.1.11 (LIVE555 Streaming Media v2011.05.25)
```

服务器接收到OPTIONS请求后发出响应报文。状态码200代表请求成功。然后返回服务器当前时间(GMT)和所支持的方法。

```
RTSP/1.0 200 OK
CSeq: 2
Date: Wed, Mar 07 2012 03:48:07 GMT
Public: OPTIONS, DESCRIBE, SETUP, TEARDOWN, PLAY, PAUSE, GET_PARAMETER, SET_PARAMETER
```

####(2)  DESCRIBE   客户端像服务端请求描述媒体的详细信息。

```
DESCRIBE rtsp://222.201.145.236/slamtv60.264 RTSP/1.0
CSeq: 3
User-Agent: LibVLC/1.1.11 (LIVE555 Streaming Media v2011.05.25)
Accept: application/sdp
```

**服务端响应DESCRIBE请求所发回的报文，通过SDP协议发送媒体属性。**

```
RTSP/1.0 200 OK
CSeq: 3
Date: Wed, Mar 07 2012 03:48:07 GMT
Content-Base: rtsp://222.201.145.236/slamtv60.264/
Content-Type: application/sdp
Content-Length: 527

v=0
o=- 1331092087436965 1 IN IP4 222.201.145.236 
s=H.264 Video, streamed by the LIVE555 Media Server
i=slamtv60.264//媒体名称
a=type:broadcast  广播方式
a=control:*
a=range:npt=0-
m=video 0 RTP/AVP 96 //媒体类型+端口+传输协议+格式列表
c=IN IP4 0.0.0.0
b=AS:500
a=rtpmap:96 H264/90000
a=fmtp:96 packetization-mode=1;profile-level-id=4D4033;sprop-parameter-sets=Z01AM5JUDAS0IAAAAwBAAAAM0eMGVA==,aO48gA==
a=control:track1
```

#### (3) SETUP 客户端向服务端发送SETUP请求，要求服务端设置会话属性和流媒体传输方式以建立会话

```
SETUP rtsp://222.201.145.236/slamtv60.264/track1 RTSP/1.0
CSeq: 4
User-Agent: LibVLC/1.1.11 (LIVE555 Streaming Media v2011.05.25)
Transport: RTP/AVP/TCP;unicast; interleaved=0-1
//Transport:传输协议+传播方式（单播或多播）+通道号。
```
**服务端响应DESCRIBE请求所发回的报文**


```
RTSP/1.0 200 OK
CSeq: 4
Date: Wed, Mar 07 2012 03:48:18 GMT
Transport: RTP/AVP/TCP;unicast;destination=125.216.243.188;source=222.201.145.236;interleaved=0-1
Session: 289BFEAE
```
 
#### (4)  PLAY 会话建立后，客户端发出PLAY请求播放所申请的流媒体。传输机制按照SETUP命令所设置的进行

```
PLAY rtsp://222.201.145.236/slamtv60.264/ RTSP/1.0
CSeq: 5
User-Agent: LibVLC/1.1.11 (LIVE555 Streaming Media v2011.05.25)
Session: 289BFEAE
Range: npt=0.000-
```
**服务器回应**
```
RTSP/1.0 200 OK
CSeq: 5
Date: Wed, Mar 07 2012 03:48:18 GMT
Range: npt=0.000-
Session: 289BFEAE
RTP-Info: url=rtsp://222.201.145.236/slamtv60.264/track1;seq=61622;rtptime=1335382752
```

 **以下是RTP over RTSP（TCP）的数据流：**

![这里写图片描述](http://img.blog.csdn.net/20160810151443076)

**RFC 2326 第10.12节说明了插入二进制数据的细节。**
