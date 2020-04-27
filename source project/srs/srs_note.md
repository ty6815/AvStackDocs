<html>

<head>
<meta http-equiv=Content-Type content="text/html; charset=gb2312">
<meta name=Generator content="Microsoft Word 15 (filtered)">
<style>
<!--
 /* Font Definitions */
 @font-face
	{font-family:"Cambria Math";
	panose-1:2 4 5 3 5 4 6 3 2 4;}
@font-face
	{font-family:等线;
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:"等线 Light";
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:"\@等线";
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:"\@等线 Light";
	panose-1:2 1 6 0 3 1 1 1 1 1;}
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:等线;}
h1
	{mso-style-link:"标题 1 字符";
	margin-top:17.0pt;
	margin-right:0cm;
	margin-bottom:16.5pt;
	margin-left:0cm;
	text-align:justify;
	text-justify:inter-ideograph;
	line-height:240%;
	page-break-after:avoid;
	font-size:22.0pt;
	font-family:等线;}
h2
	{mso-style-link:"标题 2 字符";
	margin-top:13.0pt;
	margin-right:0cm;
	margin-bottom:13.0pt;
	margin-left:0cm;
	text-align:justify;
	text-justify:inter-ideograph;
	line-height:173%;
	page-break-after:avoid;
	font-size:16.0pt;
	font-family:"等线 Light";}
p.MsoToc1, li.MsoToc1, div.MsoToc1
	{margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:等线;}
p.MsoToc2, li.MsoToc2, div.MsoToc2
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:21.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:等线;}
p.MsoHeader, li.MsoHeader, div.MsoHeader
	{mso-style-link:"页眉 字符";
	margin:0cm;
	margin-bottom:.0001pt;
	text-align:center;
	layout-grid-mode:char;
	border:none;
	padding:0cm;
	font-size:9.0pt;
	font-family:等线;}
p.MsoFooter, li.MsoFooter, div.MsoFooter
	{mso-style-link:"页脚 字符";
	margin:0cm;
	margin-bottom:.0001pt;
	layout-grid-mode:char;
	font-size:9.0pt;
	font-family:等线;}
a:link, span.MsoHyperlink
	{color:blue;
	text-decoration:underline;}
a:visited, span.MsoHyperlinkFollowed
	{color:#954F72;
	text-decoration:underline;}
p.MsoNoSpacing, li.MsoNoSpacing, div.MsoNoSpacing
	{margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:等线;}
p.MsoListParagraph, li.MsoListParagraph, div.MsoListParagraph
	{margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	text-indent:21.0pt;
	font-size:10.5pt;
	font-family:等线;}
p.MsoTocHeading, li.MsoTocHeading, div.MsoTocHeading
	{margin-top:12.0pt;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:0cm;
	margin-bottom:.0001pt;
	line-height:107%;
	page-break-after:avoid;
	font-size:16.0pt;
	font-family:"等线 Light";
	color:#2F5496;}
span.1
	{mso-style-name:"标题 1 字符";
	mso-style-link:"标题 1";
	font-weight:bold;}
span.a
	{mso-style-name:"页眉 字符";
	mso-style-link:页眉;}
span.a0
	{mso-style-name:"页脚 字符";
	mso-style-link:页脚;}
span.2
	{mso-style-name:"标题 2 字符";
	mso-style-link:"标题 2";
	font-family:"等线 Light";
	font-weight:bold;}
.MsoChpDefault
	{font-family:等线;}
 /* Page Definitions */
 @page WordSection1
	{size:595.3pt 841.9pt;
	margin:72.0pt 90.0pt 72.0pt 90.0pt;
	layout-grid:15.6pt;}
div.WordSection1
	{page:WordSection1;}
 /* List Definitions */
 ol
	{margin-bottom:0cm;}
ul
	{margin-bottom:0cm;}
-->
</style>

</head>

<body lang=ZH-CN link=blue vlink="#954F72" style='text-justify-trim:punctuation'>

<div class=WordSection1 style='layout-grid:15.6pt'>

<h1><a name="_Toc33270492"><span lang=EN-US>SRS3.0</span>代码分析</a></h1>

<p class=MsoNormal>该文档根据阅读<span lang=EN-US>srs3.0</span>源代码编写的代码分析笔记<span
lang=EN-US>(v1.00)</span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<p class=MsoTocHeading>目录</p>

<p class=MsoToc1><span lang=EN-US><a href="#_Toc33270492">SRS3.0<span
lang=EN-US><span lang=EN-US>代码分析</span></span><span style='color:windowtext;
display:none;text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc1><span lang=EN-US><a href="#_Toc33270493">SRS<span lang=EN-US><span
lang=EN-US>简介</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc1><span lang=EN-US><a href="#_Toc33270494">SRS<span lang=EN-US><span
lang=EN-US>架构</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270495">SRS<span lang=EN-US><span
lang=EN-US>系统架构</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270496">SRS<span lang=EN-US><span
lang=EN-US>模块结构</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270497">SRS<span lang=EN-US><span
lang=EN-US>媒体流发送架构</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc1><span lang=EN-US><a href="#_Toc33270498">SRS<span lang=EN-US><span
lang=EN-US>类图</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270499"><span lang=EN-US><span
lang=EN-US>类关系</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270500">SrsServer<span
lang=EN-US><span lang=EN-US>类</span></span><span style='color:windowtext;
display:none;text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270501">SrsConnection<span
lang=EN-US><span lang=EN-US>类</span></span><span style='color:windowtext;
display:none;text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270502">SrsSource<span
lang=EN-US><span lang=EN-US>类</span></span><span style='color:windowtext;
display:none;text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270503">SRS<span lang=EN-US><span
lang=EN-US>媒体流与类的关系</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc1><span lang=EN-US><a href="#_Toc33270504">SRS<span lang=EN-US><span
lang=EN-US>线程架构</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270505">SRS<span lang=EN-US><span
lang=EN-US>通用线程模型</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270506">SRS<span lang=EN-US><span
lang=EN-US>内部线程结构</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc1><span lang=EN-US><a href="#_Toc33270507">SRS<span lang=EN-US><span
lang=EN-US>程序流程</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270508">SRS<span lang=EN-US><span
lang=EN-US>启动流程</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270509">RTMP<span lang=EN-US><span
lang=EN-US>监听与连接流程</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270510">RTMP<span lang=EN-US><span
lang=EN-US>媒体流处理流程</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270511">RTMP<span lang=EN-US><span
lang=EN-US>推流流程</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoToc2><span lang=EN-US><a href="#_Toc33270512">RTMP<span lang=EN-US><span
lang=EN-US>拉流流程</span></span><span style='color:windowtext;display:none;
text-decoration:none'>... </span><span
style='color:windowtext;display:none;text-decoration:none'>1</span></a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h1><a name="_Toc33270493"><span lang=EN-US>SRS</span>简介</a></h1>

<p class=MsoNoSpacing style='text-indent:21.0pt'>官网简介<span lang=EN-US>: SRS</span>定位是运营级的互联网直播服务器集群，追求更好的概念完整性和最简单实现的代码。<span
lang=EN-US>SRS</span>提供了丰富的接入方案将<span lang=EN-US>RTMP</span>流接入<span
lang=EN-US>SRS</span>， 包括<span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_SampleRTMP"><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>推送RTMP</span></span><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>到SRS</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v2_CN_Streamer"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>推送RTSP/UDP/FLV</span></span><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>到SRS</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_Ingest"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>拉取流到SRS</span></span></a></span>。<span
lang=EN-US> SRS</span>还支持将接入的<span lang=EN-US>RTMP</span>流进行各种变换，譬如<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_SampleFFMPEG"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>将RTMP</span></span><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>流转码</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_Snapshot"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>流截图</span></span></a></span>、<span
lang=EN-US>&nbsp;<a href="https://github.com/ossrs/srs/wiki/v3_CN_SampleForward"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>转发给其他服务器</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_SampleHttpFlv"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>转封装成HTTP-FLV</span></span><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>流</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_SampleHLS"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>转封装成HLS</span></span></a></span>、<span
lang=EN-US>&nbsp;<a href="https://github.com/ossrs/srs/wiki/v2_CN_DeliveryHDS"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>转封装成HDS</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_DVR"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>录制成FLV/MP4</span></span></a></span>。<span
lang=EN-US>SRS</span>包含支大规模集群如<span lang=EN-US>CDN</span>业务的关键特性， 譬如<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_SampleRTMPCluster"><span
style='color:windowtext;text-decoration:none'>RTMP</span><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>多级集群</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_OriginCluster"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>源站集群</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_RtmpUrlVhost"><span
style='color:windowtext;text-decoration:none'>VHOST</span><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>虚拟服务器&nbsp;</span></span></a></span>、<span
lang=EN-US>&nbsp;<a href="https://github.com/ossrs/srs/wiki/v1_CN_Reload"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>无中断服务Reload</span></span></a></span>、<span
lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_SampleHttpFlvCluster"><span
style='color:windowtext;text-decoration:none'>HTTP-FLV</span><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>集群</span></span></a></span>。此外，<span
lang=EN-US>SRS</span>还提供丰富的应用接口， 包括<span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPCallback"><span
style='color:windowtext;text-decoration:none'>HTTP</span><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>回调</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v2_CN_Security"><span
lang=EN-US style='color:windowtext;text-decoration:none'><span lang=EN-US>安全策略Security</span></span></a></span>、<span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi"><span
style='color:windowtext;text-decoration:none'>HTTP API</span><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>接口</span></span></a></span>、<span
lang=EN-US>&nbsp;<a
href="https://github.com/ossrs/srs/wiki/v1_CN_BandwidthTestTool"><span
style='color:windowtext;text-decoration:none'>RTMP</span><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>测速</span></span></a></span>。<span
lang=EN-US>SRS</span>在源站和<span lang=EN-US>CDN</span>集群中都得到了广泛的<span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_Sample"><span lang=EN-US
style='color:windowtext;text-decoration:none'><span lang=EN-US>应用Applications</span></span></a></span>。</p>

<p class=MsoNormal><span lang=EN-US>srs</span>架构</p>

<p class=MsoNormal style='text-indent:21.0pt'>官网源码仓库<span lang=EN-US>: <a
href="https://github.com/ossrs/srs">https://github.com/ossrs/srs</a></span></p>

<p class=MsoNormal style='text-indent:21.0pt'>官网<span lang=EN-US>wiki: <a
href="https://github.com/ossrs/srs/wiki">https://github.com/ossrs/srs/wiki</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;&nbsp;&nbsp; </span></p>

<h1><a name="_Toc33270494"><span lang=EN-US>SRS</span>架构</a></h1>

<h2><a name="_Toc33270495"><span lang=EN-US>SRS</span>系统架构</a></h2>

<p class=MsoNormal>图片来自<span lang=EN-US>srs</span>官网<span lang=EN-US>wiki</span></p>

<p class=MsoNormal><span lang=EN-US><img border=0 width=934 height=574 id="图片 1"
src="srs_note.files/image001.jpg"></span></p>

<h2><a name="_Toc33270496"><span lang=EN-US>SRS</span>模块结构</a></h2>

<p class=MsoNormal>图片来自<span lang=EN-US>srs</span>官网<span lang=EN-US>wiki</span></p>

<p class=MsoNormal><span lang=EN-US><img border=0 width=938 height=545 id="图片 2"
src="srs_note.files/image002.jpg"></span></p>

<h2><a name="_Toc33270497"><span lang=EN-US>SRS</span>媒体流架构</a></h2>

<p class=MsoNormal>图片来自<span lang=EN-US>srs</span>官网<span lang=EN-US>wiki</span></p>

<p class=MsoNormal><span lang=EN-US><img border=0 width=832 height=875 id="图片 3"
src="srs_note.files/image003.jpg"></span></p>

<h1><a name="_Toc33270498"><span lang=EN-US>SRS</span>类图</a></h1>

<h2><a name="_Toc33270499">类关系</a></h2>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1502 height=1309
src="srs_note.files/image004.png"></span></p>

<h2><a name="_Toc33270500"><span lang=EN-US>SrsServer</span>类</a></h2>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1370 height=1090
id="图片 4" src="srs_note.files/image005.png"></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h2><a name="_Toc33270501"><span lang=EN-US>SrsConnection</span>类</a></h2>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<p class=MsoNormal><span lang=EN-US><img border=0 width=898 height=920
src="srs_note.files/image006.png"></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h2><a name="_Toc33270502"><span lang=EN-US>SrsSource</span>类</a></h2>

<p class=MsoNormal><span lang=EN-US>….</span></p>

<h2><a name="_Toc33270503"><span lang=EN-US>SRS</span>媒体流与类的关系</a></h2>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'><span
lang=EN-US>&nbsp;&nbsp; srs</span>启动之后，客户端推拉流时，需要调用下面这些主要类来相互协作完成推拉流功能， 该流程描述媒体在<span
lang=EN-US>srs</span>主要类之间的静态流程。</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'><span
lang=EN-US><img border=0 width=1293 height=1380
src="srs_note.files/image007.png"></span></p>

<p class=MsoListParagraph style='margin-left:36.0pt;text-indent:-18.0pt'><span
lang=EN-US>1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>客户端发送<span lang=EN-US>rtmp</span>连接请求，<span lang=EN-US>SrsListener</span>收到<span
lang=EN-US>connect</span>请求后，创建一个<span lang=EN-US>SrsConnection</span>，每个<span
lang=EN-US>SrsConnection</span>会启动一个线程来完成相应任务</p>

<p class=MsoListParagraph style='margin-left:36.0pt;text-indent:-18.0pt'><span
lang=EN-US>2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsRtmpConn</span>首先按<span lang=EN-US>rtmp</span>协议流程交互成功之后，根据请求<span
lang=EN-US>url</span>创建流名流类型等标启，同时调用<span lang=EN-US>fetch_or_create</span>生成一个处理音视频源的<span
lang=EN-US>SrsSource,</span>，</p>

<p class=MsoNormal style='margin-left:18.0pt;text-indent:21.0pt'><b>如果是推流</b>：</p>

<p class=MsoNormal style='margin-left:36.0pt;text-indent:21.0pt'>创建<span
lang=EN-US>SrsPublishRecvThread</span>线程，接收客户端发送过来<span lang=EN-US>rtmp</span>数据包，数据包由<span
lang=EN-US>SrsRtmpServer</span>来处理，如果是音视频数据，由<span lang=EN-US>process_publish_message</span>来处理，它会通过<span
lang=EN-US>SrsSource</span>对媒体流的进行处理</p>

<p class=MsoListParagraph style='margin-left:54.0pt;text-indent:-18.0pt'><span
lang=EN-US>1》<span style='font:7.0pt "Times New Roman"'> </span></span><span
lang=EN-US>&nbsp;</span>如果该服务是边缘服务，<span lang=EN-US>SrsSource</span>直接将媒体<span
lang=EN-US>proxy publish</span>到源站服务，</p>

<p class=MsoListParagraph style='margin-left:54.0pt;text-indent:-18.0pt'><span
lang=EN-US>2》<span style='font:7.0pt "Times New Roman"'> </span></span><span
lang=EN-US>&nbsp;</span>否则<span lang=EN-US>SrsSource</span>会将<span lang=EN-US>publish</span>流放入到每个<span
lang=EN-US>SrsConsumer</span>的媒体数据对列中<span lang=EN-US>,</span>一个<span
lang=EN-US>SrsConsumber</span>就是一个播放客户端。同时调用<span lang=EN-US>SrsOriginHub</span>将媒体流根据配置来生成<span
lang=EN-US>flv,hls,mp4</span>录相文件，以及是否将发布流转发到其他<span lang=EN-US>rtmp</span>服务器等<span
lang=EN-US>;</span>最后检查如果启用<span lang=EN-US>GopCache</span>会将媒体流写入<span
lang=EN-US>GopCache</span>对列中<span lang=EN-US>.</span>用于当一个新的播放请求来时，保证首先能获取一个<span
lang=EN-US>gop</span>数据，以防播放开始时不黑屏或花屏</p>

<p class=MsoListParagraph style='margin-left:18.0pt'><b>如果拉流</b>：</p>

<p class=MsoListParagraph style='margin-left:57.0pt;text-indent:-18.0pt'><b><span
lang=EN-US>1》<span style='font:7.0pt "Times New Roman"'> </span></span></b>如果是源站拉流同时启用源站集群，如果流不是该源站发布，则根据配置的发送<span
lang=EN-US>api</span>请求到其他源站，检查是否在其他源站发布了流，如果是，则发送一个<span lang=EN-US>redirect</span>，要求拉流客户端重定向指定服务器拉流。<b>注意<span
lang=EN-US>rtmp</span>重定向信令，如果客户端直接请求的源站，要求<span lang=EN-US>rtmp</span>客户端支持<span
lang=EN-US>redirect</span>，如果<span lang=EN-US>srs</span>边缘回源到源站后再重定向，那是没有问题的，因为<span
lang=EN-US>srs</span>边缘支持<span lang=EN-US>redirect</span></b></p>

<p class=MsoListParagraph style='margin-left:57.0pt;text-indent:-18.0pt'><b><span
lang=EN-US>2》<span style='font:7.0pt "Times New Roman"'> </span></span></b>如果不走第<span
lang=EN-US>1</span>步，则创建一个<span lang=EN-US>SrsConsumer</span>与<span lang=EN-US>SrsQueueRecvThread</span>线程<span
lang=EN-US>, </span>创建<span lang=EN-US>SrsConsumer</span>时，如果启用<span
lang=EN-US>gopcache</span>，首先会将<span lang=EN-US>gopcache</span>媒体数据插入<span
lang=EN-US>SrsConsumer</span>的数据队列中。如果是边缘拉流，则使用<span lang=EN-US>SrsPlayEdge</span>回源拉流。将回源拉的媒体流数据插入<span
lang=EN-US>SrsConsumer</span>的数据队列中</p>

<p class=MsoListParagraph style='margin-left:57.0pt;text-indent:-18.0pt'><b><span
lang=EN-US>3》<span style='font:7.0pt "Times New Roman"'> </span></span></b><span
lang=EN-US>SrsQueueRecvThread</span>线程负责将<span lang=EN-US>SrsConsumer</span>的数据队列中的媒体数据发送给客户端。<span
lang=EN-US>SrsConsumer</span>队列中数据来源于<span lang=EN-US>GopCache</span>，源站<span
lang=EN-US>publish</span>的数据，以及回源拉流的数据</p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h1><a name="_Toc33270504"><span lang=EN-US>SRS</span>线程架构</a></h1>

<h2><a name="_Toc33270505"><span lang=EN-US>SRS</span>通用线程模型</a></h2>

<p class=MsoNormal><span lang=EN-US>srs</span>线程内部是使用协程库<span lang=EN-US>(State
Threads)</span>实现，</p>

<p class=MsoNormal><span lang=EN-US>srs</span>线程模型如下</p>

<p class=MsoNormal><span lang=EN-US><img border=0 width=795 height=953
src="srs_note.files/image008.png"></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h2><a name="_Toc33270506"><span lang=EN-US>SRS</span>内部线程结构</a></h2>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1829 height=1156
src="srs_note.files/image009.png"></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h1><a name="_Toc33270507"><span lang=EN-US>SRS</span>程序流程</a></h1>

<h2><a name="_Toc33270508"><span lang=EN-US>SRS</span>启动流程</a></h2>

<p class=MsoNormal><span lang=EN-US><img border=0 width=877 height=990
src="srs_note.files/image010.png"></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>首先检查解析启动命令参数，初始日志接口，检查配置文件是否正确</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>创建<span lang=EN-US>SrsServer</span>服务，初始化一些变量</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>检查是否后台运行还是控制台运行</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>初始化<span lang=EN-US>st </span>协程库，信息号管理器</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>5.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>如果后台运行写进程<span lang=EN-US>pid</span>到文件</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>6.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>监听连接：</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:10.5pt'><span
lang=EN-US>listen_rtmp: rtmp</span>推流或拉流连接</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'><span
lang=EN-US>&nbsp; listen_http_api: api</span>请求连接</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'><span
lang=EN-US>&nbsp;&nbsp;listen_http_stream: http</span>拉流连接<span lang=EN-US>,http-flv
,http-ts</span>，<span lang=EN-US>http-aac</span>，<span lang=EN-US>http-mp3</span></p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'><span
lang=EN-US>&nbsp;&nbsp;listen_stream_caster: </span>接收<span lang=EN-US>MpegTSOverUdp</span>流请求，<span
lang=EN-US>rtsp</span>推流请求，<span lang=EN-US>http-flv</span>推流请求</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>7.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>初始化<span lang=EN-US>http_api</span>接口处理</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>8.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>启动<span lang=EN-US>ingest</span>协程，使用<span lang=EN-US>ffmpeg, </span>拉取文件或流转发到本服务</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>9.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>启动主线程</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></p>

<h2><a name="_Toc33270509"><span lang=EN-US>RTMP</span>监听与连接流程</a></h2>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1205 height=675
src="srs_note.files/image011.png"></span></p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SerServer</span>调用<span lang=EN-US>listern</span>启动<span
lang=EN-US>rtmp</span>监听线程</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>客户端发送连接请求，监听线程收到请求后，发送<span lang=EN-US>on_tcp_accetpt()</span>事件</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsrServer</span>处理<span lang=EN-US>accetp_client()
</span>创建一个新的<span lang=EN-US>SrsRtmpConn,</span>同时启动<span lang=EN-US>SrsRtmpConnThread</span>连接线程</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsRtmpConnThread</span>收到客户端<span lang=EN-US>rtmp</span>握手，同时根据<span
lang=EN-US>rtmp</span>连接流程创建一个<span lang=EN-US>rtmp</span>连接</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>5.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>连接成功之后<span lang=EN-US>,</span>调用<span lang=EN-US>stream_service_cycle</span>对<span
lang=EN-US>rtmp</span>媒体流处理</p>

<h2><a name="_Toc33270510"><span lang=EN-US>RTMP</span>媒体流处理流程</a></h2>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1595 height=1124
src="srs_note.files/image012.png"></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>identify_client </span>根据客户端请求类型创建流名，流<span
lang=EN-US>Id</span>，流类型（推拉流）等客户端标识信息</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>check_vhost </span>根据配置检查域名是否合法</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>http_hooks_on_connect </span>发送<span lang=EN-US>on_connect</span>事件</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>check</span>检测根据配置检查是否允许推拉流</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>5.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>根据请求创建或获取<span lang=EN-US>SrsSource</span>对象</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>6.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>根据流类型调用对应的推或拉流流程</p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h2><a name="_Toc33270511"><span lang=EN-US>RTMP</span>推流流程</a></h2>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1151 height=1498
src="srs_note.files/image013.png"></span></p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>接收客户端发布流交互消息，<span lang=EN-US>start_fmle_publish</span>完成发布流交互</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>发送<span lang=EN-US>on_pulibsh</span>事件</p>

<p class=MsoListParagraph align=left style='margin-left:18.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US>3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsSource::can_publish </span>检查<span
lang=EN-US>SrsSource</span>流的是否已发布，如果是返回，不再发布</p>

<p class=MsoListParagraph align=left style='margin-left:18.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US>4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>检查是否边缘推流，如果是启动<span lang=EN-US>SrsEdgeForwarder</span>线程，将流推向源站</p>

<p class=MsoListParagraph align=left style='margin-left:18.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US>5.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsSource::on_publish</span>，如果配置<span
lang=EN-US>flv,hls,mp4</span>等，则开始录相，如配置转发，则启动转发线程</p>

<p class=MsoListParagraph align=left style='margin-left:18.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US>6.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>启动<span lang=EN-US>SrsPublishRecvThread,</span>线程，接收客户端数据，调用<span
lang=EN-US>SrsRtmpConn::handle_publish_message</span>处理数据</p>

<p class=MsoListParagraph align=left style='margin-left:18.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US>7.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsRtmpConn:::process_publish_message</span>处理推流数据</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>8.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>如果是边缘推流，将数据<span lang=EN-US>SrsEdgeForwarder</span>对列，将数据发送到源站</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>9.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>如是不是边缘推流，调用<span lang=EN-US>SrsSource</span>相关方法处理音视频数据<span
lang=EN-US>. </span>对<span lang=EN-US>hls,mp4,flv</span>录相，转发，<span lang=EN-US>gopCache</span>，以其放到<span
lang=EN-US>SrsConsumber</span>的消息对列中，</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'>每个<span
lang=EN-US>,SrsConsumber</span>是一个播放客户端</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>10.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span>如果停止推流，<span
lang=EN-US> SrsPublishRecvThread</span>将<span lang=EN-US>stop</span>退出线程， </p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>11.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span>调用<span
lang=EN-US>on_edge_proxy_unpublish</span>停止边缘推流线程</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>12.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
lang=EN-US>SrsSource::on_unpublish,</span>停止<span lang=EN-US>hls.,mp4,flv, </span>转发，清容<span
lang=EN-US>gopCache</span></p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>13.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
lang=EN-US>http_hook_on_unpublish</span>发送<span lang=EN-US>on_unpublish</span>事件</p>

<h2><a name="_Toc33270512"><span lang=EN-US>RTMP</span>拉流流程</a></h2>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1856 height=1204
src="srs_note.files/image014.png"></span></p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsRtmpServer::start_play </span>根据<span
lang=EN-US>rtmp</span>协议 完成<span lang=EN-US>play</span>流程</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>SrsRtmpConn::http_hook_on_play </span>发送<span
lang=EN-US>on_play</span>事件，</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>playing</span>检查是否开启源站集群，如果是，且流没有在该源站发布，向其他源站发送请求，检查流在哪个源站发布，如果找到，重定向到该源站</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span>如是不是源站集群，<span lang=EN-US>create_consumer</span>创建<span
lang=EN-US>consumer</span>，同时将<span lang=EN-US>gop</span>缓冲数据放入<span
lang=EN-US>consumer</span>消息队列中，如果是边缘拉流，启动<span lang=EN-US>SrsEdgeIngester</span>回源拉流</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>5.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>recv_messae</span>接收客户端信息<span lang=EN-US>,</span>放下<span
lang=EN-US>consumer</span>消息对列中， <span lang=EN-US>pump</span>从队列获取消息，<span
lang=EN-US>process_play_control_msg</span>处理<span lang=EN-US>rtmp</span>控制消息</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>6.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>dump_packets</span>从<span lang=EN-US>consumber</span>的消息队列中获取媒体数据，<span
lang=EN-US> send_and_free_message </span>发送给给客户端</p>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:-18.0pt'><span
lang=EN-US>7.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US>stop</span>停止播， <span lang=EN-US>http_hook_on_stop</span>发送<span
lang=EN-US>on_stop</span>事件</p>

</div>

</body>

</html>
