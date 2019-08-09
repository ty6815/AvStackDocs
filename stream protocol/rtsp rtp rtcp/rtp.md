[原文链接](http://blog.csdn.net/machh/article/details/51868569)


## **RTP协议**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;实时传输协议RTP（Real-time Transport Protocol）是一个网络传输协议，它是由IETF的多媒体传输工作小组1996年在RFC 1889中公布的，后在RFC3550中进行更新。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   国际电信联盟ITU-T也发布了自己的RTP文档，作为H.225.0，但是后来当IETF发布了关于它的稳定的标准RFC后就被取消了。它作为因特网标准在[ [ RFC 3550 ] ](https://www.rfc-editor.org/rfc/rfc3550.txt) 有详细说明.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RTP协议详细说明了在互联网上传递音频和视频的标准数据包格式。它一开始被设计为一个多播协议，但后来被用在很多单播应用中。RTP协议常用于流媒体系统（配合RTSP协议），视频会议和一键通（Push toTalk）系统（配合H.323或SIP），使它成为IP电话产业的技术基础。RTP协议和RTP控制协议RTCP一起使用，而且它是建立在用户数据报协议上的（UDP）。

---


**RTP标准定义了两个子协议 ，RTP和RTCP**

**数据传输协议RTP**，用于实时传输数据。该协议提供的信息包括：时间戳（用于同步）、序列号（用于丢包和重排序检测）、以及负载格式（用于说明数据的编码格式）。

**控制协议RTCP**，用于QoS反馈和同步媒体流。相对于RTP来说，RTCP所占的带宽非常小，通常只有5%。


### **为什么要使用RTP**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;一提到流媒体传输、一谈到什么视频监控、视频会议、语音电话（VOIP），都离不开RTP协议的应用，但当大家都根据经验或者别人的应用而选择RTP协议的时候，你可曾想过，为什么我们要使用RTP来进行流媒体的传输呢？为什么我们一定要用RTP？难道TCP、UDP或者其他的网络协议不能达到我们的要求么？

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;像TCP这样的可靠传输协议，通过超时和重传机制来保证传输数据流中的每一个bit的正确性，但这样会使得无论从协议的实现还是传输的过程都变得非常的复杂。而且，当传输过程中有数据丢失的时候，由于对数据丢失的检测（超时检测）和重传，会数据流的传输被迫暂停和延时。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;或许你会说，我们可以利用客户端构造一个足够大的缓冲区来保证显示的正常，这种方法对于从网络播放音视频来说是可以接受的，但是对于一些需要实时交互的场合（如视频聊天、视频会议等），如果这种缓冲超过了200ms，将会产生难以接受的实时性体验。

####   **为什么RTP可以解决上述时延问题**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RTP协议是一种基于UDP的传输协议，RTP本身并不能为按顺序传送数据包提供可靠的传送机制，也不提供流量控制或拥塞控制，它依靠RTCP提供这些服务。这样，对于那些丢失的数据包，不存在由于超时检测而带来的延时，同时，对于那些丢弃的包，也可以由上层根据其重要性来选择性的重传。比如，对于I帧、P帧、B帧数据，由于其重要性依次降低，故在网络状况不好的情况下，可以考虑在B帧丢失甚至P帧丢失的情况下不进行重传，这样，在客户端方面，虽然可能会有短暂的不清晰画面，但却保证了实时性的体验和要求。


----------


###  **RTP的协议层次**

####  **传输层的子层**

图 1给出了流媒体应用中的一个典型的协议体系结构。


![这里写图片描述](https://camo.githubusercontent.com/67704718b539a7750a8ba0521d351b2708a90456/687474703a2f2f696d672e626c6f672e6373646e2e6e65742f3230313630373031313832353030363036)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;从图中可以看出，RTP被划分在传输层，它建立在UDP上。同UDP协议一样，为了实现其实时传输功能，RTP也有固定的封装形式。RTP用来为端到端的实时传输提供时间信息和流同步，但并不保证服务质量。服务质量由RTCP来提供。

#### **RTP的工作机制为：**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当应用程序建立一个RTP会话时，应用程序将确定一对目的传输地址。目的传输地址由一个网络地址和一对端口组成，有两个端口：一个给RTP包，一个给RTCP包，使得RTP/RTCP数据能够正确发送。RTP数据发向偶数的UDP端口，而对应的控制信号RTCP数据发向相邻的奇数UDP端口（偶数的UDP端口＋1），这样就构成一个UDP端口对。 RTP的发送过程如下，接收过程则相反。

       1) RTP协议从上层接收流媒体信息码流（如H.263），封装成RTP数据包；RTCP从上层接收控制信息，封装成RTCP控制包。

       2) RTP将RTP 数据包发往UDP端口对中偶数端口；RTCP将RTCP控制包发往UDP端口对中的奇数端口。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   RTP分组只包含RTP数据，而控制是由RTCP协议提供。RTP在1025到65535之间选择一个未使用的偶数UDP端口号，而在同一次会话中的RTCP则使用下一个奇数UDP端口号。端口号5004和5005分别用作RTP和RTCP的默认端口号。RTP分组的首部格式如图2所示，其中前12个字节是必须的。

![这里写图片描述](http://img.blog.csdn.net/20160709201458978)


###   **应用层的一部分**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;从应用开发者的角度看，RTP 应当是应用层的一部分。在应用的发送端，开发者必须编写用 RTP 封装分组的程序代码，然后把 RTP 分组交给 UDP 插口接口。在接收端，RTP 分组通过 UDP 插口接口进入应用层后，还要利用开发者编写的程序代码从 RTP 分组中把应用数据块提取出来。


---
###  **RTP包头中的流媒体特性**

首先，我们看看RTP的包头。
RTP报文头格式（见RFC3550 Page12）：
![这里写图片描述](http://img.blog.csdn.net/20160621122456759?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQv/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)


版本号（V）：2比特，用来标志使用的RTP版本。

填充位（P）：1比特，如果该位置位，则该RTP包的尾部就包含附加的填充字节。

**扩展位（X）：** 1比特，如果该位置位的话，RTP固定头部后面就跟有一个扩展头部。

CSRC计数器（CC）：4比特，含有固定头部后面跟着的CSRC的数目。

**标记位（M）：** 1比特,该位的解释由配置文档（Profile）来承担.

**载荷类型（PayloadType）：** 7比特，标识了RTP载荷的类型。

**序列号（SN）**：16比特，每发送一个 RTP 数据包，序列号增加1。接收端可以据此检测丢包和重建包序列。

**时间戳(Timestamp):** 2比特，记录了该包中数据的第一个字节的采样时刻。在一次会话开始时，时间戳初始化成一个初始值。即使在没有信号发送时，时间戳的数值也要随时间而不断地增加（时间在流逝嘛）。时钟频率依赖于负载数据格式，并在描述文件（profile）中进行描述。

同步源标识符(SSRC)：32比特，同步源就是指RTP包流的来源。在同一个RTP会话中不能有两个相同的SSRC值。该标识符是随机选取的 RFC1889推荐了MD5随机算法。

贡献源列表（CSRC List）：0～15项，每项32比特，用来标志对一个RTP混合器产生的新包有贡献的所有RTP包的源。由混合器将这些有贡献的SSRC标识符插入表中。SSRC标识符都被列出来，以便接收端能正确指出交谈双方的身份。


#### **RTP扩展头结构**

![这里写图片描述](http://img.blog.csdn.net/20160709205223838?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQv/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;图 4  Rtp扩展头
		
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;若 RTP 固定头中的扩展比特位置1（注意：如果有CSRC列表，则在CSRC列表之后），则一个长度可变的头扩展部分被加到 RTP 固定头之后。头扩展包含 16 比特的长度域，指示扩展项中 32 比特字的个数，不包括 4 个字节扩展头(因此零是有效值)。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RTP 固定头之后只允许有一个头扩展。为允许多个互操作实现独立生成不同的头扩展，或某种特定实现有多种不同的头扩展,扩展项的前 16 比特用以识别标识符或参数。这 16 比特的格式由具体实现的上层协议定义。基本的 RTP 说明并不定义任何头扩展本身。

---


### **RTP的会话过程**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当应用程序建立一个RTP会话时，应用程序将确定一对目的传输地址。目的传输地址由一个网络地址和一对端口组成，有两个端口：一个给RTP包，一个给RTCP包，使得RTP/RTCP数据能够正确发送。RTP数据发向偶数的UDP端口，而对应的控制信号RTCP数据发向相邻的奇数UDP端口（偶数的UDP端口＋1），这样就构成一个UDP端口对。

 **RTP的发送过程如下，接收过程则相反。**
 
 1.         RTP协议从上层接收流媒体信息码流（如H.263），封装成RTP数据包；RTCP从上层接收控制信息，封装成RTCP控制包。
 2.        RTP将RTP 数据包发往UDP端口对中偶数端口；RTCP将RTCP控制包发往UDP端口对中的接收端口。



### RTP的profile机制

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RTP为具体的应用提供了非常大的灵活性，它将传输协议与具体的应用环境、具体的控制策略分开，传输协议本身只提供完成实时传输的机制，开发者可以根据不同的应用环境，自主选择合适的配置环境、以及合适的控制策略。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这里所说的控制策略指的是你可以根据自己特定的应用需求，来实现特定的一些RTCP控制算法，比如前面提到的丢包的检测算法、丢包的重传策略、一些视频会议应用中的控制方案等等（这些策略我可能将在后续的文章中进行描述）。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;对于上面说的合适的配置环境，主要是指RTP的相关配置和负载格式的定义。RTP协议为了广泛地支持各种多媒体格式（如 H.264, MPEG-4, MJPEG, MPEG），没有在协议中体现出具体的应用配置，而是通过profile配置文件以及负载类型格式说明文件的形式来提供。对于任何一种特定的应用，RTP定义了一个profile文件以及相关的负载格式说明，相关的文件如下所示：

《RTP Profile for Audio and Video Conferences with Minimal Control》（RFC3551）

《RTP Payload Format for H.264 Video》（RFC3984）

《RTP Payload Format for MPEG-4 Audio/Visual Streams》（RFC3016）

等等，想了解更多可以点击这里：http://en.wikipedia.org/wiki/RTP_audio_video_profile

>  说明：如果应用程序不使用专有的方案来提供有效载荷类型(payload type)、顺序号或者时间戳，而是使用标准的RTP协议，应用程序就更容易与其他的网络应用程序配合运行，这是大家都希望的事情。例如，如果有两个不同的公司都在开发因特网电话软件，他们都把RTP合并到他们的产品中，这样就有希望：使用不同公司电话软件的用户之间能够进行通信。

---

### **RTCP的封装**



**RTCP的主要功能：**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;服务质量的监视与反馈、媒体间的同步，以及多播组中成员的标识。在RTP会话期 间，各参与者周期性地传送RTCP包。RTCP包中含有已发送的数据包的数量、丢失的数据包的数量等统计资料，因此，各参与者可以利用这些信息动态地改变传输速率，甚至改变有效载荷类型。RTP和RTCP配合使用，它们能以有效的反馈和最小的开销使传输效率最佳化，因而特别适合传送网上的实时数据。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RTCP也是用UDP来传送的，但RTCP封装的仅仅是一些控制信息，因而分组很短，所以可以将多个RTCP分组封装在一个UDP包中。RTCP有如下五种分组类型。

类型  | 缩写表示  | 用途 
---|---|---
200 | SR（Sender Report） |发送端报告
201 | RR（Receiver Report） |接收端报告
202 | SDES（Source Description Items） |源点描述
203 | BYE |结束传输
204 | .   APP |特定应用


上述五种分组的封装大同小异，下面只讲述SR类型，而其它类型请参考RFC3550。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;发送端报告分组SR（Sender Report）用来使发送端以多播方式向所有接收端报告发送情况。SR分组的主要内容有：相应的RTP流的SSRC，RTP流中最新产生的RTP分组的时间戳和NTP，RTP流包含的分组数，RTP流包含的字节数。SR包的封装如图3所示。


![image](http://p.blog.csdn.net/images/p_blog_csdn_net/bripengandre/RTCP%E7%9A%84%E5%A4%B4%E9%83%A8%E6%A0%BC%E5%BC%8F.JPG)

版本（V）：同RTP包头域。

填充（P）：同RTP包头域。

接收报告计数器（RC）：5比特，该SR包中的接收报告块的数目，可以为零。
包类型（PT）：8比特，SR包是200。

长度域（Length）：16比特，其中存放的是该SR包以32比特为单位的总长度减一。

同步源（SSRC）：SR包发送者的同步源标识符。与对应RTP包中的SSRC一样。
NTP Timestamp（Network time protocol）SR包发送时的绝对时间值。NTP的作用是同步不同的RTP媒体流。

RTP Timestamp：与NTP时间戳对应，与RTP数据包中的RTP时间戳具有相同的单位和随机初始值。

Sender’s packet count：从开始发送包到产生这个SR包这段时间里，发送者发送的RTP数据包的总数. SSRC改变时，这个域清零。

Sender`s octet count：从开始发送包到产生这个SR包这段时间里，发送者发送的净荷数据的总字节数（不包括头部和填充）。发送者改变其SSRC时，这个域要清零。

同步源n的SSRC标识符：该报告块中包含的是从该源接收到的包的统计信息。

丢失率（Fraction Lost）：表明从上一个SR或RR包发出以来从同步源n(SSRC_n)来的RTP数据包的丢失率。

累计的包丢失数目：从开始接收到SSRC_n的包到发送SR,从SSRC_n传过来的RTP数据包的丢失总数。

收到的扩展最大序列号：从SSRC_n收到的RTP数据包中最大的序列号，

接收抖动（Interarrival jitter）：RTP数据包接受时间的统计方差估计
上次SR时间戳（Last SR,LSR）：取最近从SSRC_n收到的SR包中的NTP时间戳的中间32比特。如果目前还没收到SR包，则该域清零。

上次SR以来的延时（Delay since last SR,DLSR）：上次从SSRC_n收到SR包到发送本报告的延时。


---

### **附： 代码描述**

####   **RTP header :**
```
/*
 * RTP header
 */
typedef struct 
{
#if 0	//BIG_ENDIA
    unsigned int version:2;   /* protocol version */
    unsigned int p:1;         /* padding flag */
    unsigned int x:1;         /* header extension flag */
    unsigned int cc:4;        /* CSRC count */
    unsigned int m:1;         /* marker bit */
    unsigned int pt:7;        /* payload type */
	unsigned int seq:16;      /* sequence number */

#else
    unsigned int cc:4;        /* CSRC count */
    unsigned int x:1;         /* header extension flag */
    unsigned int p:1;         /* padding flag */
    unsigned int version:2;   /* protocol version */
 
	unsigned int pt:7;        /* payload type */
    unsigned int m:1;         /* marker bit */
	unsigned int seq:16;      /* sequence number */
#endif

    u_int32 ts;               /* timestamp */
    u_int32 ssrc;             /* synchronization source */
    u_int32 csrc[1];          /* optional CSRC list */
} rtp_hdr_t;
```

####  **RTCP Common  header :**
```

/*
 * RTCP common header word
 */
typedef struct {
#if 0	//BIG_ENDIA
    unsigned int version:2;   /* protocol version */
    unsigned int p:1;         /* padding flag */
    unsigned int count:5;     /* varies by packet type */
#else
    unsigned int count:5;     /* varies by packet type */
    unsigned int p:1;         /* padding flag */
    unsigned int version:2;   /* protocol version */
#endif
    unsigned int pt:8;        /* RTCP packet type */
    unsigned short length;           /* pkt len in words, w/o this word */

} rtcp_common_t;
```

----------


