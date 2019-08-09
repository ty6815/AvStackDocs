

## SDP协议





###  一、SDP协议介绍
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SDP 完全是一种会话描述格式（对应的[RFC2327](https://www.rfc-editor.org/rfc/rfc2327.txt)  ,
[RFC4566](https://www.rfc-editor.org/rfc/rfc4566.txt), )

― 它不属于传输协议 ― 它只使用不同的适当的传输协议，包括会话通知协议（SAP）、会话初始协议（SIP）、实时流协议（RTSP）、MIME 扩展协议的电子邮件以及超文本传输协议（HTTP）。SDP协议是也是基于文本的协议，这样就能保证协议的可扩展性比较强，这样就使其具有广泛的应用范围。SDP 不支持会话内容或媒体编码的协商，所以在流媒体中只用来描述媒体信息。媒体协商这一块要用RTSP来实现．

流媒体协议sdp信息，附带在describe报文中有rtsp服务端发出，主要目的，告之会话的存在和给出参与该会话所必须的信息，sdp会话完全是文本形式，采用UTF-8编码的ISO 10646字符集

#### sdp描叙符包括：

- 会话名和目的
- 会话激活的时间区段
- 构成会话的媒体
- 接收这些媒体所需要的信息（地址，端口，格式）
- 会话所用的带宽信息
- 会话负责人的联系信息


#### 媒体信息包括：
- 媒体类型（视频，音频等）
- 传送协议（RTP/UDP/IP H.320等）
- 媒体格式（H,264视频，MPEG视频等）
- 媒体地址和端口

###  二、SDP协议格式
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SDP描述由许多文本行组成，文本行的格式为<类型>=<值>，<类型>是一个字母，<值>是结构化的文本串，其格式依<类型>而定。

####   ＜type＞ = < value >  [CRLF]  
  
>type:	该字节为单字节（如： v，o, m等）区分大小写，=号俩侧部允许有空格	 
>
> value:	为结构化文本串


### 会话描叙格式介绍
 
 

名称 |  格式： | 说明
---|---|---
协议版本： | 	v=0  | 给出sdp的版本号，目前为0版本，无子版本号
会话源     | 	o=(用户名)（会话标识）（版本）（网络类型）（地址类型）（地址）|如果不存在用户登录名，该字段标志位“-”	会话标识为一随机数字串	 	版本为该会话公告的版本 	 \r\n  网络类型为文本串，  \n  “IN”表示internet	  地址类型为文本串，目前定义为“IP4”和“IP6”两种地址
会话名： | s=(会话名)   | 每个会话描述必须只有一个会话名
会话信息： | 	i=(会话信息)  | 此字段并非必须，建议包括进来用于描叙相应会话文字性说明，每个会话描叙最多只能有一个
**URL:**： | 	u=(URL) | 此字段并非必须,提供url的描叙信息
连接数据： | 		c=(网络类型)（地址类型）（连接地址）


#### 时间描述

- t = （会话活动时间）
- r = * （0或多次重复次数）

#### 媒体描述

- m = （媒体名称和传输地址）
- i = * （媒体标题）
- c = * （连接信息 — 如果包含在会话层则该字段可选）
- b = * （带宽信息）
- k = * （加密密钥）
- a = * （0 个或多个会话属性行）



##### m描叙行：

 
> 格式：	m=(媒体)（端口）（传送层）（格式列表）
>
>	媒体类型：音频（audio）,视频(video),应用，数据和控制
>
> 	端口：媒体传送层端口
>
>	传送层：ip4上大多基于rtp/udp上传送（RTP/AVP）IETF RTP协议，在udp上传输
>   格式列表： 对应对应的音频负载类型（PT）
>
>   **m=video 0 RTP/AVP 96**



##### a描叙行：


> 格式：a=rtpmap:（净荷类型）（编码名）/（时钟速率）【/(编码参数)】
>  
>   a=control:（音/视频连接信息）	 
 	a=control:rtsp://192.168.1.197/h264stream0/trackID=0
>
>  a=rtpmap:96 H264/90000
 	
 	
###  	三、SDP协议例子
 	
```


v=0
o=StreamingServer 3677033027 1437537780000 IN IP4 192.168.1.44
s=\demo.mp4
u=http:///
e=admin@
c=IN IP4 0.0.0.0
b=AS:1398
t=0 0
a=control:*
a=x-copyright: MP4/3GP File hinted with GPAC 0.5.0-rev4065 (C)2000-2005 - http://gpac.sourceforge.net
a=range:npt=0- 216.52167

m=video 0 RTP/AVP 96
b=AS:1242
a=3GPP-Adaptation-Support:1
a=rtpmap:96 H264/90000
a=control:trackID=65536
a=fmtp:96 profile-level-id=42000A; packetization-mode=1; sprop-parameter-sets=Z0IACpZUBQHogA==,aM44gA==
a=framesize:96 640-480

m=audio 0 RTP/AVP 97
b=AS:156
a=3GPP-Adaptation-Support:1
a=rtpmap:97 mpeg4-generic/48000/1
a=control:trackID=65537
a=fmtp:97 profile-level-id=41; config=1188; streamType=5; mode=AAC-hbr; objectType=64; constantDuration=1024; sizeLength=13; indexLength=3; indexDeltaLength=3

```


视频"a=fmtp"字段的解析 参考 RFC3984的8.2节| 
---|---
音频config描述符的解析 参考 RFC 3016 | row 1 col 2



---

 

