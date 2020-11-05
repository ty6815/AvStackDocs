 
# Rtsp认证主要分为两种：

##  基本认证（basic authentication）和摘要认证（ digest authentication　）

**基本认证**是http 1.0提出的认证方案，其消息传输不经过加密转换因此存在严重的安全隐患。

**摘要认证**是http 1.1提出的基本认证的替代方案，其消息经过MD5哈希转换因此具有更高的安全性。下面主要介绍摘要认证：
### .一 basic 认证

1.   客户端发送DESCRIBE请求到前端设备，URL中携带请求的URL地址
DESCRIBE  rtsp://192.168.1.55:554/live/1/video.sdp?token=A00453FR805a54C8
RTSP/1.0\r\n
CSeq: 1\r\n
Accept: application/sdp\r\n
User-agent: Realplayer\r\n\r\n

2. 步骤：设备认为没有通过认证，发出WWW-Authenticate认证请求
RTSP/1.0 401 Unauthorized\r\n
CSeq: 1\r\n
WWW-Authenticate: Basic realm="RTSPD"\r\n\r\n
 
 *此时客户端程序会弹出用户名密码认证窗口，输入认证信息后* 

3. 步骤3：客户端携带Authorization串再次发出DESCRIBE请求
DESCRIBE rtsp://192.168.1.55:554/live/1/video.sdp?token=A00453FR805a54C8
RTSP/1.0\r\n
CSeq: 2\r\n
Accept: application/sdp\r\n
User-Agent: RealMedia Player HelixDNAClient/12.0.1.647 (win32)\r\n
Authorization: Basic YWRtaW46YWRtaW4=\r\n\r\n
 

### .二 摘要认证 Digest authentication
    


1.  **客户端第一次发起连接请求：**

>  OPTIONS rtsp://192.168.123.158:554/11 RTSP/1.0
> CSeq: 1
> User-Agent: LibVLC/2.0.5(LIVE555 Streaming Media v2012.09.13)
> 
**服务器端返回服务端信息及public方法**：

> RTSP/1.0 200 OK
> Server: HiIpcam/V100R003 VodServer/1.0.0
> Cseq: 1
> Public: OPTIONS, DESCRIBE, SETUP, TEARDOWN, PLAY,GET_PARAMETER
> 

**2.客户端再次发起连接：**

> DESCRIBE rtsp://192.168.123.158:554/11 RTSP/1.0
>
> CSeq: 2
>
> User-Agent: LibVLC/2.0.5(LIVE555 Streaming Media v2012.09.13)
>
> Accept: application/sdp

**服务器端返回401错误，提示未认证并以nonce质询：**

> RTSP/1.0 401 Unauthorized
> Server: HiIpcam/V100R003 VodServer/1.0.0
>
> Cseq: 2
>
> WWW-Authenticate: Digest realm="HipcamRealServer",
> nonce="3b27a446bfa49b0c48c3edb83139543d"

**3.客户端以用户名，密码，nonce，HTTP方法，请求的URI等信息为基础产生response信息进行反馈（计算方法参考说明）：**
> 
> DESCRIBE rtsp://192.168.123.158:554/11 RTSP/1.0
>
> CSeq: 3
>
> Authorization: Digest username="admin",realm="Hipcam RealServer", nonce="3b27a446bfa49b0c48c3edb83139543d",uri="rtsp://192.168.123.158:554/11", response="258af9d739589e615f711838a0ff8c58"
>
> User-Agent: LibVLC/2.0.5(LIVE555 Streaming Media v2012.09.13)
> Accept: application/sdp

**服务器对客户端反馈的response进行校验，通过则返回如下字段：**
> 
> RTSP/1.0 200 OK
>
> Server: HiIpcam/V100R003 VodServer/1.0.0
>
> Cseq: 3
>
> Content-Type: application/sdp
>
> Cache-Control: must-revalidate
>
> Content-length: 306
>
> Content-Base: rtsp://192.168.123.158:554/11/
>  
> v=0
> o=StreamingServer 3331435948 1116907222000 IN IP4192.168.123.158
>
> s=\11
> c=IN IP4 0.0.0.0
>
> b=AS:1032
> t=0 0
> a=control: *
>
> m=video 0 RTP/AVP 96
>
> b=AS:1024
> a=control:trackID=0
>
> a=rtpmap:96 H264/90000
>
> a=fmtp:96 packetization-mode=1;sprop-parameter-sets=Z0LgHtoCgPRA,aM4wpIA=
> 
>a=framesize:96 640-480

**4 然后，客户端发起建立连接请求（用同样的方法计算response）：**

> 
> SETUP rtsp://192.168.123.158:554/11/trackID=0 RTSP/1.0
>
> CSeq: 4
>
> Authorization: Digest username="admin", realm="HipcamRealServer", nonce="3b27a446bfa49b0c48c3edb83139543d",uri="rtsp://192.168.123.158:554/11/", response="7251f3cd9dec6d89fc948e4c50e0b1cf"
>
> User-Agent: LibVLC/2.0.5(LIVE555 Streaming Media v2012.09.13)
>
> Transport:RTP/AVP;unicast;client_port=4074-4075

**服务器端验证客户端返回的response字段，通过则返回通信参数：**

> RTSP/1.0 200 OK
>
> Server: HiIpcam/V100R003 VodServer/1.0.0
>
> Cseq: 4
>
> Session: 430786884314920
>
> Cache-Control: must-revalidate
>
> Transport: RTP/AVP;unicast;mode=play;source=192.168.123.158;client_port=4074-4075;server_port=5000-5001;ssrc=542289ec


**5.最后，客户端发起播放请求(同样需计算response字段)：**

> PLAY rtsp://192.168.123.158:554/11/ RTSP/1.0
> 
> CSeq: 5
> 
> Authorization: Digest username="admin", realm="HipcamRealServer", nonce="3b27a446bfa49b0c48c3edb83139543d",uri="rtsp://192.168.123.158:554/11/",response="9bfb25badcf52e6826cae5688e26cf6d"
> 
> User-Agent: LibVLC/2.0.5(LIVE555 Streaming Media v2012.09.13)
> 
> Session: 430786884314920
> 
> Range: npt=0.000-

**服务器端校验response字段，通过则返回视频数据。**
 
说明：
1. 请求头字段说明
例如：OPTIONS rtsp://192.168.123.158:554/11RTSP/1.0
字段依次包含：public_method,uri地址，协议版本
 
2. response字段的计算
RTSP客户端应该使用username + password并计算response如下:
(1)当password为MD5编码,则
   response = md5( password:nonce:md5(public_method:url) );
(2)当password为ANSI字符串,则
    response= md5( md5(username:realm:password):nonce:md5(public_method:url) );
客户端在每次发起不同的请求方法时都需要计算response字段，同样在服务器端校验时也默认采取同样的计算方法。

其中“YWRtaW46YWRtaW4=”为前端设备访问 username:password明文的base64编码
realplayer和quicktime分别基于tcp和HTTP协议实现该认证请求，抓包文件如下：
