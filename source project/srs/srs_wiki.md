<html>

<head>
<meta http-equiv=Content-Type content="text/html; charset=gb2312">
<meta name=Generator content="Microsoft Word 15 (filtered)">
<title>开源流媒体SRS介绍</title>
<style>
<!--
 /* Font Definitions */
 @font-face
	{font-family:Helvetica;
	panose-1:2 11 6 4 2 2 2 2 2 4;}
@font-face
	{font-family:Courier;
	panose-1:2 7 4 9 2 2 5 2 4 4;}
@font-face
	{font-family:"Tms Rmn";
	panose-1:2 2 6 3 4 5 5 2 3 4;}
@font-face
	{font-family:Helv;
	panose-1:2 11 6 4 2 2 2 3 2 4;}
@font-face
	{font-family:"New York";
	panose-1:2 4 5 3 6 5 6 2 3 4;}
@font-face
	{font-family:System;
	panose-1:0 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:Wingdings;
	panose-1:5 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"MS Mincho";
	panose-1:2 2 6 9 4 2 5 8 3 4;}
@font-face
	{font-family:Batang;
	panose-1:2 3 6 0 0 1 1 1 1 1;}
@font-face
	{font-family:宋体;
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:PMingLiU;
	panose-1:2 1 6 1 0 1 1 1 1 1;}
@font-face
	{font-family:"MS Gothic";
	panose-1:2 11 6 9 7 2 5 8 2 4;}
@font-face
	{font-family:Dotum;
	panose-1:2 11 6 0 0 1 1 1 1 1;}
@font-face
	{font-family:黑体;
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:MingLiU;
	panose-1:2 1 6 9 0 1 1 1 1 1;}
@font-face
	{font-family:Mincho;
	panose-1:2 2 6 9 4 3 5 8 3 5;}
@font-face
	{font-family:Gulim;
	panose-1:2 11 6 0 0 1 1 1 1 1;}
@font-face
	{font-family:Century;
	panose-1:2 4 6 4 5 5 5 2 3 4;}
@font-face
	{font-family:"Angsana New";
	panose-1:2 2 6 3 5 4 5 2 3 4;}
@font-face
	{font-family:"Cordia New";
	panose-1:2 11 3 4 2 2 2 2 2 4;}
@font-face
	{font-family:Mangal;
	panose-1:0 0 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:Latha;
	panose-1:2 0 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:Sylfaen;
	panose-1:1 10 5 2 5 3 6 3 3 3;}
@font-face
	{font-family:Vrinda;
	panose-1:0 0 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:Raavi;
	panose-1:2 0 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:Shruti;
	panose-1:2 0 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:Sendnya;
	panose-1:0 0 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:Gautami;
	panose-1:2 0 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:Tunga;
	panose-1:0 0 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Estrangelo Edessa";
	panose-1:0 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Cambria Math";
	panose-1:2 4 5 3 5 4 6 3 2 4;}
@font-face
	{font-family:"Yu Gothic";
	panose-1:2 11 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:等线;
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:Calibri;
	panose-1:2 15 5 2 2 2 4 3 2 4;}
@font-face
	{font-family:"Calibri Light";
	panose-1:2 15 3 2 2 2 4 3 2 4;}
@font-face
	{font-family:"Palatino Linotype";
	panose-1:2 4 5 2 5 5 5 3 3 4;}
@font-face
	{font-family:Verdana;
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Arial Unicode MS";
	panose-1:2 11 6 4 2 2 2 2 2 4;}
@font-face
	{font-family:"等线 Light";
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:方正等线;
	panose-1:3 0 5 9 0 0 0 0 0 0;}
@font-face
	{font-family:"Segoe UI Emoji";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:Cambria;
	panose-1:2 4 5 3 5 4 6 3 2 4;}
@font-face
	{font-family:"Microsoft YaHei UI";
	panose-1:2 11 5 3 2 2 4 2 2 4;}
@font-face
	{font-family:"Segoe UI";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:Consolas;
	panose-1:2 11 6 9 2 2 4 3 2 4;}
@font-face
	{font-family:微软雅黑;
	panose-1:2 11 5 3 2 2 4 2 2 4;}
@font-face
	{font-family:Simsun;
	panose-1:0 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:TeamViewer13;}
@font-face
	{font-family:Marlett;
	panose-1:0 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Arial Black";
	panose-1:2 11 10 4 2 1 2 2 2 4;}
@font-face
	{font-family:"Bahnschrift Light";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Bahnschrift SemiLight";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:Bahnschrift;
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Bahnschrift SemiBold";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:Candara;
	panose-1:2 14 5 2 3 3 3 2 2 4;}
@font-face
	{font-family:"Comic Sans MS";
	panose-1:3 15 7 2 3 3 2 2 2 4;}
@font-face
	{font-family:Constantia;
	panose-1:2 3 6 2 5 3 6 3 3 3;}
@font-face
	{font-family:Corbel;
	panose-1:2 11 5 3 2 2 4 2 2 4;}
@font-face
	{font-family:Ebrima;
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Franklin Gothic Medium";
	panose-1:2 11 6 3 2 1 2 2 2 4;}
@font-face
	{font-family:Gabriola;
	panose-1:4 4 6 5 5 16 2 2 13 2;}
@font-face
	{font-family:Gadugi;
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:Georgia;
	panose-1:2 4 5 2 5 4 5 2 3 3;}
@font-face
	{font-family:Impact;
	panose-1:2 11 8 6 3 9 2 5 2 4;}
@font-face
	{font-family:"Javanese Text";
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Leelawadee UI";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Leelawadee UI Semilight";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Lucida Console";
	panose-1:2 11 6 9 4 5 4 2 2 4;}
@font-face
	{font-family:"Lucida Sans Unicode";
	panose-1:2 11 6 2 3 5 4 2 2 4;}
@font-face
	{font-family:"Malgun Gothic";
	panose-1:2 11 5 3 2 0 0 2 0 4;}
@font-face
	{font-family:"\@Malgun Gothic";
	panose-1:2 11 5 3 2 0 0 2 0 4;}
@font-face
	{font-family:"Malgun Gothic Semilight";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"\@Malgun Gothic Semilight";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Microsoft Himalaya";
	panose-1:1 1 1 0 1 1 1 1 1 1;}
@font-face
	{font-family:"Microsoft JhengHei";
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"\@Microsoft JhengHei";
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Microsoft JhengHei UI";
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"\@Microsoft JhengHei UI";
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Microsoft JhengHei Light";
	panose-1:2 11 3 4 3 5 4 4 2 4;}
@font-face
	{font-family:"\@Microsoft JhengHei Light";
	panose-1:2 11 3 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Microsoft JhengHei UI Light";
	panose-1:2 11 3 4 3 5 4 4 2 4;}
@font-face
	{font-family:"\@Microsoft JhengHei UI Light";
	panose-1:2 11 3 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Microsoft New Tai Lue";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Microsoft PhagsPa";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Microsoft Sans Serif";
	panose-1:2 11 6 4 2 2 2 2 2 4;}
@font-face
	{font-family:"Microsoft Tai Le";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"\@微软雅黑";
	panose-1:2 11 5 3 2 2 4 2 2 4;}
@font-face
	{font-family:"\@Microsoft YaHei UI";
	panose-1:2 11 5 3 2 2 4 2 2 4;}
@font-face
	{font-family:"微软雅黑 Light";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"\@微软雅黑 Light";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Microsoft YaHei UI Light";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"\@Microsoft YaHei UI Light";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Microsoft Yi Baiti";
	panose-1:3 0 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:MingLiU-ExtB;
	panose-1:2 2 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@MingLiU-ExtB";
	panose-1:2 2 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:PMingLiU-ExtB;
	panose-1:2 2 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@PMingLiU-ExtB";
	panose-1:2 2 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:MingLiU_HKSCS-ExtB;
	panose-1:2 2 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@MingLiU_HKSCS-ExtB";
	panose-1:2 2 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Mongolian Baiti";
	panose-1:3 0 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@MS Gothic";
	panose-1:2 11 6 9 7 2 5 8 2 4;}
@font-face
	{font-family:"MS UI Gothic";
	panose-1:2 11 6 0 7 2 5 8 2 4;}
@font-face
	{font-family:"\@MS UI Gothic";
	panose-1:2 11 6 0 7 2 5 8 2 4;}
@font-face
	{font-family:"MS PGothic";
	panose-1:2 11 6 0 7 2 5 8 2 4;}
@font-face
	{font-family:"\@MS PGothic";
	panose-1:2 11 6 0 7 2 5 8 2 4;}
@font-face
	{font-family:"MV Boli";
	panose-1:2 0 5 0 3 2 0 9 0 0;}
@font-face
	{font-family:"Myanmar Text";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Nirmala UI";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Nirmala UI Semilight";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe MDL2 Assets";
	panose-1:5 10 1 2 1 1 1 1 1 1;}
@font-face
	{font-family:"Segoe Print";
	panose-1:2 0 6 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Segoe Script";
	panose-1:3 11 5 4 2 0 0 0 0 3;}
@font-face
	{font-family:"Segoe UI Black";
	panose-1:2 11 10 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe UI Historic";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe UI Light";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe UI Semibold";
	panose-1:2 11 7 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe UI Semilight";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe UI Symbol";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"\@宋体";
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:新宋体;
	panose-1:2 1 6 9 3 1 1 1 1 1;}
@font-face
	{font-family:"\@新宋体";
	panose-1:2 1 6 9 3 1 1 1 1 1;}
@font-face
	{font-family:SimSun-ExtB;
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:"\@SimSun-ExtB";
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:"Sitka Small";
	panose-1:2 0 5 5 0 0 0 2 0 4;}
@font-face
	{font-family:"Sitka Text";
	panose-1:2 0 5 5 0 0 0 2 0 4;}
@font-face
	{font-family:"Sitka Subheading";
	panose-1:2 0 5 5 0 0 0 2 0 4;}
@font-face
	{font-family:"Sitka Heading";
	panose-1:2 0 5 5 0 0 0 2 0 4;}
@font-face
	{font-family:"Sitka Display";
	panose-1:2 0 5 5 0 0 0 2 0 4;}
@font-face
	{font-family:"Sitka Banner";
	panose-1:2 0 5 5 0 0 0 2 0 4;}
@font-face
	{font-family:Tahoma;
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Trebuchet MS";
	panose-1:2 11 6 3 2 2 2 2 2 4;}
@font-face
	{font-family:Webdings;
	panose-1:5 3 1 2 1 5 9 6 7 3;}
@font-face
	{font-family:"\@Yu Gothic";
	panose-1:2 11 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Yu Gothic UI";
	panose-1:2 11 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@Yu Gothic UI";
	panose-1:2 11 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Yu Gothic UI Semibold";
	panose-1:2 11 7 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@Yu Gothic UI Semibold";
	panose-1:2 11 7 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Yu Gothic Light";
	panose-1:2 11 3 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@Yu Gothic Light";
	panose-1:2 11 3 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Yu Gothic UI Light";
	panose-1:2 11 3 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@Yu Gothic UI Light";
	panose-1:2 11 3 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Yu Gothic Medium";
	panose-1:2 11 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@Yu Gothic Medium";
	panose-1:2 11 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Yu Gothic UI Semilight";
	panose-1:2 11 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@Yu Gothic UI Semilight";
	panose-1:2 11 4 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@等线";
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:"\@等线 Light";
	panose-1:2 1 6 0 3 1 1 1 1 1;}
@font-face
	{font-family:仿宋;
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:"\@仿宋";
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:楷体;
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:"\@楷体";
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:"\@黑体";
	panose-1:2 1 6 9 6 1 1 1 1 1;}
@font-face
	{font-family:"HoloLens MDL2 Assets";
	panose-1:5 10 1 2 1 1 1 1 1 1;}
@font-face
	{font-family:方正舒体;
	panose-1:2 1 6 1 3 1 1 1 1 1;}
@font-face
	{font-family:"\@方正舒体";
	panose-1:2 1 6 1 3 1 1 1 1 1;}
@font-face
	{font-family:方正姚体;
	panose-1:2 1 6 1 3 1 1 1 1 1;}
@font-face
	{font-family:"\@方正姚体";
	panose-1:2 1 6 1 3 1 1 1 1 1;}
@font-face
	{font-family:隶书;
	panose-1:2 1 5 9 6 1 1 1 1 1;}
@font-face
	{font-family:"\@隶书";
	panose-1:2 1 5 9 6 1 1 1 1 1;}
@font-face
	{font-family:华文彩云;
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文彩云";
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文仿宋;
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文仿宋";
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文琥珀;
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文琥珀";
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文楷体;
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文楷体";
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文隶书;
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文隶书";
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文宋体;
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文宋体";
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文细黑;
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文细黑";
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文行楷;
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文行楷";
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文新魏;
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文新魏";
	panose-1:2 1 8 0 4 1 1 1 1 1;}
@font-face
	{font-family:华文中宋;
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:"\@华文中宋";
	panose-1:2 1 6 0 4 1 1 1 1 1;}
@font-face
	{font-family:幼圆;
	panose-1:2 1 5 9 6 1 1 1 1 1;}
@font-face
	{font-family:"\@幼圆";
	panose-1:2 1 5 9 6 1 1 1 1 1;}
@font-face
	{font-family:"MT Extra";
	panose-1:5 5 1 2 1 2 5 2 2 2;}
@font-face
	{font-family:"Book Antiqua";
	panose-1:2 4 6 2 5 3 5 3 3 4;}
@font-face
	{font-family:"Century Gothic";
	panose-1:2 11 5 2 2 2 2 2 2 4;}
@font-face
	{font-family:Haettenschweiler;
	panose-1:2 11 7 6 4 9 2 6 2 4;}
@font-face
	{font-family:"Tempus Sans ITC";
	panose-1:4 2 4 4 3 13 7 2 2 2;}
@font-face
	{font-family:Mistral;
	panose-1:3 9 7 2 3 4 7 2 4 3;}
@font-face
	{font-family:"Lucida Handwriting";
	panose-1:3 1 1 1 1 1 1 1 1 1;}
@font-face
	{font-family:"Kristen ITC";
	panose-1:3 5 5 2 4 2 2 3 2 2;}
@font-face
	{font-family:"Juice ITC";
	panose-1:4 4 4 3 4 10 2 2 2 2;}
@font-face
	{font-family:"Freestyle Script";
	panose-1:3 8 4 2 3 2 5 11 4 4;}
@font-face
	{font-family:"Arial Narrow";
	panose-1:2 11 6 6 2 2 2 3 2 4;}
@font-face
	{font-family:Garamond;
	panose-1:2 2 4 4 3 3 1 1 8 3;}
@font-face
	{font-family:"Monotype Corsiva";
	panose-1:3 1 1 1 1 2 1 1 1 1;}
@font-face
	{font-family:Algerian;
	panose-1:4 2 7 5 4 10 2 6 7 2;}
@font-face
	{font-family:"Baskerville Old Face";
	panose-1:2 2 6 2 8 5 5 2 3 3;}
@font-face
	{font-family:"Bauhaus 93";
	panose-1:4 3 9 5 2 11 2 2 12 2;}
@font-face
	{font-family:"Bell MT";
	panose-1:2 2 5 3 6 3 5 2 3 3;}
@font-face
	{font-family:"Berlin Sans FB";
	panose-1:2 14 6 2 2 5 2 2 3 6;}
@font-face
	{font-family:"Bernard MT Condensed";
	panose-1:2 5 8 6 6 9 5 2 4 4;}
@font-face
	{font-family:"Bodoni MT Poster Compressed";
	panose-1:2 7 7 6 8 6 1 5 2 4;}
@font-face
	{font-family:"Britannic Bold";
	panose-1:2 11 9 3 6 7 3 2 2 4;}
@font-face
	{font-family:Broadway;
	panose-1:4 4 9 5 8 11 2 2 5 2;}
@font-face
	{font-family:"Brush Script MT";
	panose-1:3 6 8 2 4 4 6 7 3 4;}
@font-face
	{font-family:"Californian FB";
	panose-1:2 7 4 3 6 8 11 3 2 4;}
@font-face
	{font-family:Centaur;
	panose-1:2 3 5 4 5 2 5 2 3 4;}
@font-face
	{font-family:Chiller;
	panose-1:4 2 4 4 3 16 7 2 6 2;}
@font-face
	{font-family:"Colonna MT";
	panose-1:4 2 8 5 6 2 2 3 2 3;}
@font-face
	{font-family:"Cooper Black";
	panose-1:2 8 9 4 4 3 11 2 4 4;}
@font-face
	{font-family:"Footlight MT Light";
	panose-1:2 4 6 2 6 3 10 2 3 4;}
@font-face
	{font-family:"Harlow Solid Italic";
	panose-1:4 3 6 4 2 15 2 2 13 2;}
@font-face
	{font-family:Harrington;
	panose-1:4 4 5 5 5 10 2 2 7 2;}
@font-face
	{font-family:"High Tower Text";
	panose-1:2 4 5 2 5 5 6 3 3 3;}
@font-face
	{font-family:Jokerman;
	panose-1:4 9 6 5 6 13 6 2 7 2;}
@font-face
	{font-family:"Kunstler Script";
	panose-1:3 3 4 2 2 6 7 13 13 6;}
@font-face
	{font-family:"Lucida Bright";
	panose-1:2 4 6 2 5 5 5 2 3 4;}
@font-face
	{font-family:"Lucida Calligraphy";
	panose-1:3 1 1 1 1 1 1 1 1 1;}
@font-face
	{font-family:"Lucida Fax";
	panose-1:2 6 6 2 5 5 5 2 2 4;}
@font-face
	{font-family:Magneto;
	panose-1:4 3 8 5 5 8 2 2 13 2;}
@font-face
	{font-family:"Matura MT Script Capitals";
	panose-1:3 2 8 2 6 6 2 7 2 2;}
@font-face
	{font-family:"Modern No\. 20";
	panose-1:2 7 7 4 7 5 5 2 3 3;}
@font-face
	{font-family:"Niagara Engraved";
	panose-1:4 2 5 2 7 7 3 3 2 2;}
@font-face
	{font-family:"Niagara Solid";
	panose-1:4 2 5 2 7 7 2 2 2 2;}
@font-face
	{font-family:"Old English Text MT";
	panose-1:3 4 9 2 4 5 8 3 8 6;}
@font-face
	{font-family:Onyx;
	panose-1:4 5 6 2 8 7 2 2 2 3;}
@font-face
	{font-family:Parchment;
	panose-1:3 4 6 2 4 7 8 4 8 4;}
@font-face
	{font-family:Playbill;
	panose-1:4 5 6 3 10 6 2 2 2 2;}
@font-face
	{font-family:"Poor Richard";
	panose-1:2 8 5 2 5 5 5 2 7 2;}
@font-face
	{font-family:Ravie;
	panose-1:4 4 8 5 5 8 9 2 6 2;}
@font-face
	{font-family:"Informal Roman";
	panose-1:3 6 4 2 3 4 6 11 2 4;}
@font-face
	{font-family:"Showcard Gothic";
	panose-1:4 2 9 4 2 1 2 2 6 4;}
@font-face
	{font-family:"Snap ITC";
	panose-1:4 4 10 7 6 10 2 2 2 2;}
@font-face
	{font-family:Stencil;
	panose-1:4 4 9 5 13 8 2 2 4 4;}
@font-face
	{font-family:"Viner Hand ITC";
	panose-1:3 7 5 2 3 5 2 2 2 3;}
@font-face
	{font-family:Vivaldi;
	panose-1:3 2 6 2 5 5 6 9 8 4;}
@font-face
	{font-family:"Vladimir Script";
	panose-1:3 5 4 2 4 4 7 7 3 5;}
@font-face
	{font-family:"Wide Latin";
	panose-1:2 10 10 7 5 5 5 2 4 4;}
@font-face
	{font-family:"Bookman Old Style";
	panose-1:2 5 6 4 5 5 5 2 2 4;}
@font-face
	{font-family:"Berlin Sans FB Demi";
	panose-1:2 14 8 2 2 5 2 2 3 6;}
@font-face
	{font-family:"\@方正等线";
	panose-1:3 0 5 9 0 0 0 0 0 0;}
@font-face
	{font-family:"Microsoft MHei";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"\@Microsoft MHei";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Microsoft NeoGothic";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"\@Microsoft NeoGothic";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe WP Black";
	panose-1:2 11 10 2 4 5 4 2 2 3;}
@font-face
	{font-family:"Segoe WP";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe WP Semibold";
	panose-1:2 11 7 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe WP Light";
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Segoe WP SemiLight";
	panose-1:2 11 4 2 4 2 4 2 2 3;}
@font-face
	{font-family:"HP Simplified";
	panose-1:2 11 6 4 2 2 4 2 2 4;}
@font-face
	{font-family:"HP Simplified Light";
	panose-1:2 11 4 4 2 2 4 2 2 4;}
@font-face
	{font-family:方正兰亭超细黑简体;
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@方正兰亭超细黑简体";
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:Arvo;
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Droid Serif";
	panose-1:2 2 6 0 6 5 0 2 2 0;}
@font-face
	{font-family:"Indie Flower";
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:Lobster;
	panose-1:2 0 5 6 0 0 0 2 0 3;}
@font-face
	{font-family:"Open Sans";
	panose-1:2 11 6 6 3 5 4 2 2 4;}
@font-face
	{font-family:"Poiret One";
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:Raleway;
	panose-1:2 11 0 3 3 1 1 6 0 3;}
@font-face
	{font-family:Roboto;
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Roboto Condensed";
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Roboto Slab";
	panose-1:0 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Buxton Sketch";
	panose-1:3 8 5 0 0 5 0 0 0 4;}
@font-face
	{font-family:"Segoe Marker";
	panose-1:3 8 6 2 4 3 2 2 2 4;}
@font-face
	{font-family:"SketchFlow Print";
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Agency FB";
	panose-1:2 11 5 3 2 2 2 2 2 4;}
@font-face
	{font-family:"Arial Rounded MT Bold";
	panose-1:2 15 7 4 3 5 4 3 2 4;}
@font-face
	{font-family:"Bodoni MT";
	panose-1:2 7 6 3 8 6 6 2 2 3;}
@font-face
	{font-family:"Bodoni MT Black";
	panose-1:2 7 10 3 8 6 6 2 2 3;}
@font-face
	{font-family:"Bodoni MT Condensed";
	panose-1:2 7 6 6 8 6 6 2 2 3;}
@font-face
	{font-family:"Bradley Hand ITC";
	panose-1:3 7 4 2 5 3 2 3 2 3;}
@font-face
	{font-family:"Bookshelf Symbol 7";
	panose-1:5 1 1 1 1 1 1 1 1 1;}
@font-face
	{font-family:"Calisto MT";
	panose-1:2 4 6 3 5 5 5 3 3 4;}
@font-face
	{font-family:Castellar;
	panose-1:2 10 4 2 6 4 6 1 3 1;}
@font-face
	{font-family:"Century Schoolbook";
	panose-1:2 4 6 4 5 5 5 2 3 4;}
@font-face
	{font-family:"Copperplate Gothic Bold";
	panose-1:2 14 7 5 2 2 6 2 4 4;}
@font-face
	{font-family:"Copperplate Gothic Light";
	panose-1:2 14 5 7 2 2 6 2 4 4;}
@font-face
	{font-family:"Curlz MT";
	panose-1:4 4 4 4 5 7 2 2 2 2;}
@font-face
	{font-family:Elephant;
	panose-1:2 2 9 4 9 5 5 2 3 3;}
@font-face
	{font-family:"Engravers MT";
	panose-1:2 9 7 7 8 5 5 2 3 4;}
@font-face
	{font-family:"Eras Bold ITC";
	panose-1:2 11 9 7 3 5 4 2 2 4;}
@font-face
	{font-family:"Eras Demi ITC";
	panose-1:2 11 8 5 3 5 4 2 8 4;}
@font-face
	{font-family:"Eras Light ITC";
	panose-1:2 11 4 2 3 5 4 2 8 4;}
@font-face
	{font-family:"Eras Medium ITC";
	panose-1:2 11 6 2 3 5 4 2 8 4;}
@font-face
	{font-family:"Felix Titling";
	panose-1:4 6 5 5 6 2 2 2 10 4;}
@font-face
	{font-family:Forte;
	panose-1:3 6 9 2 4 5 2 7 2 3;}
@font-face
	{font-family:"Franklin Gothic Book";
	panose-1:2 11 5 3 2 1 2 2 2 4;}
@font-face
	{font-family:"Franklin Gothic Demi";
	panose-1:2 11 7 3 2 1 2 2 2 4;}
@font-face
	{font-family:"Franklin Gothic Demi Cond";
	panose-1:2 11 7 6 3 4 2 2 2 4;}
@font-face
	{font-family:"Franklin Gothic Heavy";
	panose-1:2 11 9 3 2 1 2 2 2 4;}
@font-face
	{font-family:"Franklin Gothic Medium Cond";
	panose-1:2 11 6 6 3 4 2 2 2 4;}
@font-face
	{font-family:"French Script MT";
	panose-1:3 2 4 2 4 6 7 4 6 5;}
@font-face
	{font-family:Gigi;
	panose-1:4 4 5 4 6 16 7 2 13 2;}
@font-face
	{font-family:"Gill Sans MT";
	panose-1:2 11 5 2 2 1 4 2 2 3;}
@font-face
	{font-family:"Gill Sans MT Condensed";
	panose-1:2 11 5 6 2 1 4 2 2 3;}
@font-face
	{font-family:"Gill Sans Ultra Bold Condensed";
	panose-1:2 11 10 6 2 1 4 2 2 3;}
@font-face
	{font-family:"Gill Sans Ultra Bold";
	panose-1:2 11 10 2 2 1 4 2 2 3;}
@font-face
	{font-family:"Gloucester MT Extra Condensed";
	panose-1:2 3 8 8 2 6 1 1 1 1;}
@font-face
	{font-family:"Gill Sans MT Ext Condensed Bold";
	panose-1:2 11 9 2 2 1 4 2 2 3;}
@font-face
	{font-family:"Goudy Old Style";
	panose-1:2 2 5 2 5 3 5 2 3 3;}
@font-face
	{font-family:"Goudy Stout";
	panose-1:2 2 9 4 7 3 11 2 4 1;}
@font-face
	{font-family:"Imprint MT Shadow";
	panose-1:4 2 6 5 6 3 3 3 2 2;}
@font-face
	{font-family:"Blackadder ITC";
	panose-1:4 2 5 5 5 16 7 2 13 2;}
@font-face
	{font-family:"Edwardian Script ITC";
	panose-1:3 3 3 2 4 7 7 13 8 4;}
@font-face
	{font-family:Leelawadee;
	panose-1:2 11 5 2 4 2 4 2 2 3;}
@font-face
	{font-family:"Lucida Sans";
	panose-1:2 11 6 2 3 5 4 2 2 4;}
@font-face
	{font-family:"Lucida Sans Typewriter";
	panose-1:2 11 5 9 3 5 4 3 2 4;}
@font-face
	{font-family:"Maiandra GD";
	panose-1:2 14 5 2 3 3 8 2 2 4;}
@font-face
	{font-family:"Microsoft Uighur";
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"OCR A Extended";
	panose-1:2 1 5 9 2 1 2 1 3 3;}
@font-face
	{font-family:"MS Outlook";
	panose-1:5 1 1 0 1 0 0 0 0 0;}
@font-face
	{font-family:"Palace Script MT";
	panose-1:3 3 3 2 2 6 7 12 11 5;}
@font-face
	{font-family:Papyrus;
	panose-1:3 7 5 2 6 5 2 3 2 5;}
@font-face
	{font-family:Perpetua;
	panose-1:2 2 5 2 6 4 1 2 3 3;}
@font-face
	{font-family:"Perpetua Titling MT";
	panose-1:2 2 5 2 6 5 5 2 8 4;}
@font-face
	{font-family:Pristina;
	panose-1:3 6 4 2 4 4 6 8 2 4;}
@font-face
	{font-family:"Rage Italic";
	panose-1:3 7 5 2 4 5 7 7 3 4;}
@font-face
	{font-family:"MS Reference Sans Serif";
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"MS Reference Specialty";
	panose-1:5 0 5 0 0 0 0 0 0 0;}
@font-face
	{font-family:"Rockwell Condensed";
	panose-1:2 6 6 3 5 4 5 2 1 4;}
@font-face
	{font-family:Rockwell;
	panose-1:2 6 6 3 2 2 5 2 4 3;}
@font-face
	{font-family:"Rockwell Extra Bold";
	panose-1:2 6 9 3 4 5 5 2 4 3;}
@font-face
	{font-family:"Script MT Bold";
	panose-1:3 4 6 2 4 6 7 8 9 4;}
@font-face
	{font-family:"Tw Cen MT";
	panose-1:2 11 6 2 2 1 4 2 6 3;}
@font-face
	{font-family:"Tw Cen MT Condensed";
	panose-1:2 11 6 6 2 1 4 2 2 3;}
@font-face
	{font-family:"Tw Cen MT Condensed Extra Bold";
	panose-1:2 11 8 3 2 2 2 2 2 4;}
@font-face
	{font-family:"\@Arial Unicode MS";
	panose-1:2 11 6 4 2 2 2 2 2 4;}
@font-face
	{font-family:"Wingdings 2";
	panose-1:5 2 1 2 1 5 7 7 7 7;}
@font-face
	{font-family:"Wingdings 3";
	panose-1:5 4 1 2 1 8 7 7 7 7;}
@font-face
	{font-family:方正粗黑宋简体;
	panose-1:2 0 0 0 0 0 0 0 0 0;}
@font-face
	{font-family:"\@方正粗黑宋简体";}
@font-face
	{font-family:Abadi;}
@font-face
	{font-family:"Abadi Extra Light";}
@font-face
	{font-family:Aharoni;}
@font-face
	{font-family:Aldhabi;}
@font-face
	{font-family:AngsanaUPC;}
@font-face
	{font-family:Aparajita;}
@font-face
	{font-family:"Arabic Typesetting";}
@font-face
	{font-family:"Arial Nova";}
@font-face
	{font-family:"Arial Nova Cond";}
@font-face
	{font-family:"Arial Nova Cond Light";}
@font-face
	{font-family:"Arial Nova Light";}
@font-face
	{font-family:"Avenir Next LT Pro";}
@font-face
	{font-family:"Avenir Next LT Pro Light";}
@font-face
	{font-family:BatangChe;}
@font-face
	{font-family:Bembo;}
@font-face
	{font-family:Biome;}
@font-face
	{font-family:"Biome Light";}
@font-face
	{font-family:"Browallia New";}
@font-face
	{font-family:BrowalliaUPC;}
@font-face
	{font-family:Cavolini;}
@font-face
	{font-family:CordiaUPC;}
@font-face
	{font-family:Dante;}
@font-face
	{font-family:DaunPenh;}
@font-face
	{font-family:David;}
@font-face
	{font-family:Daytona;}
@font-face
	{font-family:"Daytona Pro Condensed";}
@font-face
	{font-family:"Daytona Pro Condensed Light";}
@font-face
	{font-family:"Daytona Pro Light";}
@font-face
	{font-family:DilleniaUPC;}
@font-face
	{font-family:DokChampa;}
@font-face
	{font-family:DotumChe;}
@font-face
	{font-family:Dubai;}
@font-face
	{font-family:"Dubai Light";}
@font-face
	{font-family:"Dubai Medium";}
@font-face
	{font-family:EucrosiaUPC;}
@font-face
	{font-family:Euphemia;}
@font-face
	{font-family:FangSong;}
@font-face
	{font-family:FrankRuehl;}
@font-face
	{font-family:FreesiaUPC;}
@font-face
	{font-family:"Georgia Pro";}
@font-face
	{font-family:"Georgia Pro Black";}
@font-face
	{font-family:"Georgia Pro Cond";}
@font-face
	{font-family:"Georgia Pro Cond Black";}
@font-face
	{font-family:"Georgia Pro Cond Light";}
@font-face
	{font-family:"Georgia Pro Cond Semibold";}
@font-face
	{font-family:"Georgia Pro Light";}
@font-face
	{font-family:"Georgia Pro Semibold";}
@font-face
	{font-family:"Gill Sans Nova";}
@font-face
	{font-family:"Gill Sans Nova Cond";}
@font-face
	{font-family:"Gill Sans Nova Cond Lt";}
@font-face
	{font-family:"Gill Sans Nova Cond Ultra Bold";}
@font-face
	{font-family:"Gill Sans Nova Cond XBd";}
@font-face
	{font-family:"Gill Sans Nova Light";}
@font-face
	{font-family:"Gill Sans Nova Ultra Bold";}
@font-face
	{font-family:Gisha;}
@font-face
	{font-family:Grotesque;}
@font-face
	{font-family:"Grotesque Light";}
@font-face
	{font-family:GulimChe;}
@font-face
	{font-family:Gungsuh;}
@font-face
	{font-family:GungsuhChe;}
@font-face
	{font-family:"Hadassah Friedlaender";}
@font-face
	{font-family:HGGothicE;}
@font-face
	{font-family:HGMaruGothicMPRO;}
@font-face
	{font-family:HGMinchoE;}
@font-face
	{font-family:HGPGothicE;}
@font-face
	{font-family:HGPMinchoE;}
@font-face
	{font-family:HGPSoeiKakugothicUB;}
@font-face
	{font-family:HGSGothicE;}
@font-face
	{font-family:HGSMinchoE;}
@font-face
	{font-family:HGSoeiKakugothicUB;}
@font-face
	{font-family:HGSSoeiKakugothicUB;}
@font-face
	{font-family:"Ink Free";}
@font-face
	{font-family:IrisUPC;}
@font-face
	{font-family:"Iskoola Pota";}
@font-face
	{font-family:JasmineUPC;}
@font-face
	{font-family:KaiTi;}
@font-face
	{font-family:Kalinga;}
@font-face
	{font-family:Kartika;}
@font-face
	{font-family:"Khmer UI";}
@font-face
	{font-family:KodchiangUPC;}
@font-face
	{font-family:Kokila;}
@font-face
	{font-family:"Lao UI";}
@font-face
	{font-family:"Levenim MT";}
@font-face
	{font-family:LilyUPC;}
@font-face
	{font-family:Meiryo;
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Meiryo UI";
	panose-1:2 11 6 4 3 5 4 4 2 4;}
@font-face
	{font-family:"Microsoft GothicNeo";}
@font-face
	{font-family:"Microsoft GothicNeo Light";}
@font-face
	{font-family:"Microsoft YaHei Light";}
@font-face
	{font-family:MingLiU_HKSCS;}
@font-face
	{font-family:Miriam;}
@font-face
	{font-family:"Miriam Fixed";}
@font-face
	{font-family:"Modern Love";}
@font-face
	{font-family:"Modern Love Caps";}
@font-face
	{font-family:"Modern Love Grunge";}
@font-face
	{font-family:MoolBoran;}
@font-face
	{font-family:"MS PMincho";}
@font-face
	{font-family:Narkisim;}
@font-face
	{font-family:"Neue Haas Grotesk Text Pro";}
@font-face
	{font-family:"News Gothic MT";}
@font-face
	{font-family:Nyala;}
@font-face
	{font-family:OCRB;}
@font-face
	{font-family:"Plantagenet Cherokee";}
@font-face
	{font-family:Posterama;}
@font-face
	{font-family:"Quire Sans";}
@font-face
	{font-family:"Quire Sans Pro Light";}
@font-face
	{font-family:"Rockwell Light";}
@font-face
	{font-family:"Rockwell Nova";}
@font-face
	{font-family:"Rockwell Nova Cond";}
@font-face
	{font-family:"Rockwell Nova Cond Light";}
@font-face
	{font-family:"Rockwell Nova Extra Bold";}
@font-face
	{font-family:"Rockwell Nova Light";}
@font-face
	{font-family:Rod;}
@font-face
	{font-family:"Sabon Next LT";}
@font-face
	{font-family:"Sagona Book";}
@font-face
	{font-family:"Sagona ExtraLight";}
@font-face
	{font-family:"Sakkal Majalla";}
@font-face
	{font-family:"Sanskrit Text";}
@font-face
	{font-family:Selawik;}
@font-face
	{font-family:"Selawik Light";}
@font-face
	{font-family:"Selawik Semibold";}
@font-face
	{font-family:"Shonar Bangla";}
@font-face
	{font-family:"Simplified Arabic";}
@font-face
	{font-family:"Simplified Arabic Fixed";}
@font-face
	{font-family:"Source Sans Pro";}
@font-face
	{font-family:"Source Sans Pro Black";}
@font-face
	{font-family:"Source Sans Pro ExtraLight";}
@font-face
	{font-family:"Source Sans Pro Light";}
@font-face
	{font-family:"Source Sans Pro SemiBold";}
@font-face
	{font-family:"Speak Pro";}
@font-face
	{font-family:"Speak Pro Light";}
@font-face
	{font-family:"TH SarabunPSK";}
@font-face
	{font-family:"The Hand";}
@font-face
	{font-family:"The Hand Black";}
@font-face
	{font-family:"The Hand Extrablack";}
@font-face
	{font-family:"The Hand Light";}
@font-face
	{font-family:"The Serif Hand";}
@font-face
	{font-family:"The Serif Hand Black";}
@font-face
	{font-family:"The Serif Hand Extrablack";}
@font-face
	{font-family:"The Serif Hand Light";}
@font-face
	{font-family:"Tisa Offc Serif Pro";}
@font-face
	{font-family:"Tisa Offc Serif Pro Thin";}
@font-face
	{font-family:"Traditional Arabic";}
@font-face
	{font-family:"UD Digi Kyokasho N-B";}
@font-face
	{font-family:"UD Digi Kyokasho N-R";}
@font-face
	{font-family:"UD Digi Kyokasho NK-B";}
@font-face
	{font-family:"UD Digi Kyokasho NK-R";}
@font-face
	{font-family:"UD Digi Kyokasho NP-B";}
@font-face
	{font-family:"UD Digi Kyokasho NP-R";}
@font-face
	{font-family:Univers;}
@font-face
	{font-family:"Univers Condensed";}
@font-face
	{font-family:"Univers Condensed Light";}
@font-face
	{font-family:"Univers Light";}
@font-face
	{font-family:"Urdu Typesetting";}
@font-face
	{font-family:Utsaah;}
@font-face
	{font-family:Vani;}
@font-face
	{font-family:"Verdana Pro";}
@font-face
	{font-family:"Verdana Pro Black";}
@font-face
	{font-family:"Verdana Pro Cond";}
@font-face
	{font-family:"Verdana Pro Cond Black";}
@font-face
	{font-family:"Verdana Pro Cond Light";}
@font-face
	{font-family:"Verdana Pro Cond SemiBold";}
@font-face
	{font-family:"Verdana Pro Light";}
@font-face
	{font-family:"Verdana Pro SemiBold";}
@font-face
	{font-family:Vijaya;}
@font-face
	{font-family:"Walbaum Display";}
@font-face
	{font-family:"Walbaum Display Heavy";}
@font-face
	{font-family:"Walbaum Display Light";}
@font-face
	{font-family:"Walbaum Display SemiBold";}
@font-face
	{font-family:"Walbaum Heading";}
@font-face
	{font-family:"Walbaum Text";}
@font-face
	{font-family:"Yu Mincho";}
@font-face
	{font-family:"Yu Mincho Demibold";}
@font-face
	{font-family:"Yu Mincho Light";}
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
h1
	{mso-style-link:"标题 1 字符";
	margin-right:0cm;
	margin-left:0cm;
	font-size:24.0pt;
	font-family:宋体;
	font-weight:bold;}
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
	font-family:"Cambria",serif;
	font-weight:bold;}
h3
	{mso-style-link:"标题 3 字符";
	margin-top:13.0pt;
	margin-right:0cm;
	margin-bottom:13.0pt;
	margin-left:0cm;
	text-align:justify;
	text-justify:inter-ideograph;
	line-height:173%;
	page-break-after:avoid;
	font-size:16.0pt;
	font-family:"Calibri",sans-serif;
	font-weight:bold;}
h4
	{mso-style-link:"标题 4 字符";
	margin-top:14.0pt;
	margin-right:0cm;
	margin-bottom:14.5pt;
	margin-left:0cm;
	text-align:justify;
	text-justify:inter-ideograph;
	line-height:156%;
	page-break-after:avoid;
	font-size:14.0pt;
	font-family:"Cambria",serif;
	font-weight:bold;}
h5
	{mso-style-link:"标题 5 字符";
	margin-top:14.0pt;
	margin-right:0cm;
	margin-bottom:14.5pt;
	margin-left:0cm;
	text-align:justify;
	text-justify:inter-ideograph;
	line-height:156%;
	page-break-after:avoid;
	font-size:14.0pt;
	font-family:"Calibri",sans-serif;
	font-weight:bold;}
h6
	{mso-style-link:"标题 6 字符";
	margin-top:12.0pt;
	margin-right:0cm;
	margin-bottom:3.2pt;
	margin-left:0cm;
	text-align:justify;
	text-justify:inter-ideograph;
	line-height:133%;
	page-break-after:avoid;
	font-size:12.0pt;
	font-family:"Cambria",serif;
	font-weight:bold;}
p.MsoToc1, li.MsoToc1, div.MsoToc1
	{margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc2, li.MsoToc2, div.MsoToc2
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:21.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc3, li.MsoToc3, div.MsoToc3
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:42.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc4, li.MsoToc4, div.MsoToc4
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:63.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc5, li.MsoToc5, div.MsoToc5
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:84.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc6, li.MsoToc6, div.MsoToc6
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:105.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc7, li.MsoToc7, div.MsoToc7
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:126.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc8, li.MsoToc8, div.MsoToc8
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:147.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoToc9, li.MsoToc9, div.MsoToc9
	{margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:168.0pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoHeader, li.MsoHeader, div.MsoHeader
	{mso-style-link:"页眉 字符";
	margin:0cm;
	margin-bottom:.0001pt;
	text-align:center;
	layout-grid-mode:char;
	border:none;
	padding:0cm;
	font-size:9.0pt;
	font-family:"Calibri",sans-serif;}
p.MsoFooter, li.MsoFooter, div.MsoFooter
	{mso-style-link:"页脚 字符";
	margin:0cm;
	margin-bottom:.0001pt;
	layout-grid-mode:char;
	font-size:9.0pt;
	font-family:"Calibri",sans-serif;}
a:link, span.MsoHyperlink
	{color:blue;
	text-decoration:underline;}
a:visited, span.MsoHyperlinkFollowed
	{color:purple;
	text-decoration:underline;}
p
	{margin-right:0cm;
	margin-left:0cm;
	font-size:12.0pt;
	font-family:宋体;}
code
	{font-family:宋体;}
pre
	{mso-style-link:"HTML 预设格式 字符";
	margin:0cm;
	margin-bottom:.0001pt;
	font-size:12.0pt;
	font-family:宋体;}
p.MsoAcetate, li.MsoAcetate, div.MsoAcetate
	{mso-style-link:"批注框文本 字符";
	margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:9.0pt;
	font-family:"Calibri",sans-serif;}
p.MsoNoSpacing, li.MsoNoSpacing, div.MsoNoSpacing
	{mso-style-link:"无间隔 字符";
	margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoListParagraph, li.MsoListParagraph, div.MsoListParagraph
	{margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	text-indent:21.0pt;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
p.MsoTocHeading, li.MsoTocHeading, div.MsoTocHeading
	{margin-top:24.0pt;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:0cm;
	margin-bottom:.0001pt;
	line-height:115%;
	page-break-after:avoid;
	font-size:14.0pt;
	font-family:"Cambria",serif;
	color:#365F91;
	font-weight:bold;}
span.a
	{mso-style-name:"页眉 字符";
	mso-style-link:页眉;}
span.a0
	{mso-style-name:"页脚 字符";
	mso-style-link:页脚;}
span.HTML
	{mso-style-name:"HTML 预设格式 字符";
	mso-style-link:"HTML 预设格式";
	font-family:宋体;}
span.1
	{mso-style-name:"标题 1 字符";
	mso-style-link:"标题 1";
	font-family:宋体;
	font-weight:bold;}
span.2
	{mso-style-name:"标题 2 字符";
	mso-style-link:"标题 2";
	font-family:"Cambria",serif;
	font-weight:bold;}
span.3
	{mso-style-name:"标题 3 字符";
	mso-style-link:"标题 3";
	font-weight:bold;}
span.a1
	{mso-style-name:"批注框文本 字符";
	mso-style-link:批注框文本;}
span.4
	{mso-style-name:"标题 4 字符";
	mso-style-link:"标题 4";
	font-family:"Cambria",serif;
	font-weight:bold;}
span.5
	{mso-style-name:"标题 5 字符";
	mso-style-link:"标题 5";
	font-weight:bold;}
span.pl-k
	{mso-style-name:pl-k;}
span.6
	{mso-style-name:"标题 6 字符";
	mso-style-link:"标题 6";
	font-family:"Cambria",serif;
	font-weight:bold;}
span.pl-c
	{mso-style-name:pl-c;}
span.pl-s
	{mso-style-name:pl-s;}
span.pl-pds
	{mso-style-name:pl-pds;}
span.pl-c1
	{mso-style-name:pl-c1;}
span.pl-en
	{mso-style-name:pl-en;}
span.pl-ent
	{mso-style-name:pl-ent;}
span.pl-e
	{mso-style-name:pl-e;}
span.apple-converted-space
	{mso-style-name:apple-converted-space;}
span.a2
	{mso-style-name:"无间隔 字符";
	mso-style-link:无间隔;}
p.xl34, li.xl34, div.xl34
	{mso-style-name:xl34;
	margin-top:0cm;
	margin-right:0cm;
	margin-bottom:0cm;
	margin-left:41.15pt;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	text-indent:-35.45pt;
	font-size:10.5pt;
	font-family:"Calibri",sans-serif;}
span.msoIns
	{mso-style-name:"";
	text-decoration:underline;
	color:teal;}
span.msoDel
	{mso-style-name:"";
	text-decoration:line-through;
	color:red;}
.MsoChpDefault
	{font-family:"Calibri",sans-serif;}
 /* Page Definitions */
 @page WordSection1
	{size:595.3pt 841.9pt;
	margin:72.0pt 90.0pt 72.0pt 90.0pt;
	border:solid windowtext 1.0pt;
	padding:24.0pt 24.0pt 24.0pt 24.0pt;
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

<body lang=ZH-CN link=blue vlink=purple style='text-justify-trim:punctuation'>

<div class=WordSection1 style='layout-grid:15.6pt'>

<h1><a name="_Toc462219403"></a><a name="_Toc26097915">开源直播服务srs详细介绍(wiki整理)</a></h1>

<p class=MsoTocHeading><span style='font-family:宋体'>目录</span></p>

<p class=MsoToc1><a href="#_Toc26097915"><span style='font-family:宋体'>开源直播服务</span>srs<span
style='font-family:宋体'>详细介绍</span>(wiki<span style='font-family:宋体'>整理</span>)<span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>0</span></a></p>

<p class=MsoToc1><a href="#_Toc26097916"><span lang=EN-US>1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>简介</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>2</span></a></p>

<p class=MsoToc2><a href="#_Toc26097917"><span lang=EN-US>1.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>功能</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>2</span></a></p>

<p class=MsoToc2><a href="#_Toc26097918"><span lang=EN-US>1.2.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>架构</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>2</span></a></p>

<p class=MsoToc1><a href="#_Toc26097919"><span lang=EN-US>2.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>流接入方式</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>3</span></a></p>

<p class=MsoToc2><a href="#_Toc26097920"><span lang=EN-US>2.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>推送</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>到</span><span lang=EN-US>SRS</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>4</span></a></p>

<p class=MsoToc2><a href="#_Toc26097921"><span lang=EN-US>2.2.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>分发</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>流</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>4</span></a></p>

<p class=MsoToc3><a href="#_Toc26097922"><span lang=EN-US>2.2.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>应用场景</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>4</span></a></p>

<p class=MsoToc3><a href="#_Toc26097923"><span lang=EN-US style='font-family:
宋体'>2.2.2.</span><span lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US style='font-family:宋体'>WIKI</span><span lang=EN-US style='color:
windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>5</span></a></p>

<p class=MsoToc3><a href="#_Toc26097924"><span lang=EN-US>2.2.3.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>补充</span><span lang=EN-US>:SRS</span><span
style='font-family:宋体'>不支持点播</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>5</span></a></p>

<p class=MsoToc3><a href="#_Toc26097925"><span lang=EN-US>2.2.4.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>补充</span><span lang=EN-US>:</span><span
style='font-family:宋体'>常用的第三方的推流与播放工具</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>6</span></a></p>

<p class=MsoToc2><a href="#_Toc26097926"><span lang=EN-US>2.3.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>推送</span><span lang=EN-US>RTSP/UDP/FLV </span><span
style='font-family:宋体'>到</span><span lang=EN-US>SRS</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>6</span></a></p>

<p class=MsoToc3><a href="#_Toc26097927"><span lang=EN-US>2.3.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>Push MPEG-TS over UDP</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>7</span></a></p>

<p class=MsoToc3><a href="#_Toc26097928"><span lang=EN-US>2.3.2.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>Push RTSP to SRS</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>7</span></a></p>

<p class=MsoToc3><a href="#_Toc26097929"><span lang=EN-US>2.3.3.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>Push HTTP FLV to SRS</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>8</span></a></p>

<p class=MsoToc3><a href="#_Toc26097930"><span lang=EN-US>2.3.4.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>WIKI</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>8</span></a></p>

<p class=MsoToc2><a href="#_Toc26097931"><span lang=EN-US>2.4.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>拉取流到</span><span lang=EN-US>SRS</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>9</span></a></p>

<p class=MsoToc3><a href="#_Toc26097932"><span lang=EN-US>2.4.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>补充</span><span lang=EN-US>:RTSP</span><span
style='font-family:宋体'>开源项目</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>10</span></a></p>

<p class=MsoToc3><a href="#_Toc26097933"><span lang=EN-US>2.4.2.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>WIKI</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>11</span></a></p>

<p class=MsoToc2><a href="#_Toc26097934"><span lang=EN-US>2.5.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>RTMP</span><span style='font-family:宋体'>流的低延时配置</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>11</span></a></p>

<p class=MsoToc3><a href="#_Toc26097935"><span lang=EN-US>2.5.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>低延时直播应用</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>11</span></a></p>

<p class=MsoToc3><a href="#_Toc26097936"><span lang=EN-US>2.5.2.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>应用场景</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>11</span></a></p>

<p class=MsoToc3><a href="#_Toc26097937"><span lang=EN-US>2.5.3.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>RTMP</span><span style='font-family:宋体'>和延时</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>12</span></a></p>

<p class=MsoToc3><a href="#_Toc26097938"><span lang=EN-US>2.5.4.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>累积延迟</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>13</span></a></p>

<p class=MsoToc3><a href="#_Toc26097939"><span lang=EN-US>2.5.5.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>低延时配置</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>14</span></a></p>

<p class=MsoToc3><a href="#_Toc26097940"><span lang=EN-US>2.5.6.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>WIKI</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>15</span></a></p>

<p class=MsoToc1><a href="#_Toc26097941"><span lang=EN-US>3.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>流变换</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>15</span></a></p>

<p class=MsoToc2><a href="#_Toc26097942"><span lang=EN-US>3.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>将</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>流转码</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>15</span></a></p>

<p class=MsoToc3><a href="#_Toc26097943"><span lang=EN-US>3.1.1.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>应用场景</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>15</span></a></p>

<p class=MsoToc3><a href="#_Toc26097944"><span lang=EN-US>3.1.2.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>工作流程</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>16</span></a></p>

<p class=MsoToc3><a href="#_Toc26097945"><span lang=EN-US>3.1.3.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>配置</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>17</span></a></p>

<p class=MsoToc3><a href="#_Toc26097946"><span lang=EN-US>3.1.4.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>转码规则</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>17</span></a></p>

<p class=MsoToc3><a href="#_Toc26097947"><span lang=EN-US>3.1.5.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>Transcode on ARM cpu</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>19</span></a></p>

<p class=MsoToc3><a href="#_Toc26097948"><span lang=EN-US>3.1.6.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>FFMPEG Transcode the Stream by Flash encoder</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>20</span></a></p>

<p class=MsoToc3><a href="#_Toc26097949"><span lang=EN-US>3.1.7.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>补充</span><span lang=EN-US>:</span><span
style='font-family:宋体'>测试效果图</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>20</span></a></p>

<p class=MsoToc3><a href="#_Toc26097950"><span lang=EN-US>3.1.8.</span><span
lang=EN-US style='color:windowtext;text-decoration:none'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
lang=EN-US>WIKI</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>20</span></a></p>

<p class=MsoToc2><a href="#_Toc26097951"><span style='font-family:宋体'>流截图</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>20</span></a></p>

<p class=MsoToc3><a href="#_Toc26097952"><span lang=EN-US>WIKI</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>21</span></a></p>

<p class=MsoToc3><a href="#_Toc26097953"><span style='font-family:宋体'>补充</span><span
lang=EN-US>:</span><span style='font-family:宋体'>测试效果图</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>21</span></a></p>

<p class=MsoToc3><a href="#_Toc26097954"><span style='font-family:宋体'>转发给其他服务器</span><span
lang=EN-US>(Forward)</span><span lang=EN-US style='color:windowtext;display:
none;text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>21</span></a></p>

<p class=MsoToc3><a href="#_Toc26097955"><span style='font-family:宋体'>转封装成</span><span
lang=EN-US>HTTP</span><span style='font-family:宋体'>直播流</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>22</span></a></p>

<p class=MsoToc3><a href="#_Toc26097956"><span style='font-family:宋体'>转封装成</span><span
lang=EN-US>HLS</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>25</span></a></p>

<p class=MsoToc3><a href="#_Toc26097957"><span style='font-family:宋体'>转封装成</span><span
lang=EN-US>HDS</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>28</span></a></p>

<p class=MsoToc3><a href="#_Toc26097958"><span style='font-family:宋体'>录制成</span><span
lang=EN-US>FLV</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>28</span></a></p>

<p class=MsoToc3><a href="#_Toc26097959"><span style='font-family:宋体'>分发方式比较</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>29</span></a></p>

<p class=MsoToc2><a href="#_Toc26097960"><span style='font-family:宋体'>集群与</span><span
lang=EN-US>CDN</span><span style='font-family:宋体'>相关功能</span><span lang=EN-US
style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>32</span></a></p>

<p class=MsoToc3><a href="#_Toc26097961"><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>多级集群</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>32</span></a></p>

<p class=MsoToc3><a href="#_Toc26097962"><span lang=EN-US>VHOST</span><span
style='font-family:宋体'>虚拟服务器</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>37</span></a></p>

<p class=MsoToc3><a href="#_Toc26097963"><span style='font-family:宋体'>无中断服务</span><span
lang=EN-US>Reload</span><span lang=EN-US style='color:windowtext;display:none;
text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>46</span></a></p>

<p class=MsoToc3><a href="#_Toc26097964"><span lang=EN-US>HTTP-FLV</span><span
style='font-family:宋体'>集群</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>47</span></a></p>

<p class=MsoToc3><a href="#_Toc26097965"><span lang=EN-US>Kafka</span><span
style='font-family:宋体'>对接</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>48</span></a></p>

<p class=MsoToc2><a href="#_Toc26097966"><span style='font-family:宋体'>应用接口</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>48</span></a></p>

<p class=MsoToc3><a href="#_Toc26097967"><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>回调</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>48</span></a></p>

<p class=MsoToc3><a href="#_Toc26097968"><span style='font-family:宋体'>安全策略</span><span
lang=EN-US>Security</span><span lang=EN-US style='color:windowtext;display:
none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>54</span></a></p>

<p class=MsoToc3><a href="#_Toc26097969"><span lang=EN-US>HTTP API</span><span
style='font-family:宋体'>接口</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>57</span></a></p>

<p class=MsoToc3><a href="#_Toc26097970"><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>测速</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>71</span></a></p>

<p class=MsoToc2><a href="#_Toc26097971"><span style='font-family:宋体'>其他功能</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>74</span></a></p>

<p class=MsoToc3><a href="#_Toc26097972"><span lang=EN-US>Send Minimal Interval</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'> </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>74</span></a></p>

<p class=MsoToc3><a href="#_Toc26097973"><span lang=EN-US>Reduce Sequence
Header</span><span lang=EN-US style='color:windowtext;display:none;text-decoration:
none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>75</span></a></p>

<p class=MsoToc3><a href="#_Toc26097974"><span lang=EN-US>Publish 1st Packet
Timeout</span><span lang=EN-US style='color:windowtext;display:none;text-decoration:
none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>75</span></a></p>

<p class=MsoToc3><a href="#_Toc26097975"><span lang=EN-US>Publish Normal
Timeout</span><span lang=EN-US style='color:windowtext;display:none;text-decoration:
none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>75</span></a></p>

<p class=MsoToc3><a href="#_Toc26097976"><span lang=EN-US>Debug SRS Upnode</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>75</span></a></p>

<p class=MsoToc3><a href="#_Toc26097977"><span lang=EN-US>UTC Time</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>76</span></a></p>

<p class=MsoToc3><a href="#_Toc26097978"><span lang=EN-US>HLS TS Floor</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>76</span></a></p>

<p class=MsoToc3><a href="#_Toc26097979"><span lang=EN-US>HLS Wait Keyframe</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>76</span></a></p>

<p class=MsoToc3><a href="#_Toc26097980"><span lang=EN-US>HttpHooks On HLS
Notify</span><span lang=EN-US style='color:windowtext;display:none;text-decoration:
none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>76</span></a></p>

<p class=MsoToc3><a href="#_Toc26097981"><span lang=EN-US>TCP NoDelay</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>77</span></a></p>

<p class=MsoToc3><a href="#_Toc26097982"><span lang=EN-US>ATC Auto</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>77</span></a></p>

<p class=MsoToc3><a href="#_Toc26097983"><span lang=EN-US>NGINX RTMP EXEC</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>77</span></a></p>

<p class=MsoToc2><a href="#_Toc26097984"><span lang=EN-US>SRS</span><span
style='font-family:宋体'>与其他流媒体比较</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>78</span></a></p>

<p class=MsoToc3><a href="#_Toc26097985"><span style='font-family:宋体'>流发分</span><span
lang=EN-US> Stream Delivery</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>78</span></a></p>

<p class=MsoToc3><a href="#_Toc26097986"><span style='font-family:宋体'>集群</span><span
lang=EN-US> Cluster</span><span lang=EN-US style='color:windowtext;display:
none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>79</span></a></p>

<p class=MsoToc3><a href="#_Toc26097987"><span style='font-family:宋体'>流处理服务</span><span
lang=EN-US> Stream Service</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>79</span></a></p>

<p class=MsoToc3><a href="#_Toc26097988"><span lang=EN-US>Efficiency</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>79</span></a></p>

<p class=MsoToc3><a href="#_Toc26097989"><span lang=EN-US>Stream Caster</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>79</span></a></p>

<p class=MsoToc3><a href="#_Toc26097990"><span lang=EN-US>Debug System</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>.. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>80</span></a></p>

<p class=MsoToc3><a href="#_Toc26097991"><span lang=EN-US>Docs</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>80</span></a></p>

<p class=MsoToc3><a href="#_Toc26097992"><span lang=EN-US>Others</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>. </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>80</span></a></p>

<p class=MsoToc3><a href="#_Toc26097993"><span style='font-family:宋体;
background:white'>市面主要的流媒体服务器对比</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>80</span></a></p>

<p class=MsoToc3><a href="#_Toc26097994"><span lang=EN-US>SRS</span><span
style='font-family:宋体'>商业版（</span><span lang=EN-US>BMS</span><span
style='font-family:宋体'>）简介</span><span lang=EN-US style='color:windowtext;
display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>93</span></a></p>

<p class=MsoToc1><a href="#_Toc26097995"><span style='font-family:宋体'>常用的直播平台网站</span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>... </span><span
lang=EN-US style='color:windowtext;display:none;text-decoration:none'>96</span></a></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h1 style='margin-left:21.25pt;text-indent:-21.25pt'><a name="_Toc26097916"><span
lang=EN-US>1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp; </span></span>简介</a></h1>

<p class=MsoNormal style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>该文档介绍了开源直播服务器<span lang=EN-US>SRS</span>架构、功能以及应用、<span
lang=EN-US>SRS</span>与其他直播服务器的比较、<span lang=EN-US>SRS</span>商业版的功能简介。内容主要来自于<span
lang=EN-US>SRS WIKI</span>整理，以及网上有关博客内容<span lang=EN-US>,</span>有些地方加了补充内容。出掉<span
lang=EN-US>WIKI</span>上一些讲解配置使用的内容，需要了解这些内容可点击文档中相关<span lang=EN-US>wiki</span>链接。</span></p>

<p class=MsoNormal style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>整理这些内容的目的是为了方便查阅，阅读后能对<span lang=EN-US>SRS</span>比较全面的了解，特别是对刚接解<span
lang=EN-US>SRS</span>的使用者。</span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097917"><span
lang=EN-US>1.1.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
lang=EN-US>SRS</span></a><span style='font-family:宋体'>功能</span></h2>

<p class=MsoNormal style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt;font-family:宋体'>SRS</span><span style='font-size:14.0pt;
font-family:宋体'>提供了丰富的接入方案将<span lang=EN-US>RTMP</span>流接入<span lang=EN-US>SRS</span>，包括推送<span
lang=EN-US>RTMP</span>到<span lang=EN-US>SRS</span>、推送<span lang=EN-US>RTSP/UDP/FLV</span>到<span
lang=EN-US>SRS</span>、拉取流到<span lang=EN-US>SRS</span>。<span lang=EN-US>SRS</span>还支持将接入的<span
lang=EN-US>RTMP</span>流进行各种变换，譬如将<span lang=EN-US>RTMP</span>流转码、流截图、转发给其他服务器、转封装成<span
lang=EN-US>HTTP-FLV</span>流、转封装成<span lang=EN-US>HLS</span>、转封装成<span
lang=EN-US>HDS</span>、录制成<span lang=EN-US>FLV</span>。<span lang=EN-US>SRS</span>包含支大规模集群如<span
lang=EN-US>CDN</span>业务的关键特性，譬如<span lang=EN-US>RTMP</span>多级集群、<span
lang=EN-US>VHOST</span>虚拟服务器、无中断服务<span lang=EN-US>Reload</span>、<span
lang=EN-US>HTTP-FLV</span>集群、<span lang=EN-US>Kafka</span>对接。此外，<span
lang=EN-US>SRS</span>还提供丰富的应用接口，包括<span lang=EN-US>HTTP</span>回调、安全策略<span
lang=EN-US>Security</span>、<span lang=EN-US>HTTP API</span>接口、<span lang=EN-US>RTMP</span>测速。</span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097918"></a><a
name="_Toc462219404"><span lang=EN-US>1.2.<span style='font:7.0pt "Times New Roman"'>&nbsp;
</span></span><span style='font-family:宋体'>架构</span></a></h2>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
+---------+&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
+----------+</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
| Publish
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp; Deliver |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
+---|-----+&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
+----|-----+</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>+----------------------+-------------------------+----------------+</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;&nbsp;&nbsp;
Input&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |
SRS(Simple RTMP Server) |&nbsp;&nbsp;&nbsp;&nbsp;
Output&nbsp;&nbsp;&nbsp;&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>+----------------------+-------------------------+----------------+</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;&nbsp;
Encoder(1)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |&nbsp;&nbsp; +-&gt;
RTMP/HDS&nbsp; --------+-&gt; Flash player |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp; (FMLE,FFMPEG,
-rtmp-+-&gt;-+-&gt; HLS/HTTP ---------+-&gt; M3u8 player&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;
Flash,XSPLIT,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |&nbsp;&nbsp; +-&gt;
FLV/MP3/Aac/Ts ---+-&gt; HTTP player&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;
......)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp; +-&gt; Fowarder ---------+-&gt; RTMP server&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp; +-&gt; Transcoder -------+-&gt; RTMP server&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp; +-&gt; DVR --------------+-&gt; Flv file&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp; +-&gt; BandwidthTest ----+-&gt;
flash&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>+----------------------+&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;
MediaSource(2)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;
(RTSP,FILE,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp; HTTP,HLS,&nbsp;&nbsp;
--pull-+-&gt;-- Ingester(3) -(rtmp)-+-&gt;
SRS&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp; Device,&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;
......)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>+----------------------+&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;
MediaSource(2)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;
(RTSP,FILE,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp; HTTP,HLS,&nbsp;&nbsp;
--push-+-&gt;-- Streamer(4) -(rtmp)-+-&gt;
SRS&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; |</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;
Device,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>|&nbsp;&nbsp;
......)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-size:12.0pt;font-family:宋体'>+----------------------+-------------------------+----------------+</span></p>

<h1 style='margin-left:21.25pt;text-indent:-21.25pt'><a name="_Toc26097919"></a><a
name="_Toc462219405"></a><a name="_Toc456260508"><span lang=EN-US>2.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp; </span></span>流接入方式</a></h1>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>可以通过以下几种方式将音视频流接入到</span><span lang=EN-US style='font-size:
14.0pt'>SRS: </span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>1.</span><span style='font-size:14.0pt;font-family:
宋体'>客户端使用编码器将音视频编码成</span><span lang=EN-US style='font-size:14.0pt'>h264 ,aac,mp3</span><span
style='font-size:14.0pt;font-family:宋体'>使用</span><span lang=EN-US
style='font-size:14.0pt'>rtmp</span><span style='font-size:14.0pt;font-family:
宋体'>协议推送到</span><span lang=EN-US style='font-size:14.0pt'>SRS;</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>2.</span><span style='font-size:14.0pt;font-family:
宋体'>使用</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>采取器</span><span lang=EN-US
style='font-size:14.0pt'>(</span><span lang=EN-US style='font-size:14.0pt;
font-family:宋体'>Ingester</span><span lang=EN-US style='font-size:14.0pt'>),</span><span
style='font-size:14.0pt;font-family:宋体'>将各种源</span><span lang=EN-US
style='font-size:14.0pt'>(</span><span style='font-size:14.0pt;font-family:
宋体'>流，文件，设备等</span><span lang=EN-US style='font-size:14.0pt'>)</span><span
style='font-size:14.0pt;font-family:宋体'>拉过来后，推送给自己</span><span lang=EN-US
style='font-size:14.0pt'>;</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>3.SRS</span><span style='font-size:14.0pt;font-family:
宋体'>作为服务器侦听并接收其他协议的流（譬如</span><span lang=EN-US style='font-size:14.0pt'>RTSP</span><span
style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
style='font-size:14.0pt'>MPEG-TS over UDP</span><span style='font-size:14.0pt;
font-family:宋体'>等等），将协议的流转换成</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt;font-family:宋体'>推送给自己</span><span lang=EN-US
style='font-size:14.0pt'>;</span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097920"></a><a
name="_Toc462219406"></a><a name="_Toc456260509"><span lang=EN-US>2.1.<span
style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
style='font-family:宋体'>推送</span><span lang=EN-US>RTMP</span></a><span
style='font-family:宋体'>到</span><span lang=EN-US>SRS</span></h2>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>这是</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>的核心功能之一，通过客户端使用</span><span lang=EN-US
style='font-size:14.0pt'>rtmp</span><span style='font-size:14.0pt;font-family:
宋体'>协议将音视频流推送</span><span lang=EN-US style='font-size:14.0pt'>srs</span><span
style='font-size:14.0pt;font-family:宋体'>。然后使用</span><span lang=EN-US
style='font-size:14.0pt'>rtmp</span><span style='font-size:14.0pt;font-family:
宋体'>播放器连接</span><span lang=EN-US style='font-size:14.0pt'>srs</span><span
style='font-size:14.0pt;font-family:宋体'>后观看，</span><span style='font-size:14.0pt'>
<span lang=EN-US>Srs</span></span><span style='font-size:14.0pt;font-family:
宋体'>目前支持视频</span><span lang=EN-US style='font-size:14.0pt'>H264, </span><span
style='font-size:14.0pt;font-family:宋体'>音频</span><span lang=EN-US
style='font-size:14.0pt'>AAC</span><span style='font-size:14.0pt;font-family:
宋体'>、</span><span lang=EN-US style='font-size:14.0pt'>MP3</span><span
style='font-size:14.0pt;font-family:宋体'>。</span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097921"></a><a
name="_Toc462219407"><span lang=EN-US>2.2.<span style='font:7.0pt "Times New Roman"'>&nbsp;
</span></span><span style='font-family:宋体'>分发</span><span lang=EN-US>RTMP</span></a><span
style='font-family:宋体'>流</span></h2>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt'>（<span lang=EN-US>Simple RTMP Server</span>）分发<span
lang=EN-US>RTMP</span>也是核心功能之一，<span lang=EN-US>srs</span>的主要定位就是分发<span
lang=EN-US>RTMP</span>低延时流媒体，同时支持分发<span lang=EN-US>HLS</span>流。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097922"></a><a
name="_Toc462219408"><span lang=EN-US>2.2.1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>应用场景</span></a></h3>

<p><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
14.0pt'>是<span lang=EN-US>PC-flash</span>支持最完善的流分发方式，主要的应用场景包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>无插件流媒体应用：十年前各种浏览器插件大行其道，最后</span><span lang=EN-US
     style='font-size:14.0pt'>adobe</span><span style='font-size:14.0pt;
     font-family:宋体'>的</span><span lang=EN-US style='font-size:14.0pt'>flash</span><span
     style='font-size:14.0pt;font-family:宋体'>一统天下，现在如何观看视频还需要用户装插件，已经是非常罕见的事情。打开浏览器就能用，不用装插件，这是</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>的最基本的应用方式。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>适配广泛的播放器：如果没有专业的</span><span lang=EN-US style='font-size:
     14.0pt'>flash</span><span style='font-size:14.0pt;font-family:宋体'>开发人员，那么</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>会是个很好的选择，只要</span><span lang=EN-US
     style='font-size:14.0pt'>3</span><span style='font-size:14.0pt;font-family:
     宋体'>行代码就能完成一个播放器，和</span><span lang=EN-US style='font-size:14.0pt'>html5</span><span
     style='font-size:14.0pt;font-family:宋体'>的</span><span lang=EN-US
     style='font-size:14.0pt'>video</span><span style='font-size:14.0pt;
     font-family:宋体'>标签一样方便。</span><span lang=EN-US style='font-size:14.0pt'>HDS/HLS</span><span
     style='font-size:14.0pt;font-family:宋体'>在</span><span lang=EN-US
     style='font-size:14.0pt'>PC</span><span style='font-size:14.0pt;
     font-family:宋体'>上，都需要库支持，</span><span lang=EN-US style='font-size:14.0pt'>N</span><span
     style='font-size:14.0pt;font-family:宋体'>行代码很麻烦。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>苛刻的稳定性支持：</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>服务器能</span><span lang=EN-US
     style='font-size:14.0pt'>365x24</span><span style='font-size:14.0pt;
     font-family:宋体'>提供服务，当然</span><span lang=EN-US style='font-size:14.0pt'>http</span><span
     style='font-size:14.0pt;font-family:宋体'>服务器也可以。客户端的稳定性呢？</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>在</span><span lang=EN-US style='font-size:14.0pt'>flash</span><span
     style='font-size:14.0pt;font-family:宋体'>中连续播放</span><span lang=EN-US
     style='font-size:14.0pt'>10</span><span style='font-size:14.0pt;
     font-family:宋体'>天</span><span style='font-size:14.0pt'> </span><span
     style='font-size:14.0pt;font-family:宋体'>没有问题，</span><span lang=EN-US
     style='font-size:14.0pt'>flash</span><span style='font-size:14.0pt;
     font-family:宋体'>如果播放</span><span lang=EN-US style='font-size:14.0pt'>HTTP</span><span
     style='font-size:14.0pt;font-family:宋体'>流就真的很难讲。如果在</span><span
     lang=EN-US style='font-size:14.0pt'>PC</span><span style='font-size:14.0pt;
     font-family:宋体'>上需要客户端长时间播放，稳定播放，选择</span><span lang=EN-US
     style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;
     font-family:宋体'>会是最佳选择。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>稳定的较小延迟：</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>延迟在</span><span lang=EN-US
     style='font-size:14.0pt'>0.8-3</span><span style='font-size:14.0pt;
     font-family:宋体'>秒，能应用于交互式直播，视频会议，互动式直播等等。如果对延时有一定要求，就不要选择</span><span
     lang=EN-US style='font-size:14.0pt'>HLS</span><span style='font-size:14.0pt;
     font-family:宋体'>，</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>会是最佳选择。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>通用接入标准：</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>是编码器到服务器的实际标准协议，所有编码器都支持</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>推送流。选择</span><span lang=EN-US style='font-size:
     14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:宋体'>作为直播接入协议，能适配多种编码器，不至于绑定到一种编码器。如果服务器只能接入</span><span
     lang=EN-US style='font-size:14.0pt'>HTTP FLV</span><span style='font-size:
     14.0pt;font-family:宋体'>流，像某些公司做的私有协议，那么对接通用编码器就有问题。何必闭门造车？！绑定用户的方式在于良好的客户关系和优秀的软件质量，而不是上了贼船就</span><span
     style='font-size:14.0pt'> </span><span style='font-size:14.0pt;font-family:
     宋体'>下不了船了。</span></li>
</ul>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt'>直播将<span lang=EN-US>RTMP</span>作为基本协议，以各种方式转码为<span
lang=EN-US>RTMP</span>后输入到<span lang=EN-US>SRS</span>，输出为<span lang=EN-US>RTMP</span>和<span
lang=EN-US>HLS</span>，支持广泛的客户端和各种应用场景</span>。</p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097923"></a><a
name="_Toc462219409"><code><span lang=EN-US style='font-size:12.0pt;line-height:
173%'>2.2.2.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span></code><code><span
lang=EN-US style='font-size:12.0pt;line-height:173%'>WIKI</span></code></a></h3>

<p><span lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_SampleRTMP">https://github.com/ossrs/srs/wiki/v1_CN_SampleRTMP</a></span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097924"></a><a
name="_Toc462219410"><span lang=EN-US>2.2.3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>补充</span><span lang=EN-US>:SRS</span></a><span
style='font-family:宋体'>不支持点播</span></h3>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt'>不支持点播，一般点播不会使用<span lang=EN-US>RTMP</span>作为点播协议，目前点播以<span
lang=EN-US>HTTP</span>协议为主。<span lang=EN-US>Nginx rtmp</span>可以使用<span
lang=EN-US>rtmp</span>点播<span lang=EN-US>.</span>不过在测试过程中发现，托放支持不是很好<span
lang=EN-US>,</span>国内很少使用<span lang=EN-US>rtmp</span>点播，现在点播大都使用<span
lang=EN-US>http</span>。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097925"></a><a
name="_Toc462219411"><span class=3><span lang=EN-US style='font-weight:normal'>2.2.4.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp; </span></span></span><span
class=3><span style='font-family:宋体;font-weight:normal'>补充</span></span></a><span
class=3><span lang=EN-US style='font-weight:normal'>:</span></span><span
class=3><span style='font-family:宋体;font-weight:normal'>常用的第三方的推流与播放工具</span></span></h3>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>常用的第三方的推流工具有<span lang=EN-US>OBS,&nbsp; XSplit,&nbsp; FMLE,&nbsp;
video_broadcast++(Android)</span>，<span lang=EN-US>Broadcast_Me(iPhone),</span>除上面这些工具外，还可以使用<span
lang=EN-US>ffmpeg</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US style='font-size:14.0pt;font-family:
宋体'>&nbsp;&nbsp;&nbsp; </span><span style='font-size:14.0pt;font-family:宋体'>常用播放器<span
lang=EN-US>:&nbsp; flash player, ffplay, vlc</span>等。</span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097926"></a><a
name="_Toc462219412"></a><a name="_Toc456260510"><span lang=EN-US>2.3.<span
style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
style='font-family:宋体'>推送</span><span lang=EN-US>RTSP/UDP/FLV </span></a><span
style='font-family:宋体'>到</span><span lang=EN-US>SRS</span></h2>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt;font-family:宋体'>Streamer</span><span style='font-size:
14.0pt;font-family:宋体'>（流服务）是<span lang=EN-US>SRS</span>作为服务器侦听并接收其他协议的流（譬如<span
lang=EN-US>RTSP</span>，<span lang=EN-US>MPEG-TS over UDP</span>等等），将这些协议的流转换成<span
lang=EN-US>RTMP</span>推送给自己，以使用<span lang=EN-US>RTMP/HLS/HTTP</span>分发流。</span></p>

<p class=MsoNoSpacing><span style='font-size:14.0pt;font-family:宋体'>常见的应用场景包括：</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt;font-family:宋体'>Push MPEG-TS over UDP to SRS</span><span
style='font-size:14.0pt;font-family:宋体'>：通过<span lang=EN-US>UDP</span>协议，将<span
lang=EN-US>MPEG-TS</span>推送到<span lang=EN-US>SRS</span>，分发为<span lang=EN-US>RTMP/HLS/HTTP</span>流。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt;font-family:宋体'>Push RTSP to SRS</span><span
style='font-size:14.0pt;font-family:宋体'>：通过<span lang=EN-US>RTSP</span>协议，将流推送到<span
lang=EN-US>SRS</span>，分发为<span lang=EN-US>RTMP/HLS/HTTP</span>流。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt;font-family:宋体'>POST FLV over HTTP to SRS: </span><span
style='font-size:14.0pt;font-family:宋体'>通过<span lang=EN-US>HTTP</span>协议，将<span
lang=EN-US>FLV</span>流<span lang=EN-US>POST</span>到<span lang=EN-US>SRS</span>，分发为<span
lang=EN-US>RTMP/HLS/HTTP</span>流。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>备注：<span lang=EN-US>Streamer</span>将其他支持的协议推送<span lang=EN-US>RTMP</span>给<span
lang=EN-US>SRS</span>后，所有<span lang=EN-US>SRS</span>的功能都能支持。譬如，推<span
lang=EN-US>RTSP</span>流给<span lang=EN-US> Streamer</span>，<span lang=EN-US>Streamer</span>转成<span
lang=EN-US>RTMP</span>推送给<span lang=EN-US>SRS</span>，若<span lang=EN-US>vhost</span>是<span
lang=EN-US>edge</span>，<span lang=EN-US>SRS</span>将<span lang=EN-US>RTMP</span>流转发给源站。或者将<span
lang=EN-US>RTMP</span>流转码，或者直接转发。另外，所有分发方法都是可用的，譬如推<span lang=EN-US>RTSP</span>流给<span
lang=EN-US>Streamer</span>，<span lang=EN-US>Streamer</span>转成<span lang=EN-US>RTMP</span>推给<span
lang=EN-US>SRS</span>，以<span lang=EN-US>RTMP/HLS/HTTP</span>分发。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097927"></a><a
name="_Toc462219413"><span lang=EN-US>2.3.1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>Push MPEG-TS over UDP</span></a></h3>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt'>可以侦听一个<span lang=EN-US>udp</span>端口，编码器将流推送到这个<span
lang=EN-US>udp</span>端口（<span lang=EN-US>SPTS</span>）后，<span lang=EN-US>SRS</span>会转成一路<span
lang=EN-US>RTMP</span>流。后面<span lang=EN-US>RTMP</span>流能支持的功能都支持。</span></p>

<p><span style='font-size:14.0pt'>配置如下，参考<code><span lang=EN-US>conf/push.mpegts.over.udp.conf</span></code>：</span></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>#
the streamer cast stream from other protocol to SRS over RTMP.</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>#
@see https://github.com/ossrs/srs/tree/develop#stream-architecture</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>stream_caster
{</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
caster&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; mpegts_over_udp;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
output&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
rtmp://127.0.0.1/live/livestream;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>}</span></code></p>

<p>参考：<span lang=EN-US><a
href="https://github.com/ossrs/srs/issues/250#issuecomment-72321769">https://github.com/ossrs/srs/issues/250#issuecomment-72321769</a></span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097928"></a><a
name="_Toc462219414"><span lang=EN-US>2.3.2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>Push RTSP to SRS</span></a></h3>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;font-family:
宋体'>可以侦听一个</span><span lang=EN-US style='font-size:14.0pt'>tcp</span><span
style='font-size:14.0pt;font-family:宋体'>端口，编码器将流推送到这个</span><span lang=EN-US
style='font-size:14.0pt'>tcp</span><span style='font-size:14.0pt;font-family:
宋体'>端口（</span><span lang=EN-US style='font-size:14.0pt'>RTSP</span><span
style='font-size:14.0pt;font-family:宋体'>）后，</span><span lang=EN-US
style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;font-family:
宋体'>会转成一路</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt;font-family:宋体'>流。后面</span><span lang=EN-US
style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:
宋体'>流能支持的功能都支持。</span></p>

<p class=MsoNoSpacing><span style='font-size:14.0pt;font-family:宋体'>配置如下，参考</span><code><span
lang=EN-US style='font-size:14.0pt'>conf/push.rtsp.conf</span></code><span
style='font-size:14.0pt;font-family:宋体'>：</span></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>#
the streamer cast stream from other protocol to SRS over RTMP.</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>#
@see https://github.com/ossrs/srs/tree/develop#stream-architecture</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>stream_caster
{</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
caster&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; rtsp;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
output&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
rtmp://127.0.0.1/[app]/[stream];</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 554;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
rtp_port_min&nbsp;&nbsp;&nbsp; 57200;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>&nbsp;&nbsp;&nbsp;
rtp_port_max&nbsp;&nbsp;&nbsp; 57300;</span></code></p>

<p class=MsoNoSpacing><code><span lang=EN-US style='font-family:"Calibri",sans-serif'>}</span></code></p>

<p>参考：<span lang=EN-US><a
href="https://github.com/ossrs/srs/issues/133#issuecomment-75531884">https://github.com/ossrs/srs/issues/133#issuecomment-75531884</a></span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097929"></a><a
name="_Toc462219415"><span lang=EN-US>2.3.3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>Push HTTP FLV to SRS</span></a></h3>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt'>可以侦听一个<span lang=EN-US>HTTP</span>端口，编码器将流推送到这个<span
lang=EN-US>http</span>端口后，<span lang=EN-US>SRS</span>会转成一路<span lang=EN-US>RTMP</span>流。所有<span
lang=EN-US>RTMP</span>流的功能都能支持。</span></p>

<p>配置如下，参考<code><span lang=EN-US>conf/push.flv.conf</span></code>：</p>

<pre><code><span lang=EN-US># the streamer cast stream from other protocol to SRS over RTMP.</span></code></pre><pre><code><span
lang=EN-US># @see https://github.com/ossrs/srs/tree/develop#stream-architecture</span></code></pre><pre><code><span
lang=EN-US>stream_caster {</span></code></pre><pre><code><span lang=EN-US>&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;on;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp; caster&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; flv;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp; output&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; rtmp://127.0.0.1/[app]/[stream];</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp; listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 8936;</span></code></pre><pre><code><span
lang=EN-US>}</span></code></pre>

<p><span style='font-size:14.0pt'>这个配置时，客户端推流的地址，例如：<code><span lang=EN-US>http://127.0.0.1:8936/live/sea.flv</span></code><span
lang=EN-US><br>
</span>播放<span lang=EN-US>RTMP</span>流地址是：<code><span lang=EN-US>rtmp://127.0.0.1/live/sea</span></code><span
lang=EN-US><br>
</span>播放<span lang=EN-US>HLS</span>流地址是：<code><span lang=EN-US>http://127.0.0.1:8080/live/sea.m3u8</span></code></span></p>

<p><span style='font-size:14.0pt'>注意：需要配置<span lang=EN-US>HTTP</span>服务器和<span
lang=EN-US>HLS</span>，参考<code><span lang=EN-US>conf/push.flv.conf</span></code></span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097930"></a><a
name="_Toc462219416"><span lang=EN-US>2.3.4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>WIKI</span></a></h3>

<p class=MsoNoSpacing style='text-indent:15.75pt'><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v2_CN_Streamer"><span style='font-size:
12.0pt;font-family:宋体'>https://github.com/ossrs/srs/wiki/v2_CN_Streamer</span></a></span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097931"></a><a
name="_Toc462219418"></a><a name="_Toc456260511"><span lang=EN-US>2.4.<span
style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
style='font-family:宋体'>拉取流到</span><span lang=EN-US>SRS</span></a></h2>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>采集</span><span lang=EN-US style='font-size:14.0pt'>(Ingest)</span><span
style='font-size:14.0pt;font-family:宋体'>指的是将文件（</span><span lang=EN-US
style='font-size:14.0pt'>flv</span><span style='font-size:14.0pt;font-family:
宋体'>，</span><span lang=EN-US style='font-size:14.0pt'>mp4</span><span
style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
style='font-size:14.0pt'>mkv</span><span style='font-size:14.0pt;font-family:
宋体'>，</span><span lang=EN-US style='font-size:14.0pt'>avi</span><span
style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
style='font-size:14.0pt'>rmvb</span><span style='font-size:14.0pt;font-family:
宋体'>等等），流（</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
style='font-size:14.0pt'>RTMPT</span><span style='font-size:14.0pt;font-family:
宋体'>，</span><span lang=EN-US style='font-size:14.0pt'>RTMPS</span><span
style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
style='font-size:14.0pt'>RTSP</span><span style='font-size:14.0pt;font-family:
宋体'>，</span><span lang=EN-US style='font-size:14.0pt'>HTTP</span><span
style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
style='font-size:14.0pt'>HLS</span><span style='font-size:14.0pt;font-family:
宋体'>等等），设备等的数据，转封装为</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt;font-family:宋体'>流（若编码不是</span><span lang=EN-US
style='font-size:14.0pt'>h264/aac</span><span style='font-size:14.0pt;
font-family:宋体'>则需要转码），推送到</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>。采集基本上就是使用</span><span lang=EN-US
style='font-size:14.0pt'>FFMPEG</span><span style='font-size:14.0pt;font-family:
宋体'>作为编码器，或者转封装器，将外部流主动抓取到</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>采集的主要应用场景包括：</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>1.</span><span style='font-size:14.0pt;font-family:
宋体'>虚拟直播：将文件编码为直播流。可以指定多个文件后，</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>会循环播放。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>2.RTSP</span><span style='font-size:14.0pt;font-family:
宋体'>摄像头对接：以前安防摄像头都支持访问</span><span lang=EN-US style='font-size:14.0pt'>RTSP</span><span
style='font-size:14.0pt;font-family:宋体'>地址，</span><span lang=EN-US
style='font-size:14.0pt'>RTSP </span><span style='font-size:14.0pt;font-family:
宋体'>无法在互联网播放。可以将</span><span lang=EN-US style='font-size:14.0pt'>RTSP</span><span
style='font-size:14.0pt;font-family:宋体'>采集后，以</span><span lang=EN-US
style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:
宋体'>推送到</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>，后面的东西就不用讲了。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>3.</span><span style='font-size:14.0pt;font-family:
宋体'>直接采集设备：</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>采集功能可以作为编码器采集设备上的未压缩图像数据，譬如</span><span
lang=EN-US style='font-size:14.0pt'>video4linux</span><span style='font-size:
14.0pt;font-family:宋体'>和</span><span lang=EN-US style='font-size:14.0pt'>alsa</span><span
style='font-size:14.0pt;font-family:宋体'>设备，编码为</span><span lang=EN-US
style='font-size:14.0pt'>h264/aac</span><span style='font-size:14.0pt;
font-family:宋体'>后输出</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt;font-family:宋体'>到</span><span lang=EN-US
style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;font-family:
宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>4.</span><span style='font-size:14.0pt;font-family:
宋体'>将</span><span lang=EN-US style='font-size:14.0pt'>HTTP</span><span
style='font-size:14.0pt;font-family:宋体'>流采集为</span><span lang=EN-US
style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:
宋体'>：有些老的设备，能输出</span><span lang=EN-US style='font-size:14.0pt'>HTTP</span><span
style='font-size:14.0pt;font-family:宋体'>的</span><span lang=EN-US
style='font-size:14.0pt'>ts</span><span style='font-size:14.0pt;font-family:
宋体'>或</span><span lang=EN-US style='font-size:14.0pt'>FLV</span><span
style='font-size:14.0pt;font-family:宋体'>流，可以采集后转封装为</span><span lang=EN-US
style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:
宋体'>，支持</span><span lang=EN-US style='font-size:14.0pt'>HLS</span><span
style='font-size:14.0pt;font-family:宋体'>输出。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>总之，采集的应用场景主要是<span lang=EN-US>“SRS</span>拉流<span lang=EN-US>”</span>；能拉任意的流，只要<span
lang=EN-US>ffmpeg</span>支持；不是<span lang=EN-US>h264/aac</span>都没有关系，<span
lang=EN-US>ffmpeg</span>能转码。<span lang=EN-US>SRS</span>默认是支持<span lang=EN-US>“</span>推流<span
lang=EN-US>”</span>，即等待编码器推流上来，可以是专门的编码设备，<span lang=EN-US>FMLE</span>，<span
lang=EN-US>ffmpeg</span>，<span lang=EN-US>xsplit</span>，<span lang=EN-US>flash,
obs</span>等等。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>如此，<span lang=EN-US>SRS</span>的接入方式可以是<span lang=EN-US>“</span>推流到<span
lang=EN-US>SRS”</span>和<span lang=EN-US>“SRS</span>主动拉流<span lang=EN-US>”</span>，基本上作为源站的功能就完善了。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc462219419"></a><a
name="_Toc26097932"></a><a name="_Toc462219417"><span lang=EN-US>2.4.1.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp; </span></span><span
style='font-family:宋体'>补充</span><span lang=EN-US>:RTSP</span></a><span
style='font-family:宋体'>开源项目</span></h3>

<p class=MsoNormal style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>“</span><span style='font-size:14.0pt;font-family:
宋体'>推送</span><span lang=EN-US style='font-size:14.0pt'>RTSP/UDP/FLV </span><span
style='font-size:14.0pt;font-family:宋体'>到</span><span lang=EN-US
style='font-size:14.0pt'>SRS”</span><span style='font-size:14.0pt;font-family:
宋体'>功能目前版本</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>中，还是实验性功能，不是特别稳定，测试</span><span
lang=EN-US style='font-size:14.0pt'>rtsp</span><span style='font-size:14.0pt;
font-family:宋体'>过程中</span><span lang=EN-US style='font-size:14.0pt'>, </span><span
style='font-size:14.0pt;font-family:宋体'>声音正常，视频有花屏，</span><span lang=EN-US
style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;font-family:
宋体'>商业版应该这些功能已经稳定，因为</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>原作者</span><span lang=EN-US
style='font-size:14.0pt'>2016</span><span style='font-size:14.0pt;font-family:
宋体'>春节后更新很慢，现在主要做商业版。</span></p>

<p class=MsoNormal style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>RTSP</span><span style='font-size:14.0pt;font-family:
宋体'>协议主要在安防监控，</span><span lang=EN-US style='font-size:14.0pt'>iptv</span><span
style='font-size:14.0pt;font-family:宋体'>项目使用特别多。现在市场上网络摄象机（</span><span
lang=EN-US style='font-size:14.0pt'>IPC</span><span style='font-size:14.0pt;
font-family:宋体'>）中</span><span lang=EN-US style='font-size:14.0pt'>rtsp</span><span
style='font-size:14.0pt;font-family:宋体'>是标配。而现在互联网播放端通用的基本是</span><span
lang=EN-US style='font-size:14.0pt'>rtmp,hls</span><span style='font-size:14.0pt;
font-family:宋体'>，移动端通用的主要是</span><span lang=EN-US style='font-size:14.0pt'>hls</span><span
style='font-size:14.0pt;font-family:宋体'>。未来</span><span lang=EN-US
style='font-size:14.0pt'>IPC</span><span style='font-size:14.0pt;font-family:
宋体'>走互联网越来越多。所以对于通用型直播平台来说，多协议转换是非常重要的功能。</span></p>

<p class=MsoNormal style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体'>常用的</span><span lang=EN-US style='font-size:14.0pt'>rtsp</span><span
style='font-size:14.0pt;font-family:宋体'>开源流媒体服务器有</span><span lang=EN-US
style='font-size:14.0pt'>live555</span><span style='font-size:14.0pt;
font-family:宋体'>（</span><span lang=EN-US style='font-size:14.0pt;font-family:
"Microsoft YaHei UI",sans-serif;color:black'>http://www.live555.com</span><span
style='font-size:14.0pt;font-family:"Microsoft YaHei UI",sans-serif;color:black'>）</span><span
lang=EN-US style='font-size:14.0pt'>,Easydarwin</span><span style='font-size:
14.0pt;font-family:宋体'>（</span><span lang=EN-US style='font-size:14.0pt;
font-family:"Microsoft YaHei UI",sans-serif;color:black'>http://www.easydarwin.org</span><span
style='font-size:14.0pt;font-family:宋体'>）等。</span></p>

<p class=MsoNormal style='text-indent:28.0pt'><span style='font-size:14.0pt;
font-family:宋体;color:#333333'>目前</span><span lang=EN-US style='font-size:14.0pt;
font-family:"Helvetica",sans-serif;color:#333333'>EasyDarwin</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>流媒体云平台整套解决方案包括有：</span><span
lang=EN-US style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'>EasyCMS(</span><span style='font-size:14.0pt;font-family:宋体;
color:#333333'>中心管理服务、跨平台、支持分布式部署</span><span lang=EN-US style='font-size:14.0pt;
font-family:"Helvetica",sans-serif;color:#333333'>)</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>，</span><span lang=EN-US
style='font-size:14.0pt;font-family:"Helvetica",sans-serif;color:#333333'>EasyDarwin(</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>流媒体服务、跨平台、支持分布式部署</span><span
lang=EN-US style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'>)</span><span style='font-size:14.0pt;font-family:宋体;color:#333333'>，</span><span
lang=EN-US style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'>EasyRMS(</span><span style='font-size:14.0pt;font-family:宋体;
color:#333333'>云录像服务、跨平台、支持分布式部署</span><span lang=EN-US style='font-size:14.0pt;
font-family:"Helvetica",sans-serif;color:#333333'>)</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>，</span><span lang=EN-US
style='font-size:14.0pt;font-family:"Helvetica",sans-serif;color:#333333'>EasyCamera(</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>开源流媒体云摄像机方案、支持</span><span
lang=EN-US style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'>ARM</span><span style='font-size:14.0pt;font-family:宋体;
color:#333333'>、</span><span lang=EN-US style='font-size:14.0pt;font-family:
"Helvetica",sans-serif;color:#333333'>Android)</span><span style='font-size:
14.0pt;font-family:宋体;color:#333333'>，</span><span lang=EN-US style='font-size:
14.0pt;font-family:"Helvetica",sans-serif;color:#333333'>EasyNVR(</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>将标准</span><span
lang=EN-US style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'>RTSP/Onvif</span><span style='font-size:14.0pt;font-family:宋体;
color:#333333'>摄像机接入到云平台</span><span lang=EN-US style='font-size:14.0pt;
font-family:"Helvetica",sans-serif;color:#333333'>)</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>，</span><span lang=EN-US
style='font-size:14.0pt;font-family:"Helvetica",sans-serif;color:#333333'>EasyPlayer</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>（流媒体播放器），</span><span
lang=EN-US style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'>EasyClient</span><span style='font-size:14.0pt;font-family:宋体;
color:#333333'>（云平台客户端），</span><span style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'> </span><span style='font-size:14.0pt;font-family:宋体;color:#333333'>以及周边众多工具库</span><span
lang=EN-US style='font-size:14.0pt;font-family:"Helvetica",sans-serif;
color:#333333'>(EasyHLS / EasyRTSPClient / EasyPusher / EasyAACEncoder)</span><span
style='font-size:14.0pt;font-family:宋体;color:#333333'>，后续也将继续扩展的录像、回放等多种服务和工具集，各个功能单元既可以独立使用于项目，又可以整体使用，形成一个完整、简单、易用、高效的流媒体解决方案。</span></p>

<p class=MsoNormal><span lang=EN-US><img border=0 width=937 height=409 id="图片 8"
src="srs_wiki.files/image001.jpg"></span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097933"><span
lang=EN-US>2.4.2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp; </span></span><span
lang=EN-US>WIKI</span></a></h3>

<p class=MsoNoSpacing><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_Ingest"><span style='font-size:
12.0pt;font-family:宋体'>https://github.com/ossrs/srs/wiki/v1_CN_Ingest</span></a></span></p>

<p class=MsoNoSpacing><span lang=EN-US style='font-size:12.0pt;font-family:
宋体'>&nbsp;</span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097934"></a><a
name="_Toc462219420"><span lang=EN-US>2.5.<span style='font:7.0pt "Times New Roman"'>&nbsp;
</span></span><span lang=EN-US>RTMP</span></a><span style='font-family:宋体'>流的低延时配置</span></h2>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt'>流的延时一般在<span lang=EN-US>1-3</span>秒，比<span lang=EN-US>HLS</span>的延时小，<span
lang=EN-US>hls</span>延时<span lang=EN-US>10-30</span>秒左右。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097935"></a><a
name="_Toc462219421"><span lang=EN-US>2.5.1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>低延时直播应用</span></a></h3>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>直播应用中，<span
lang=EN-US>RTMP</span>和<span lang=EN-US>HLS</span>基本上可以覆盖所有客户端观看（参考：</span><span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_DeliveryHLS"><span
style='font-size:14.0pt'>DeliveryHLS</span></a></span><span style='font-size:
14.0pt'>），<span lang=EN-US>HLS</span>主要是延时比较大，<span lang=EN-US>RTMP</span>主要优势在于延时低。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097936"></a><a
name="_Toc462219422"><span lang=EN-US>2.5.2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>应用场景</span></a></h3>

<p><span style='font-size:14.0pt'>低延时应用场景包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>互动式直播：譬如</span><span lang=EN-US style='font-size:14.0pt'>2013</span><span
     style='font-size:14.0pt;font-family:宋体'>年大行其道的美女主播，游戏直播等等各种主播，流媒体分发给用户观看。用户可以文字聊天和主播互动。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>视频会议：</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
     style='font-size:14.0pt;font-family:宋体'>的</span><span lang=EN-US
     style='font-size:14.0pt'>DEMO</span><span style='font-size:14.0pt;
     font-family:宋体'>就有视频会议应用，我们要是有同事出差在外地，就用这个视频会议开内部会议。其实会议</span><span
     lang=EN-US style='font-size:14.0pt'>1</span><span style='font-size:14.0pt;
     font-family:宋体'>秒延时无所谓，因为人家讲完话后，其他人需要思考，思考的延时也会在</span><span lang=EN-US
     style='font-size:14.0pt'>1</span><span style='font-size:14.0pt;font-family:
     宋体'>秒左右。当然如果用视频会议吵架就不行。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>其他：监控，直播也有些地方需要对延迟有要求，互联网上</span><span lang=EN-US
     style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;
     font-family:宋体'>协议的延迟基本上能够满足要求。</span></li>
</ul>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097937"></a><a
name="_Toc462219423"><span lang=EN-US>2.5.3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>RTMP</span></a><span style='font-family:宋体'>和延时</span></h3>

<p><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
14.0pt'>的特点如下：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>Adobe</span><span style='font-size:14.0pt;font-family:宋体'>支持得很好：</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>实际上是现在编码器输出的工业标准协议，基本上所有的编码器（摄像头之类）都支持</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>输出。原因在于</span><span lang=EN-US style='font-size:
     14.0pt'>PC</span><span style='font-size:14.0pt;font-family:宋体'>市场巨大，</span><span
     lang=EN-US style='font-size:14.0pt'>PC</span><span style='font-size:14.0pt;
     font-family:宋体'>主要是</span><span lang=EN-US style='font-size:14.0pt'>Windows</span><span
     style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
     style='font-size:14.0pt'>Windows</span><span style='font-size:14.0pt;
     font-family:宋体'>的浏览器基本上都支持</span><span lang=EN-US style='font-size:14.0pt'>flash</span><span
     style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
     style='font-size:14.0pt'>Flash</span><span style='font-size:14.0pt;
     font-family:宋体'>又支持</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>支持得灰常好。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>适合长时间播放：因为</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>支持的很完善，所以能做到</span><span
     lang=EN-US style='font-size:14.0pt'>flash</span><span style='font-size:
     14.0pt;font-family:宋体'>播放</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>流长时间不断流，当时测试是</span><span
     lang=EN-US style='font-size:14.0pt'>100</span><span style='font-size:14.0pt;
     font-family:宋体'>万秒，即</span><span lang=EN-US style='font-size:14.0pt'>10</span><span
     style='font-size:14.0pt;font-family:宋体'>天多可以连续播放。</span><span
     style='font-size:14.0pt'> </span><span style='font-size:14.0pt;font-family:
     宋体'>对于商用流媒体应用，客户端的稳定性当然也是必须的，否则最终用户看不了还怎么玩？我就知道有个教育客户，最初使用播放器播放</span><span
     lang=EN-US style='font-size:14.0pt'>http</span><span style='font-size:
     14.0pt;font-family:宋体'>流，需要播放不同的</span><span style='font-size:14.0pt'> </span><span
     style='font-size:14.0pt;font-family:宋体'>文件，结果就总出问题，如果换成服务器端将不同的文件转换成</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>流，客户端就可以一直播放；该客户走</span><span lang=EN-US
     style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;
     font-family:宋体'>方案后，经过</span><span lang=EN-US style='font-size:14.0pt'>CDN</span><span
     style='font-size:14.0pt;font-family:宋体'>分发，没听说客户端出</span><span
     style='font-size:14.0pt'> </span><span style='font-size:14.0pt;font-family:
     宋体'>问题了。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>延迟较低：比起</span><span lang=EN-US style='font-size:14.0pt'>YY</span><span
     style='font-size:14.0pt;font-family:宋体'>的那种</span><span lang=EN-US
     style='font-size:14.0pt'>UDP</span><span style='font-size:14.0pt;
     font-family:宋体'>私有协议，</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>算延迟大的（延迟在</span><span lang=EN-US
     style='font-size:14.0pt'>1-3</span><span style='font-size:14.0pt;
     font-family:宋体'>秒），比起</span><span lang=EN-US style='font-size:14.0pt'>HTTP</span><span
     style='font-size:14.0pt;font-family:宋体'>流的延时（一般在</span><span lang=EN-US
     style='font-size:14.0pt'>10</span><span style='font-size:14.0pt;
     font-family:宋体'>秒以上）</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>算低延时。</span><span
     style='font-size:14.0pt'> </span><span style='font-size:14.0pt;font-family:
     宋体'>一般的直播应用，只要不是电话类对话的那种要求，</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>延迟是可以接受的。在一般的视频会议（参考</span><span
     lang=EN-US style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;
     font-family:宋体'>的视频会议延时）应用中，</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
     style='font-size:14.0pt;font-family:宋体'>延时也能接</span><span
     style='font-size:14.0pt'> </span><span style='font-size:14.0pt;font-family:
     宋体'>受，原因是别人在说话的时候我们一般在听，实际上</span><span lang=EN-US style='font-size:14.0pt'>1</span><span
     style='font-size:14.0pt;font-family:宋体'>秒延时没有关系，我们也要思考（话说有些人的</span><span
     lang=EN-US style='font-size:14.0pt'>CPU</span><span style='font-size:14.0pt;
     font-family:宋体'>处理速度还没有这么快）。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>有累积延迟：技术一定要知道弱点，</span><span lang=EN-US style='font-size:
     14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:宋体'>有个弱点就是累积误差，原因是</span><span
     lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:
     14.0pt;font-family:宋体'>基于</span><span lang=EN-US style='font-size:14.0pt'>TCP</span><span
     style='font-size:14.0pt;font-family:宋体'>不会丢包。所以当网络状态差时，服务器会将包缓存起</span><span
     style='font-size:14.0pt'> </span><span style='font-size:14.0pt;font-family:
     宋体'>来，导致累积的延迟；待网络状况好了，就一起发给客户端。这个的对策就是，当客户端的缓冲区很大，就断开重连。当然</span><span
     lang=EN-US style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;
     font-family:宋体'>也提供配置。</span></li>
</ul>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097938"></a><a
name="_Toc462219424"><span lang=EN-US>2.5.4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>累积延迟</span></a></h3>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>除了<span
lang=EN-US>GOP-Cache</span>，还有一个有关系，就是累积延迟。<span lang=EN-US>SRS</span>可以配置直播队列的长度，服务器会将数据放在直播队列中，如果超过这个长度就清空到最后一个<span
lang=EN-US>I</span>帧：</span></p>

<pre><span lang=EN-US>vhost your_vhost {</span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span
class=pl-c># the max live queue length in seconds.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c># if the messages in the queue exceed the max length, </span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;<span class=pl-c># drop the old whole gop.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c># default: 30</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; queue_length&nbsp;&nbsp;&nbsp; 10<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>}</span></pre>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>当然这个不能配置太小，譬如<span
lang=EN-US>GOP</span>是<span lang=EN-US>1</span>秒，<span lang=EN-US>queue_length</span>是<span
lang=EN-US>1</span>秒，这样会导致有<span lang=EN-US>1</span>秒数据就清空，会导致跳跃。</span></p>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>有更好的方法？有的。延迟基本上就等于客户端的缓冲区长度，因为延迟大多由于网络带宽低，服务器缓存后一起发给客户端，现象就是客户端的缓冲区变大了，譬如<span
lang=EN-US>NetStream.BufferLength=5</span>秒，那么说明缓冲区中至少有<span lang=EN-US>5</span>秒数据。</span></p>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>处理累积延迟的最好方法，是客户端检测到缓冲区有很多数据了，如果可以的话，就重连服务器。当然如果网络一直不好，那就没有办法了。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097939"></a><a
name="_Toc462219425"><span lang=EN-US>2.5.5.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>低延时配置</span></a></h3>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>考虑<span
lang=EN-US>GOP-Cache</span>和累积延迟，推荐的低延时配置如下（参考<span lang=EN-US>min.delay.com</span>）</span>：</p>

<p class=MsoNoSpacing><span class=pl-c><span lang=EN-US># the listen ports,
split by space.</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
1935<span class=pl-k>;</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>vhost __defaultVhost__ {</span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#
whether cache the last gop.</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c># if
on, cache the last gop and dispatch to client,</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#&nbsp;&nbsp;
to enable fast startup for client, client play immediately.</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c># if
off, send the latest media data to client,</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#&nbsp;&nbsp;
client need to wait for the next Iframe to decode and show the video.</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#
set to off if requires min delay;</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#
set to on if requires client fast startup.</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#
default: on</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp;
gop_cache&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; off<span class=pl-k>;</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#
the max live queue length in seconds.</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c># if
the messages in the queue exceed the max length, </span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#
drop the old whole gop.</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c>#
default: 30</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp;
queue_length&nbsp;&nbsp;&nbsp; 10<span class=pl-k>;</span></span></p>

<p class=MsoNoSpacing><span lang=EN-US>}</span></p>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>当然，服务器的性能也要考虑，不可以让一个<span
lang=EN-US>SRS</span>进程跑太高带宽，一般<span lang=EN-US>CPU</span>在<span lang=EN-US>80%</span>以下不会影响延迟，连接数参考</span><span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_Performance"><span
lang=EN-US style='font-size:14.0pt'><span lang=EN-US>性能</span></span></a></span><span
style='font-size:14.0pt'>。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097940"></a><a
name="_Toc462219426"><span lang=EN-US>2.5.6.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>WIKI</span></a></h3>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_SampleRealtime">https://github.com/ossrs/srs/wiki/v3_CN_SampleRealtime</a></span></p>

<p class=MsoNoSpacing><span lang=EN-US style='font-size:12.0pt;font-family:
宋体'>&nbsp;</span></p>

<h1 style='margin-left:21.25pt;text-indent:-21.25pt'><a name="_Toc26097941"></a><a
name="_Toc462219427"></a><a name="_Toc456260512"><span lang=EN-US>3.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp; </span></span>流</a>变换</h1>

<p class=MsoNormal style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;font-family:
宋体'>还支持将接入的</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt;font-family:宋体'>流进行各种变换，譬如将</span><span lang=EN-US
style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:
宋体'>流转码、流截图、转发给其他服务器、转封装成</span><span lang=EN-US style='font-size:14.0pt'>HTTP-FLV</span><span
style='font-size:14.0pt;font-family:宋体'>流、转封装成</span><span lang=EN-US
style='font-size:14.0pt'>HLS</span><span style='font-size:14.0pt;font-family:
宋体'>、转封装成</span><span lang=EN-US style='font-size:14.0pt'>HDS</span><span
style='font-size:14.0pt;font-family:宋体'>、录制成</span><span lang=EN-US
style='font-size:14.0pt'>FLV</span><span style='font-size:14.0pt;font-family:
宋体'>等。</span></p>

<h2 style='margin-left:1.0cm;text-indent:-1.0cm'><a name="_Toc26097942"></a><a
name="_Toc462219428"></a><a name="_Toc456260513"><span lang=EN-US>3.1.<span
style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
style='font-family:宋体'>将</span><span lang=EN-US>RTMP</span></a><span
style='font-family:宋体'>流转码</span></h2>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;font-family:
宋体'>通过</span><span lang=EN-US style='font-size:14.0pt'>FFMPEG</span><span
style='font-size:14.0pt;font-family:宋体'>对</span><span lang=EN-US
style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:
宋体'>直播流转码，</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>在收到编码器推送的直播流后，可以对直播流进行转码，输出</span><span
lang=EN-US style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;
font-family:宋体'>流到服务器（也可以到</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>自己）。如使用该功能将直播流转换多码率流，或者给流添加水印等。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097943"></a><a
name="_Toc462219429"><span lang=EN-US>3.1.1.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>应用场景</span></a></h3>

<p><span style='font-size:14.0pt'>转码的重要应用场景包括：</span></p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>推送一路高码率，转多路输出。譬如：游戏直播中，推送一路</span><span lang=EN-US
     style='font-size:14.0pt'>1080p</span><span style='font-size:14.0pt;
     font-family:宋体'>流到</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
     style='font-size:14.0pt;font-family:宋体'>，</span><span lang=EN-US
     style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;
     font-family:宋体'>可以转码输出</span><span lang=EN-US style='font-size:14.0pt'>1080p/720p/576p</span><span
     style='font-size:14.0pt;font-family:宋体'>多路，低码率可以给移动设备观看。这样节省了推流带宽（一般源站为</span><span
     lang=EN-US style='font-size:14.0pt'>BGP</span><span style='font-size:14.0pt;
     font-family:宋体'>带宽，很贵），也减轻了客户端压力（譬如客户端边玩游戏边直播）。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>支持多屏输出。譬如：网页推流（主播）编码为</span><span lang=EN-US
     style='font-size:14.0pt'>vp6/mp3</span><span style='font-size:14.0pt;
     font-family:宋体'>或</span><span lang=EN-US style='font-size:14.0pt'>speex</span><span
     style='font-size:14.0pt;font-family:宋体'>，推流到</span><span lang=EN-US
     style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;
     font-family:宋体'>后无法支持</span><span lang=EN-US style='font-size:14.0pt'>HLS</span><span
     style='font-size:14.0pt;font-family:宋体'>（要求</span><span lang=EN-US
     style='font-size:14.0pt'>h264+aac</span><span style='font-size:14.0pt;
     font-family:宋体'>），可以转码成</span><span lang=EN-US style='font-size:14.0pt'>h264+aac</span><span
     style='font-size:14.0pt;font-family:宋体'>后切片成</span><span lang=EN-US
     style='font-size:14.0pt'>HLS</span><span style='font-size:14.0pt;
     font-family:宋体'>或者推送到其他服务器再分发。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>加水印。适用于需要对流进行加水印的情况，譬如打上自己的</span><span lang=EN-US
     style='font-size:14.0pt'>logo</span><span style='font-size:14.0pt;
     font-family:宋体'>。</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
     style='font-size:14.0pt;font-family:宋体'>支持文字水印和图片水印，也可以支持视频作为水印，或者将两路流叠加（参考</span><span
     lang=EN-US style='font-size:14.0pt'>ffmpeg</span><span style='font-size:
     14.0pt;font-family:宋体'>的用法）。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>截图。</span><span style='font-size:14.0pt'> </span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-size:14.0pt;
     font-family:宋体'>其他滤镜：</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
     style='font-size:14.0pt;font-family:宋体'>支持所有</span><span lang=EN-US
     style='font-size:14.0pt'>ffmpeg</span><span style='font-size:14.0pt;
     font-family:宋体'>的滤镜。</span></li>
</ol>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097944"></a><a
name="_Toc462219430"><span lang=EN-US>3.1.2.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>工作流程</span></a></h3>

<p><span lang=EN-US style='font-size:14.0pt'>SRS</span><span style='font-size:
14.0pt'>转码的主要流程包括：</span></p>

<p class=MsoNormal align=left style='margin-left:36.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US style='font-size:14.0pt'>1.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span
style='font-size:14.0pt;font-family:宋体'>编码器推送</span><span lang=EN-US
style='font-size:14.0pt'>RTMP</span><span style='font-size:14.0pt;font-family:
宋体'>流到</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>的</span><span lang=EN-US
style='font-size:14.0pt'>vhost</span><span style='font-size:14.0pt;font-family:
宋体'>。</span></p>

<p class=MsoNormal align=left style='margin-left:36.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US style='font-size:14.0pt'>2.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span
lang=EN-US style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;
font-family:宋体'>的</span><span lang=EN-US style='font-size:14.0pt'>vhost</span><span
style='font-size:14.0pt;font-family:宋体'>若配置了转码，则进行转码。</span></p>

<p class=MsoNormal align=left style='margin-left:36.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US style='font-size:14.0pt'>3.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span
style='font-size:14.0pt;font-family:宋体'>转码后，按照配置，推送到</span><span lang=EN-US
style='font-size:14.0pt'>SRS</span><span style='font-size:14.0pt;font-family:
宋体'>本身或者其他</span><span lang=EN-US style='font-size:14.0pt'>RTMP</span><span
style='font-size:14.0pt;font-family:宋体'>服务器。</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097945"></a><a
name="_Toc462219431"><span lang=EN-US>3.1.3.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>配置</span></a></h3>

<p><span lang=EN-US style='font-size:14.0pt'>SRS</span><span style='font-size:
14.0pt'>可以对<span lang=EN-US>vhost</span>的所有的流转码，或者对某些<span lang=EN-US>app</span>的流转码，或者对某些流转码。</span></p>

<p><span style='font-size:14.0pt'>对<span lang=EN-US>app</span>或流转码时，只要在<span
lang=EN-US>transcode</span>后面加<span lang=EN-US>app</span>和<span lang=EN-US>stream</span>就可以。譬如：</span></p>

<pre><span lang=EN-US>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>vhost __defaultVhost__ {</span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c># </span></span><span
class=pl-c>对<span lang=EN-US>app</span>为<span lang=EN-US>live</span>的所有流转码</span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; transcode live{</span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; }</span></pre><pre><span lang=EN-US>}</span></pre>

<p><span style='font-size:14.0pt'>以及对指定的流转码：</span></p>

<pre><span lang=EN-US>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>vhost __defaultVhost__ {</span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; <span class=pl-c># </span></span><span
class=pl-c>对<span lang=EN-US>app</span>为<span lang=EN-US>live</span>并且流名称为<span
lang=EN-US>livestream</span>的流转码</span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp; transcode live/livestream{</span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; }</span></pre><pre><span lang=EN-US>}</span></pre>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097946"></a><a
name="_Toc462219432"><span lang=EN-US>3.1.4.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span style='font-family:宋体'>转码规则</span></a></h3>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt'>的转码参数全是<span lang=EN-US>FFMPEG</span>的参数，有些参数<span
lang=EN-US>SRS</span>做了自定义，见下表。</span></p>

<table class=MsoNormalTable border=0 cellpadding=0 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>SRS</span></b><b><span style='font-family:宋体;color:black'>参数</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FFMPEG</span></b><b><span style='font-family:
   宋体;color:black'>参数</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>实例</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>说明</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vcodec</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vcodec</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -vcodec
  libx264 ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>指定视频编码器</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vbitrate</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>b:v</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -b:v
  500000 ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>输出的视频码率</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vfps</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>r</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -r 25 ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>输出的视频帧率</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vwidth/vheight</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -s 400x300
  -aspect 400:300 ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>输出的视频宽度</span><span
  lang=EN-US style='color:black'>x</span><span style='font-family:宋体;
  color:black'>高度，以及宽高比</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vthreads</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>threads</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -threads 8
  ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>编码线程数</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vprofile</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>profile:v</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -profile:v
  high ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>编码</span><span
  lang=EN-US style='color:black'>x264</span><span style='font-family:宋体;
  color:black'>的</span><span lang=EN-US style='color:black'>profile</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vpreset</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>preset</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -preset
  medium ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>编码</span><span
  lang=EN-US style='color:black'>x264</span><span style='font-family:宋体;
  color:black'>的</span><span lang=EN-US style='color:black'>preset</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>acodec</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>acodec</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -acodec
  libfdk_aac ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>音频编码器</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>abitrate</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>b:a</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -b:a 70000
  ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>音频输出码率。</span><span
  lang=EN-US style='color:black'>libaacplus</span><span style='font-family:
  宋体;color:black'>：</span><span lang=EN-US style='color:black'>16-72k</span><span
  style='font-family:宋体;color:black'>。</span><span lang=EN-US style='color:
  black'>libfdk_aac</span><span style='font-family:宋体;color:black'>没有限制。</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>asample_rate</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ar</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -ar 44100
  ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>音频采样率</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>achannels</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ac</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ffmpeg ... -ac 2 ...</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>音频声道</span></p>
  </td>
 </tr>
</table>

<p><span style='font-size:14.0pt;color:black'>另外，还有三个是可以加其他</span><span
lang=EN-US style='font-size:14.0pt'>ffmpeg</span><span style='font-size:14.0pt'>参数：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>vfilter</span><span style='font-size:14.0pt;font-family:宋体'>：添加在</span><span
     lang=EN-US style='font-size:14.0pt'>vcodec</span><span style='font-size:
     14.0pt;font-family:宋体'>之前的滤镜参数。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>vparams</span><span style='font-size:14.0pt;font-family:宋体'>：添加在</span><span
     lang=EN-US style='font-size:14.0pt'>vcodec</span><span style='font-size:
     14.0pt;font-family:宋体'>之后，</span><span lang=EN-US style='font-size:14.0pt'>acodec</span><span
     style='font-size:14.0pt;font-family:宋体'>之前的视频编码参数。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>aparams</span><span style='font-size:14.0pt;font-family:宋体'>：添加在</span><span
     lang=EN-US style='font-size:14.0pt'>acodec</span><span style='font-size:
     14.0pt;font-family:宋体'>之后，</span><span lang=EN-US style='font-size:14.0pt'>-y</span><span
     style='font-size:14.0pt;font-family:宋体'>之前的音频编码参数。</span></li>
</ul>

<p class=MsoNormal><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt;font-family:宋体'>的</span><span lang=EN-US
style='font-size:14.0pt'>ffmpeg</span><span style='font-size:14.0pt;font-family:
宋体'>转码器可以使用</span><span lang=EN-US style='font-size:14.0pt'>ffmpeg</span><span
style='font-size:14.0pt;font-family:宋体'>所有功能如</span><span lang=EN-US
style='font-size:14.0pt'>:</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>1 </span><span style='font-size:14.0pt;font-family:
宋体'>不转码只复制流：可以配置</span><span lang=EN-US style='font-size:14.0pt'>vcodec/acodec
copy</span><span style='font-size:14.0pt;font-family:宋体'>，实现不转码。譬如，视频为</span><span
lang=EN-US style='font-size:14.0pt'>h264</span><span style='font-size:14.0pt;
font-family:宋体'>编码，但是音频是</span><span lang=EN-US style='font-size:14.0pt'>mp3/speex</span><span
style='font-size:14.0pt;font-family:宋体'>，需要转码音频为</span><span lang=EN-US
style='font-size:14.0pt'>aac</span><span style='font-size:14.0pt;font-family:
宋体'>，然后切片为</span><span lang=EN-US style='font-size:14.0pt'>HLS</span><span
style='font-size:14.0pt;font-family:宋体'>输出。</span></p>

<p class=MsoNoSpacing style='text-indent:28.0pt'><span lang=EN-US
style='font-size:14.0pt'>2 </span><span style='font-size:14.0pt;font-family:
宋体'>禁用视频或者音频：可以禁用视频或者音频，只输出音频或视频。譬如，电台可以丢弃视频，对音频转码为</span><span lang=EN-US
style='font-size:14.0pt'>aac</span><span style='font-size:14.0pt;font-family:
宋体'>后输出</span><span lang=EN-US style='font-size:14.0pt'>HLS</span><span
style='font-size:14.0pt;font-family:宋体'>。该配置只输出纯音频，编码为</span><span lang=EN-US
style='font-size:14.0pt'>aac</span><span style='font-size:14.0pt;font-family:
宋体'>。</span></p>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>conf/full.conf</span><span
style='font-size:14.0pt'>中有很多<span lang=EN-US>FFMPEG</span>转码配置的实例，也可以参考<span
lang=EN-US>ffmpeg</span>的命令行。</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>mirror.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>将视频流上半截，翻转到下半截，看起来像个镜子。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>drawtext.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>加文字水印。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>crop.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>剪裁视频。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>logo.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>添加图片</span><span lang=EN-US style='font-size:14.0pt'>logo</span><span
     style='font-size:14.0pt;font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>audio.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>只对音频转码。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>copy.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>不转码只转封装，类似于</span><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
     style='font-size:14.0pt;font-family:宋体'>的</span><span lang=EN-US
     style='font-size:14.0pt'>Forward</span><span style='font-size:14.0pt;
     font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>all.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>转码参数的详细说明。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>ffempty.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>一个</span><span lang=EN-US style='font-size:14.0pt'>ffmpeg</span><span
     style='font-size:14.0pt;font-family:宋体'>的</span><span lang=EN-US
     style='font-size:14.0pt'>mock</span><span style='font-size:14.0pt;
     font-family:宋体'>，不转码只打印参数。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>app.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>对指定的</span><span lang=EN-US style='font-size:14.0pt'>app</span><span
     style='font-size:14.0pt;font-family:宋体'>的流转码。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>stream.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>对指定的流转码。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     14.0pt'>vn.transcode.srs.com </span><span style='font-size:14.0pt;
     font-family:宋体'>只输出音频，禁止视频输出。</span></li>
</ul>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097947"></a><a
name="_Toc462219433"><span lang=EN-US>3.1.5.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>Transcode on ARM cpu</span></a></h3>

<p style='text-indent:28.0pt'><span lang=EN-US style='font-size:14.0pt'>SRS</span><span
style='font-size:14.0pt'>可以在<span lang=EN-US>ARM</span>下调用系统的<span lang=EN-US>ffmpeg</span>转码，参考：</span><span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_ARMTranscode"><span
style='font-size:14.0pt'>Raspberry pi </span><span lang=EN-US style='font-size:
14.0pt'><span lang=EN-US>转码</span></span></a></span></p>

<p style='text-indent:28.0pt'><span style='font-size:14.0pt'>注意：使用自己的工具时，需要禁用<span
lang=EN-US>ffmpeg</span>，但是打开<span lang=EN-US>transcode</span>选项：<code><span
lang=EN-US>--with-transcode --without-ffmpeg</span></code>，这样就不会编译<span
lang=EN-US>ffmpeg</span>，但是编译了直播转码功能。参考</span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097948"></a><a
name="_Toc462219434"><span lang=EN-US>3.1.6.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>FFMPEG Transcode the Stream by Flash encoder</span></a></h3>

<p><span lang=EN-US>flash</span>可以当作编码器推流，参考演示中的编码器或者视频会议。<span lang=EN-US>flash</span>只支持<span
lang=EN-US>speex/nellymoser/pcma/pcmu</span>，但<span lang=EN-US>flash</span>会有一个特性，没有声音时就没有音频包。<span
lang=EN-US>FFMPEG</span>会依赖于这些音频包，如果没有会认为没有音频。</p>

<p>所以<span lang=EN-US>FFMPEG</span>用来转码<span lang=EN-US>flash</span>推上来的<span
lang=EN-US>RTMP</span>流时，可能会有一个问题：<span lang=EN-US>ffmpeg</span>认为没有音频。</p>

<p>另外，<span lang=EN-US>FFMPEG</span>取<span lang=EN-US>flash</span>的流的时间会很长，也可能是在等待这些音频包。</p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097949"><span
lang=EN-US>3.1.7.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp; </span></span><span
style='font-family:宋体'>补充</span><span lang=EN-US>:</span></a><span
style='font-family:宋体'>测试效果图</span></h3>

<p class=MsoNormal><span lang=EN-US><img border=0 width=1106 height=586
id="图片 4" src="srs_wiki.files/image002.jpg"></span></p>

<h3 style='margin-left:35.45pt;text-indent:-35.45pt'><a name="_Toc26097950"></a><a
name="_Toc462219435"><span lang=EN-US>3.1.8.<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;
</span></span><span lang=EN-US>WIKI</span></a></h3>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_SampleFFMPEG">https://github.com/ossrs/srs/wiki/v1_CN_SampleFFMPEG</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h2><a name="_Toc26097951"></a><a name="_Toc462219436"></a><a
name="_Toc456260514"><span style='font-family:宋体'>流截图</span></a></h2>

<p><span lang=EN-US>&nbsp;</span>使用<span lang=EN-US>SRS</span>实现截图有以下几种方式可以实现：</p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     12.0pt;font-family:宋体'>HttpCallback</span><span style='font-size:12.0pt;
     font-family:宋体'>：使用<span lang=EN-US>HTTP</span>回调，收到<span lang=EN-US>on_publish</span>事件后开启<span
     lang=EN-US>ffmpeg</span>进程截图，收到<span lang=EN-US>on_unpublish</span>事件后停止<span
     lang=EN-US>ffmpeg</span>进程。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-size:
     12.0pt;font-family:宋体'>Transcoder</span><span style='font-size:12.0pt;
     font-family:宋体'>：转码可以配置为截图，实际上是通过<span lang=EN-US>ffmpeg</span>命令将直播流按一帧数据转换为图片。</span></li>
</ol>

<h3><a name="_Toc26097952"></a><a name="_Toc462219437"><span lang=EN-US>WIKI</span></a></h3>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_Snapshot">https://github.com/ossrs/srs/wiki/v3_CN_Snapshot</a></span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097953"></a><a name="_Toc462219438"><span style='font-family:
宋体'>补充</span><span lang=EN-US>:</span></a><span style='font-family:宋体'>测试效果图</span></h3>

<p class=MsoNormal align=left style='margin-left:18.0pt;text-align:left'><span
lang=EN-US><img border=0 width=959 height=428 id="图片 1"
src="srs_wiki.files/image003.jpg"></span></p>

<h3><a name="_Toc26097954"></a><a name="_Toc462219439"></a><a
name="_Toc456260515"><span style='font-family:宋体'>转发给其他服务器</span></a><span
class=MsoHyperlink><span lang=EN-US style='color:windowtext;text-decoration:
none'>(Forward)</span></span></h3>

<p class=MsoNormal><span lang=EN-US>&nbsp;&nbsp; &nbsp;SRS</span><span
style='font-family:宋体'>可以将送到</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>的流转发给其他</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>服务器，实现简单集群</span><span lang=EN-US>/</span><span
style='font-family:宋体'>热备功能，也可以实现一路流热备（譬如编码器由于带宽限制，只能送一路流到</span><span
lang=EN-US>RTMP</span><span style='font-family:宋体'>服务器，要求</span><span
lang=EN-US>RTMP</span><span style='font-family:宋体'>服务器能将这路流也转发给其他</span><span
lang=EN-US>RTMP</span><span style='font-family:宋体'>备用服务器，实现主备容错集群）。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>Forward</span><span
style='font-family:宋体'>就是</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>将流拷贝输出给其他的</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>服务器，以</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>转发给</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>为例：</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>主</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>：</span><span lang=EN-US>Master,
</span><span style='font-family:宋体'>编码器推流到主</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>，主</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>将流处理的同时，将流转发到备</span><span lang=EN-US>SRS</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>备</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>：</span><span lang=EN-US>Slave,
</span><span style='font-family:宋体'>主</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>转发流到备</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>，就像编码器推送流到备用</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>一样。</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span style='font-family:宋体'>该功能会在集群与</span><span
lang=EN-US>CDN</span><span style='font-family:宋体'>相关功能章节做详细的介绍</span></p>

<p><span lang=EN-US>forward</span>也可以用作搭建小型集群。架构图如下：</p>

<pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img
border=0 width=745 height=411 id="图片 9" src="srs_wiki.files/image004.png"></span></pre>

<h4><a name="_Toc462219440"><span lang=EN-US>WIKI</span></a><span lang=EN-US> </span></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_SampleForward">https://github.com/ossrs/srs/wiki/v3_CN_SampleForward</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097955"></a><a name="_Toc462219441"></a><a
name="_Toc456260516"><span style='font-family:宋体'>转封装成</span><span lang=EN-US>HTTP</span></a><span
style='font-family:宋体'>直播流</span></h3>

<p class=MsoListParagraph style='margin-left:18.0pt;text-indent:0cm'><span
lang=EN-US>SRS</span><span style='font-family:宋体'>支持将</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>流转封装为</span><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>流，</span><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>流格式可以</span><span lang=EN-US>flv, ts,mp3,aac</span><span
style='font-family:宋体'>等。</span></p>

<h4><a name="_Toc462219442"><span lang=EN-US>HTTP TS Live Stream</span></a></h4>

<p><span lang=EN-US>SRS</span>支持将<span lang=EN-US>RTMP</span>流转封装为<span
lang=EN-US>HTTP ts</span>流，即在<span lang=EN-US>publish</span>发布<span lang=EN-US>RTMP</span>流时，在<span
lang=EN-US>SRS</span>的<span lang=EN-US>http</span>模块中挂载一个对应的<span lang=EN-US>http</span>地址（根据配置），用户在访问这个<span
lang=EN-US>http ts</span>文件时，从<span lang=EN-US>rtmp</span>流转封装为<span
lang=EN-US>ts</span>分发给用户。</p>

<h4><a name="_Toc462219443"><span lang=EN-US>HTTP Mp3 Live Stream</span></a></h4>

<p><span lang=EN-US>SRS</span>支持将<span lang=EN-US>rtmp</span>流中的视频丢弃，将音频流转封装为<span
lang=EN-US>mp3</span>格式，在<span lang=EN-US>SRS</span>的<span lang=EN-US>http</span>模块中挂载对应的<span
lang=EN-US>http</span>地址（根据配置），用户在访问这个<span lang=EN-US>http mp3</span>文件时，从<span
lang=EN-US>rtmp</span>转封装为<span lang=EN-US>mp3</span>分发给用户。</p>

<h4><a name="_Toc462219444"><span lang=EN-US>HTTP Aac Live Stream</span></a></h4>

<p><span lang=EN-US>SRS</span>支持将<span lang=EN-US>rtmp</span>流中的视频丢弃，将音频流转封装为<span
lang=EN-US>aac</span>格式，在<span lang=EN-US>SRS</span>的<span lang=EN-US>http</span>模块中挂载对应的<span
lang=EN-US>http</span>地址（根据配置），用户在访问这个<span lang=EN-US>http aac</span>文件时，从<span
lang=EN-US>rtmp</span>转封装为<span lang=EN-US>aac</span>分发给用户。</p>

<h4><a name="_Toc462219445"><span lang=EN-US>HTTP FLV Live Stream</span></a></h4>

<p><span lang=EN-US>SRS</span>支持将<span lang=EN-US>RTMP</span>流转封装为<span
lang=EN-US>HTTP flv</span>流，即在<span lang=EN-US>publish</span>发布<span
lang=EN-US>RTMP</span>流时，在<span lang=EN-US>SRS</span>的<span lang=EN-US>http</span>模块中挂载一个对应的<span
lang=EN-US>http</span>地址（根据配置），用户在访问这个<span lang=EN-US>http flv</span>文件时，从<span
lang=EN-US>rtmp</span>流转封装为<span lang=EN-US>flv</span>分发给用户</p>

<h5><span lang=EN-US>What is HTTP FLV</span></h5>

<p>所有的<span lang=EN-US>HTTP FLV</span>流都是一个<span lang=EN-US>HTTP FLV</span>地址，譬如：<code><span
lang=EN-US>http://ossrs.net:8081/live/livestream.flv</span></code>，但是，流的形式却至少有三种：</p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>FLV</span><span
     style='font-family:宋体'>文件，渐进式</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>流。放一个文件到</span><span lang=EN-US>nginx</span><span
     style='font-family:宋体'>目录，可以访问下载在播放器播放，这是</span><span lang=EN-US>HTTP FLV</span><span
     style='font-family:宋体'>文件，也就是渐进式下载流。所谓渐进式下载，也就是用户观看时无法从未下载的地方开始看。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>FLV</span><span
     style='font-family:宋体'>伪流。一般说的</span><span lang=EN-US>HTTP FLV</span><span
     style='font-family:宋体'>，比上面的渐进式流高级一点，譬如，一个</span><span lang=EN-US>120</span><span
     style='font-family:宋体'>分钟的电影，作为渐进式流播放时，用户需要从</span><span lang=EN-US>60</span><span
     style='font-family:宋体'>分钟开始看，如何支持呢？因为</span><span lang=EN-US>nginx</span><span
     style='font-family:宋体'>是当做文件</span> <span style='font-family:宋体'>下载的，无法直接跳转到第</span><span
     lang=EN-US>60</span><span style='font-family:宋体'>分钟（</span><span
     lang=EN-US>nginx</span><span style='font-family:宋体'>也不知道</span><span
     lang=EN-US>60</span><span style='font-family:宋体'>分钟对应的字节偏移是多少呀）。后来有人就支持这种跳着播放，通过指定时间服务器从指定的位置</span>
     <span style='font-family:宋体'>开始给流，这种支持</span><span lang=EN-US>flv?start=</span><span
     style='font-family:宋体'>，就是</span><span lang=EN-US>http flv</span><span
     style='font-family:宋体'>的伪流，本质上还是点播流。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>FLV</span><span
     style='font-family:宋体'>直播流。</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>所指的</span><span lang=EN-US>HTTP FLV</span><span
     style='font-family:宋体'>流，是严格意义上的直播流，有</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>的所有特征，譬如集群、低延迟、热备、</span><span lang=EN-US>GOP cache</span><span
     style='font-family:宋体'>，而且有</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>的优势，譬如</span><span lang=EN-US>302</span><span
     style='font-family:宋体'>、穿墙、通用。由于</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>内部实现了</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>服务器，所以</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>是在边缘将</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>流转换成</span><span lang=EN-US>HTTP </span><span
     style='font-family:宋体'>流，</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>集群内部还是使用</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>分发。当前唯一将</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>和</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>协议都解析的服务器，目前只有</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>和</span><span lang=EN-US>nginx-rtmp</span><span
     style='font-family:宋体'>，可惜</span><span lang=EN-US>nginx- rtmp</span><span
     style='font-family:宋体'>没有实现这个流。</span></li>
</ol>

<p>用一句话概括，<span lang=EN-US>SRS</span>的<span lang=EN-US>HTTP FLV</span>就是增强的<span
lang=EN-US>RTMP</span>，真正的实时流媒体分发。</p>

<h5><span lang=EN-US>Confuse HTTP FLV</span></h5>

<p><span lang=EN-US>SRS</span>的<span lang=EN-US>HTTP FLV</span>容易和下面的几种分发方式混淆：</p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>RTMPT</span><span
     style='font-family:宋体'>：这个实际上是最接近</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>HTTP FLV</span><span
     style='font-family:宋体'>的概念的。但是从本质上来讲，</span><span lang=EN-US>rtmpt</span><span
     style='font-family:宋体'>是基于</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>，所以还是</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>而不是</span><span lang=EN-US>FLV</span><span
     style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HDL/HFL</span><span
     style='font-family:宋体'>：国内一些厂家的</span><span lang=EN-US>HXX</span><span
     style='font-family:宋体'>流，就是</span><span lang=EN-US>FLV</span><span
     style='font-family:宋体'>流，主要和</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>的区别在于服务器集群内部</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>还是走</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>，所以延迟可能会有很大差异。</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>HTTP FLV</span><span
     style='font-family:宋体'>和</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>延迟一样，</span><span lang=EN-US>0.8-3</span><span
     style='font-family:宋体'>秒。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HDS</span><span
     style='font-family:宋体'>：这个差的太远了，不是一个东西。</span><span lang=EN-US>HDS</span><span
     style='font-family:宋体'>和</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>像，但是</span><span lang=EN-US>HTTP FLV</span><span
     style='font-family:宋体'>和他们两个都完全不像。</span></li>
</ol>

<h5><span lang=EN-US>Why HTTP FLV</span></h5>

<p>为何要整个<span lang=EN-US>HTTP FLV</span>出来呢？当下<span lang=EN-US>HTTP FLV</span>流正大行其道。主要的优势在于：</p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>互联网流媒体实时领域，还是</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>。</span><span
     lang=EN-US>HTTP-FLV</span><span style='font-family:宋体'>和</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>的延迟一样，因此可以满足延迟的要求。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>穿墙：很多防火墙会墙掉</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>，但是不会墙</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>，因此</span><span
     lang=EN-US>HTTP FLV</span><span style='font-family:宋体'>出现奇怪问题的概率很小。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>调度：</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>也有个</span><span
     lang=EN-US>302</span><span style='font-family:宋体'>，可惜是播放器</span><span
     lang=EN-US>as</span><span style='font-family:宋体'>中支持的，</span><span
     lang=EN-US>HTTP FLV</span><span style='font-family:宋体'>流就支持</span><span
     lang=EN-US>302</span><span style='font-family:宋体'>方便</span><span
     lang=EN-US>CDN</span><span style='font-family:宋体'>纠正</span><span
     lang=EN-US>DNS</span><span style='font-family:宋体'>的错误。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>容错：</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>的</span><span
     lang=EN-US>HTTP FLV</span><span style='font-family:宋体'>回源时可以回多个，和</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>一样，可以支持多级热备。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>通用：</span><span
     lang=EN-US>Flash</span><span style='font-family:宋体'>可以播</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>，也可以播</span><span
     lang=EN-US>HTTP FLV</span><span style='font-family:宋体'>。自己做的</span><span
     lang=EN-US>APP</span><span style='font-family:宋体'>，也都能支持。主流播放器也都支持</span><span
     lang=EN-US>http flv</span><span style='font-family:宋体'>的播放。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>简单：</span><span
     lang=EN-US>FLV</span><span style='font-family:宋体'>是最简单的流媒体封装，</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>是最广泛的协议，这两个到一起维护性很高，比</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>简单多了。</span></li>
</ol>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>Srs</span><span
style='font-family:宋体'>除了支持</span><span lang=EN-US>http-flv</span><span
style='font-family:宋体'>直播流外，现可以支持</span><span lang=EN-US>HTTP TS Live Stream</span><span
style='font-family:宋体'>，</span><span lang=EN-US>HTTP Mp3 Live Stream</span><span
style='font-family:宋体'>，</span><span lang=EN-US>HTTP Aac Live Stream</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>备注：若需要同时分发不同的</span><span
lang=EN-US>http live stream</span><span style='font-family:宋体'>，可以使用</span><span
lang=EN-US>forward</span><span style='font-family:宋体'>到其他</span><span
lang=EN-US>vhost</span><span style='font-family:宋体'>，不同的</span><span
lang=EN-US>vhost</span><span style='font-family:宋体'>配置不同的</span><span
lang=EN-US>http live stream</span><span style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>HSTRS(http
stream trigger rtmp source)</span><span style='font-family:宋体'>由</span><span
lang=EN-US>HTTP</span><span style='font-family:宋体'>流触发的</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>回源，该功能可以用于构建</span><span lang=EN-US>HTTP-FLV</span><span
style='font-family:宋体'>集群，即</span><span lang=EN-US>HTTP-FLV</span><span
style='font-family:宋体'>流的合并回源，以及</span><span lang=EN-US>HTTP-FLV</span><span
style='font-family:宋体'>在没有流时的等待</span><span lang=EN-US>standby</span><span
style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>HSTRS</span><span style='font-family:
宋体'>需要开启配置项</span><span lang=EN-US>http_remux</span><span style='font-family:
宋体'>的</span><span lang=EN-US>hstrs</span><span style='font-family:宋体'>，默认是开启的</span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;</span></p>

<h4><a name="_Toc462219446"><span style='font-family:宋体'>点播</span><span
lang=EN-US>FLV</span></a><span style='font-family:宋体'>流</span></h4>

<h5><span lang=EN-US>HTTP VOD</span></h5>

<p>推荐以下的方式：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>点播建议用</span><span
     lang=EN-US>http</span><span style='font-family:宋体'>分发，</span><span
     lang=EN-US>http</span><span style='font-family:宋体'>服务器一大堆。</span><span
     lang=EN-US> SRS</span><span style='font-family:宋体'>能将直播流录制为</span><span
     lang=EN-US>flv</span><span style='font-family:宋体'>文件，并且提供了一些工具来支持</span><span
     lang=EN-US>flv</span><span style='font-family:宋体'>点播流，</span> <span
     style='font-family:宋体'>但是应该使用其他的</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>服务器分发</span><span lang=EN-US>flv</span><span
     style='font-family:宋体'>文件。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>总之，</span><span
     lang=EN-US>srs</span><span style='font-family:宋体'>不支持点播，只支持直播。这是官方回答。</span></li>
</ul>

<p>点播<span lang=EN-US>FLV</span>流的主要流程是：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>服务器录制直播为</span><span
     lang=EN-US>FLV</span><span style='font-family:宋体'>文件，或者上传</span><span
     lang=EN-US>FLV</span><span style='font-family:宋体'>点播文件资源，到</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>的</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>根目录：</span><code><span
     lang=EN-US style='font-size:12.0pt'>objs/nginx/html</span></code><span
     lang=EN-US> </span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>服务器必须要支持</span><span lang=EN-US>flv</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>start=offset</span><span
     style='font-family:宋体'>，譬如</span><span lang=EN-US>nginx</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>flv</span><span
     style='font-family:宋体'>模块，或者</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>的实验性</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>服务器。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>使用</span><code><span
     lang=EN-US style='font-size:12.0pt'>research/librtmp/objs/srs_flv_injecter</span></code><span
     style='font-family:宋体'>将</span><span lang=EN-US>FLV</span><span
     style='font-family:宋体'>的时间和对于的</span><span lang=EN-US>offset</span><span
     style='font-family:宋体'>（文件偏移量）写入</span><span lang=EN-US>FLV</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>metadata</span><span
     style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>播放器请求</span><span
     lang=EN-US>FLV</span><span style='font-family:宋体'>文件，譬如：</span><code><span
     lang=EN-US style='font-size:12.0pt'>http://192.168.1.170:8080/sample.flv</span></code><span
     lang=EN-US> </span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>用户点击进度条进行</span><span
     lang=EN-US>SEEK</span><span style='font-family:宋体'>，譬如</span><span
     lang=EN-US>SEEK</span><span style='font-family:宋体'>到</span><span
     lang=EN-US>300</span><span style='font-family:宋体'>秒。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>播放器根据</span><span
     lang=EN-US>inject</span><span style='font-family:宋体'>的时间和</span><span
     lang=EN-US>offset</span><span style='font-family:宋体'>对应关系找出准确的关键帧的</span><span
     lang=EN-US>offset</span><span style='font-family:宋体'>。譬如：</span><span
     lang=EN-US>300</span><span style='font-family:宋体'>秒偏移是</span><code><span
     lang=EN-US style='font-size:12.0pt'>6638860</span></code><span lang=EN-US>
     </span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>根据</span><span
     lang=EN-US>offset</span><span style='font-family:宋体'>发起新请求：</span><code><span
     lang=EN-US style='font-size:12.0pt'>http://192.168.1.170:8080/sample.flv?start=6638860</span></code><span
     lang=EN-US> </span></li>
</ul>

<p>备注：<span lang=EN-US>SRS</span>还不支持限速，会以最快的速度将文件发给客户端。 备注：<span lang=EN-US>SRS</span>还提供了查看<span
lang=EN-US>FLV</span>文件内容的工具<code><span lang=EN-US>research/librtmp/objs/srs_flv_parser</span></code>，可以看到<span
lang=EN-US>metadata</span>和每个<span lang=EN-US>tag</span>信息。</p>

<h4><a name="_Toc462219447"><span lang=EN-US>SRS Embeded HTTP server</span></a></h4>

<p class=MsoNoSpacing><span lang=EN-US>SRS</span><span style='font-family:宋体'>支持</span><span
lang=EN-US>http-api</span><span style='font-family:宋体'>，因此也能解析</span><span
lang=EN-US>HTTP</span><span style='font-family:宋体'>协议（目前是部分支持），所以也实现了一个简单的</span><span
lang=EN-US>HTTP</span><span style='font-family:宋体'>服务器。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>SRS</span><span style='font-family:宋体'>的</span><span
lang=EN-US>HTTP</span><span style='font-family:宋体'>服务器已经重写，稳定可以商用。</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>对于一些嵌入式设备，并发也不高时，可以考虑使用</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>的</span><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>服务器分发</span><span lang=EN-US>HLS</span><span
style='font-family:宋体'>，这样比较简单。</span></p>

<h4><a name="_Toc462219448"><span lang=EN-US>Wiki</span></a></h4>

<p class=MsoNormal><span lang=EN-US>&nbsp;<a
href="https://github.com/ossrs/srs/wiki/v2_CN_DeliveryHttpStream">https://github.com/ossrs/srs/wiki/v2_CN_DeliveryHttpStream</a></span></p>

<h3><a name="_Toc26097956"></a><a name="_Toc462219449"></a><a
name="_Toc456260517"><span style='font-family:宋体'>转封装成</span><span lang=EN-US>HLS</span></a></h3>

<p class=MsoNoSpacing><span lang=EN-US>SRS</span><span style='font-family:宋体'>支持</span><span
lang=EN-US>HLS/RTMP</span><span style='font-family:宋体'>两种成熟而且广泛应用的流媒体分发方式。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>RTMP</span><span style='font-family:
宋体'>指</span><span lang=EN-US>Adobe</span><span style='font-family:宋体'>的</span><span
lang=EN-US>RTMP(Realtime Message Protocol)</span><span style='font-family:宋体'>，广泛应用于低延时直播，也是编码器和服务器对接的实际标准协议，在</span><span
lang=EN-US>PC</span><span style='font-family:宋体'>（</span><span lang=EN-US>Flash</span><span
style='font-family:宋体'>）上有最佳观看体验和最佳稳定性。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>HLS</span><span style='font-family:宋体'>指</span><span
lang=EN-US>Apple</span><span style='font-family:宋体'>的</span><span lang=EN-US>HLS(Http
Live Streaming)</span><span style='font-family:宋体'>，本身就是</span><span
lang=EN-US>Live</span><span style='font-family:宋体'>（直播）的，不过</span><span
lang=EN-US>Vod</span><span style='font-family:宋体'>（点播）也能支持。</span><span
lang=EN-US>HLS</span><span style='font-family:宋体'>是</span><span lang=EN-US>Apple</span><span
style='font-family:宋体'>平台的标准流媒体协议，和</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>在</span><span lang=EN-US>PC</span><span
style='font-family:宋体'>上一样支持得天衣无缝。</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-family:宋体'>HLS</span><span style='font-family:宋体'>主要的应用场景包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>跨平台：<span
     lang=EN-US>PC</span>主要的直播方案是<span lang=EN-US>RTMP</span>，也有一些库能播放<span
     lang=EN-US>HLS</span>，譬如<span lang=EN-US>jwplayer</span>，基于<span
     lang=EN-US>osmf</span>的<span lang=EN-US>hls</span>插件也一大堆。所以实际上如果选一种协议能跨<span
     lang=EN-US>PC/Android/IOS</span>，那就是<span lang=EN-US>HLS</span>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-family:
     宋体'>IOS</span><span style='font-family:宋体'>上苛刻的稳定性要求：<span lang=EN-US>IOS</span>上最稳定的当然是<span
     lang=EN-US>HLS</span>，稳定性不差于<span lang=EN-US>RTMP</span>在<span lang=EN-US>PC-flash</span>上的表现。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>友好的<span
     lang=EN-US>CDN</span>分发方式：目前<span lang=EN-US>CDN</span>对于<span lang=EN-US>RTMP</span>也是基本协议，但是<span
     lang=EN-US>HLS</span>分发的基础是<span lang=EN-US>HTTP</span>，所以<span
     lang=EN-US>CDN</span>的接入和分发会比<span lang=EN-US>RTMP</span>更加完善。能在各种<span
     lang=EN-US>CDN</span>之间切换，<span lang=EN-US>RTMP</span>也能，只是可能需要对接测试。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>简单：<span
     lang=EN-US>HLS</span>作为流媒体协议非常简单，<span lang=EN-US>apple</span>支持得也很完善。<span
     lang=EN-US>Android</span>对<span lang=EN-US>HLS</span>的支持也会越来越完善。至于<span
     lang=EN-US>DASH/HDS</span>，好像没有什么特别的理由，就像<span lang=EN-US>linux</span>已经大行其道而且开放，其他的系统很难再广泛应用。</span></li>
</ul>

<p class=MsoNormal align=left style='text-align:left'><span style='font-family:
宋体'>总之，<span lang=EN-US>SRS</span>支持<span lang=EN-US>HLS</span>主要是作为输出的分发协议，直播以<span
lang=EN-US>RTMP+HLS</span>分发，满总各种应用场景。点播以<span lang=EN-US>HLS</span>为主。</span></p>

<h4><a name="_Toc462219450"><span style='font-family:宋体'>各种分发流协议介绍</span></a></h4>

<table class=MsoNormalTable border=0 cellpadding=0 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=48 style='width:35.95pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体'>分发</span></b></p>
   </td>
   <td width=69 style='width:51.75pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>平台</span></b></p>
   </td>
   <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>协议</span></b></p>
   </td>
   <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>公司</span></b></p>
   </td>
   <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>说明</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=48 style='width:35.95pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>RTMP</span></p>
  </td>
  <td width=69 style='width:51.75pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Windows Flash</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>RTMP</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Adobe</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>主流的低延时分发方式，</span><span
  lang=EN-US style='color:black'><br>
  Adobe</span><span style='font-family:宋体;color:black'>对</span><span
  lang=EN-US style='color:black'>RTMP</span><span style='font-family:宋体;
  color:black'>是</span><span lang=EN-US style='color:black'>Flash</span><span
  style='font-family:宋体;color:black'>原生支持方式，</span><span lang=EN-US
  style='color:black'><br>
  FMS</span><span style='font-family:宋体;color:black'>（</span><span lang=EN-US
  style='color:black'>Adobe Media Server</span><span style='font-family:宋体;
  color:black'>前身），</span><span lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>就是</span><span lang=EN-US
  style='color:black'>Flash Media Server</span><span style='font-family:宋体;
  color:black'>的简写，可见</span><span lang=EN-US style='color:black'>Flash</span><span
  style='font-family:宋体;color:black'>播放</span><span lang=EN-US
  style='color:black'>RTMP</span><span style='font-family:宋体;color:black'>是多么</span><span
  lang=EN-US style='color:black'>“</span><span style='font-family:宋体;
  color:black'>原生</span><span lang=EN-US style='color:black'>”</span><span
  style='font-family:宋体;color:black'>，</span><span lang=EN-US style='color:
  black'><br>
  </span><span style='font-family:宋体;color:black'>就像浏览器打开</span><span
  lang=EN-US style='color:black'>http</span><span style='font-family:宋体;
  color:black'>网页一样</span><span lang=EN-US style='color:black'>“</span><span
  style='font-family:宋体;color:black'>原生</span><span lang=EN-US
  style='color:black'>”</span><span style='font-family:宋体;color:black'>，</span><span
  lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>经测试，</span><span lang=EN-US
  style='color:black'>Flash</span><span style='font-family:宋体;color:black'>播放</span><span
  lang=EN-US style='color:black'>RTMP</span><span style='font-family:宋体;
  color:black'>流可以</span><span lang=EN-US style='color:black'>10</span><span
  style='font-family:宋体;color:black'>天以上不间断播放。</span></p>
  </td>
 </tr>
 <tr>
  <td width=48 style='width:35.95pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HLS</span></p>
  </td>
  <td width=69 style='width:51.75pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Apple/<br>
  Android</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HTTP</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Apple/<br>
  Google</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>延时一个切片以上（一般</span><span
  lang=EN-US style='color:black'>10</span><span style='font-family:宋体;
  color:black'>秒以上），</span><span lang=EN-US style='color:black'><br>
  Apple</span><span style='font-family:宋体;color:black'>平台上</span><span
  lang=EN-US style='color:black'>HLS</span><span style='font-family:宋体;
  color:black'>的效果比</span><span lang=EN-US style='color:black'>PC</span><span
  style='font-family:宋体;color:black'>的</span><span lang=EN-US style='color:
  black'>RTMP</span><span style='font-family:宋体;color:black'>还要好，</span><span
  lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>而且</span><span lang=EN-US
  style='color:black'>Apple</span><span style='font-family:宋体;color:black'>所有设备都支持，</span><span
  lang=EN-US style='color:black'><br>
  Android</span><span style='font-family:宋体;color:black'>最初不支持</span><span
  lang=EN-US style='color:black'>HLS</span><span style='font-family:宋体;
  color:black'>，后来也支持了，</span><span lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>但测试发现支持得还不如</span><span
  lang=EN-US style='color:black'>Apple</span><span style='font-family:宋体;
  color:black'>，</span><span lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>不过观看是没有问题，稳定性稍差，</span><span
  lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>所以有些公司专门做</span><span
  lang=EN-US style='color:black'>Android</span><span style='font-family:宋体;
  color:black'>上的流媒体播放器。</span></p>
  </td>
 </tr>
 <tr>
  <td width=48 style='width:35.95pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HDS</span></p>
  </td>
  <td width=69 style='width:51.75pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>-</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HTTP</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Adobe</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Adobe</span><span
  style='font-family:宋体;color:black'>自己的</span><span lang=EN-US
  style='color:black'>HLS</span><span style='font-family:宋体;color:black'>，</span><span
  lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>协议方面做得是复杂而且没有什么好处，</span><span
  lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>国内没有什么应用，传说国外有，</span><span
  lang=EN-US style='color:black'><br>
  SRS2.0</span><span style='font-family:宋体;color:black'>以后已经支持。</span></p>
  </td>
 </tr>
 <tr>
  <td width=48 style='width:35.95pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'><a
  href="http://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP">DASH</a></span></p>
  </td>
  <td width=69 style='width:51.75pt;background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>-</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HTTP</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>-</span></p>
  </td>
  <td style='background:#8DB3E2;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Dynamic Adaptive
  Streaming over HTTP (DASH)</span><span style='font-family:宋体;color:black'>，</span><span
  lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>一些公司提出的</span><span
  lang=EN-US style='color:black'>HLS</span><span style='font-family:宋体;
  color:black'>，</span><span lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>国内还没有应用，国外据说有用了，</span><span
  lang=EN-US style='color:black'><br>
  nginx-rtmp</span><span style='font-family:宋体;color:black'>好像已经支持了，</span><span
  lang=EN-US style='color:black'><br>
  </span><span style='font-family:宋体;color:black'>明显这个还不成熟。</span></p>
  </td>
 </tr>
</table>

<h4><a name="_Toc462219451"><span lang=EN-US>HLS Introduction</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>HLS</span><span style='font-size:
10.5pt'>是提供一个<span lang=EN-US>m3u8</span>地址，<span lang=EN-US>Apple</span>的<span
lang=EN-US>Safari</span>浏览器直接就能打开<span lang=EN-US>m3u8</span>地址，譬如：</span></p>

<pre><span lang=EN-US style='font-size:10.5pt'>http://demo.srs.com/live/livestream.m3u8</span></pre>

<p><span lang=EN-US style='font-size:10.5pt'>Android</span><span
style='font-size:10.5pt'>不能直接打开，需要使用<span lang=EN-US>html5</span>的<span
lang=EN-US>video</span>标签，然后在浏览器中打开这个页面即可，譬如：</span></p>

<pre><span class=pl-c><span lang=EN-US style='font-size:10.5pt'>&lt;!-- livestream.html --&gt;</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&lt;<span class=pl-ent>video</span> <span
class=pl-e>width</span>=<span class=pl-pds>&quot;</span><span class=pl-s>640</span><span
class=pl-pds>&quot;</span> <span class=pl-e>height</span>=<span class=pl-pds>&quot;</span><span
class=pl-s>360</span><span class=pl-pds>&quot;</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-e>autoplay</span> <span class=pl-e>controls</span> <span class=pl-e>autobuffer</span> </span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span
class=pl-e>src</span>=<span class=pl-pds>&quot;</span><span class=pl-s>http://demo.srs.com/live/livestream.m3u8</span><span
class=pl-pds>&quot;</span></span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-e>type</span>=<span
class=pl-pds>&quot;</span><span class=pl-s>application/vnd.apple.mpegurl</span><span
class=pl-pds>&quot;</span>&gt;</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>&lt;/<span class=pl-ent>video</span>&gt;</span></pre>

<p><span lang=EN-US style='font-size:10.5pt'>HLS</span><span style='font-size:
10.5pt'>的</span><span lang=EN-US><a
href="https://github.com/ossrs/srs/blob/master/trunk/doc/hls-m3u8-draft-pantos-http-live-streaming-12.txt"><span
style='font-size:10.5pt'>m3u8</span></a></span><span style='font-size:10.5pt'>，是一个<span
lang=EN-US>ts</span>的列表，也就是告诉浏览器可以播放这些<span lang=EN-US>ts</span>文件，譬如：</span></p>

<pre><span class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXTM3U</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXT-X-VERSION:3</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXT-X-MEDIA-SEQUENCE:64</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXT-X-TARGETDURATION:12</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXTINF:11.550</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>livestream-64.ts</span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXTINF:5.250</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>livestream-65.ts</span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXTINF:7.700</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>livestream-66.ts</span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:10.5pt'>#EXTINF:6.850</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>livestream-67.ts</span></pre>

<p><span style='font-size:10.5pt'>有几个关键的参数，这些参数在<span lang=EN-US>SRS</span>的配置文件中都有配置项：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>EXT-X-TARGETDURATION</span><span
     style='font-family:宋体'>：所有切片的最大时长。有些</span><span lang=EN-US>Apple</span><span
     style='font-family:宋体'>设备这个参数不正确会无法播放。</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>会自动计算出</span><span lang=EN-US>ts</span><span
     style='font-family:宋体'>文件的最大时长，然后更新</span><span lang=EN-US>m3u8</span><span
     style='font-family:宋体'>时会自动更新这个值。用户不必自己配置。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>EXTINF</span><span
     style='font-family:宋体'>：</span><span lang=EN-US>ts</span><span
     style='font-family:宋体'>切片的实际时长，</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>提供配置项</span><span lang=EN-US>hls_fragment</span><span
     style='font-family:宋体'>，但实际上的</span><span lang=EN-US>ts</span><span
     style='font-family:宋体'>时长还受</span><span lang=EN-US>gop</span><span
     style='font-family:宋体'>影响，详见下面配置</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>的说明。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>ts</span><span
     style='font-family:宋体'>文件的数目：</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>可配置</span><span lang=EN-US>hls_window</span><span
     style='font-family:宋体'>，指定</span><span lang=EN-US>m3u8</span><span
     style='font-family:宋体'>中保存多少个切片，</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>会自动清理旧的切片。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>livestream-67.ts</span><span
     style='font-family:宋体'>：</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>会自动维护</span><span lang=EN-US>ts</span><span
     style='font-family:宋体'>切片的文件名，在编码器重推之后，这个编号会继续增长，保证流的连续性。直到</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>重启，这个编号才重置为</span><span
     lang=EN-US>0</span><span style='font-family:宋体'>。</span></li>
</ul>

<p><span style='font-size:10.5pt'>譬如，每个<span lang=EN-US>ts</span>切片为<span
lang=EN-US>10</span>秒，窗口为<span lang=EN-US>60</span>秒，那么<span lang=EN-US>m3u8</span>中会保存<span
lang=EN-US>6</span>个<span lang=EN-US>ts</span>切片。</span></p>

<h4><a name="_Toc462219452"><span lang=EN-US>HLS Workflow</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>HLS</span><span style='font-size:
10.5pt'>的主要流程是：</span></p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>FFMPEG</span><span
     style='font-family:宋体'>或</span><span lang=EN-US>FMLE</span><span
     style='font-family:宋体'>或编码器，推送</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>流到</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>，编码为</span><span lang=EN-US>H264/AAC</span><span
     style='font-family:宋体'>（其他编码需要</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>转码）</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>将</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>切片成</span><span lang=EN-US>TS</span><span
     style='font-family:宋体'>，并生成</span><span lang=EN-US>M3U8</span><span
     style='font-family:宋体'>。若流非</span><span lang=EN-US>H264</span><span
     style='font-family:宋体'>和</span><span lang=EN-US>AAC</span><span
     style='font-family:宋体'>，则停止输出</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>（可使用</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>转码到</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>其他</span><span lang=EN-US>vhost</span><span
     style='font-family:宋体'>或流，然后再切</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>）。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>访问</span><span
     lang=EN-US>m3u8</span><span style='font-family:宋体'>，</span><span
     lang=EN-US>srs</span><span style='font-family:宋体'>内置的</span><span
     lang=EN-US>http</span><span style='font-family:宋体'>服务器（或者通用</span><span
     lang=EN-US>http</span><span style='font-family:宋体'>服务器）提供</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>服务。</span></li>
</ol>

<p><span style='font-size:10.5pt'>注意：<span lang=EN-US>SRS</span>只需要在<span
lang=EN-US>Vhost</span>上配置<span lang=EN-US>HLS</span>，会自动根据流的<span lang=EN-US>app</span>创建目录，但是配置的<span
lang=EN-US>hls_path</span>必须自己创建</span></p>

<h4><a name="_Toc462219453"><span lang=EN-US>Wiki</span></a></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_DeliveryHLS">https://github.com/ossrs/srs/wiki/v1_CN_DeliveryHLS</a></span></p>

<h4><a name="_Toc462219454"><span style='font-family:宋体'>补充</span><span
lang=EN-US>:</span></a><span style='font-family:宋体'>直播时移</span></h4>

<p class=MsoNormal style='text-indent:15.75pt'><span style='font-family:宋体'>使用</span><span
lang=EN-US>hls</span><span style='font-family:宋体'>可以实现时移回看功能。时移回看功能实际</span><span
lang=EN-US>m3u8</span><span style='font-family:宋体'>文件还是按直播的方式，只不过里面的</span><span
lang=EN-US>ts</span><span style='font-family:宋体'>片段播放列表，不是从直播实时流生成，而是从历史</span><span
lang=EN-US>ts</span><span style='font-family:宋体'>文件中来生成播放列表。直播生成的</span><span
lang=EN-US>ts</span><span style='font-family:宋体'>片段，需要按时间目录存放，比如</span><span
lang=EN-US>2016071209</span><span style='font-family:宋体'>目录存放</span><span
lang=EN-US>9</span><span style='font-family:宋体'>点内生成所有</span><span lang=EN-US>ts</span><span
style='font-family:宋体'>片段，</span><span lang=EN-US>ts</span><span
style='font-family:宋体'>文件需要按格式</span><span lang=EN-US>:</span><span
style='font-family:宋体'>“时间戳</span><span lang=EN-US>_Ts</span><span
style='font-family:宋体'>片长</span><span lang=EN-US>.ts”</span><span
style='font-family:宋体'>来存放。时移回看时根据指定时间搜索</span><span lang=EN-US>ts</span><span
style='font-family:宋体'>文件片段，生成直播</span><span lang=EN-US>m3u8</span><span
style='font-family:宋体'>文件。</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>可以使用</span><span lang=EN-US>on_hls</span><span
style='font-family:宋体'>事件来对直播流生成</span><span lang=EN-US>ts</span><span
style='font-family:宋体'>文件按时间目录下转存，也可以通进脚本解析</span><span lang=EN-US>srs</span><span
style='font-family:宋体'>生成的直播</span><span lang=EN-US>m3u8</span><span
style='font-family:宋体'>文件来转存</span><span lang=EN-US>ts</span><span
style='font-family:宋体'>片段。后一种方法也可以适用于</span><span lang=EN-US>nginx rtmp </span><span
style='font-family:宋体'>的</span><span lang=EN-US>hls</span><span
style='font-family:宋体'>中。</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span style='font-family:宋体'>通过直播时移，用户可以随时回到当前时间点之前的任意时间点开始回看。回看的时间可以根据自己需求来定，可以一天，七天，一个月等。</span></p>

<p class=MsoNormal style='text-indent:15.75pt'><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097957"></a><a name="_Toc462219455"></a><a
name="_Toc456260518"><span style='font-family:宋体'>转封装成</span><span lang=EN-US>HDS</span></a></h3>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>HDS</span><span
style='font-family:宋体;color:#333333'>指</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>Adobe</span><span style='font-family:宋体;
color:#333333'>的</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>Http Dynamic Stream</span><span style='font-family:宋体;
color:#333333'>，和</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>Apple</span><span style='font-family:宋体;color:#333333'>的</span><span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v2_CN_DeliveryHLS"><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#4078C0;text-decoration:
none'>HLS</span></a></span><span style='font-family:宋体;color:#333333'>类似。</span></p>

<h4><span lang=EN>&nbsp;<a name="_Toc462219456">Wiki</a></span></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v2_CN_DeliveryHDS"><span lang=EN
style='font-family:"Segoe UI",sans-serif'>https://github.com/ossrs/srs/wiki/v2_CN_DeliveryHDS</span></a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097958"></a><a name="_Toc462219457"></a><a
name="_Toc456260519"><span style='font-family:宋体'>录制成</span><span lang=EN-US>FLV</span></a></h3>

<p class=MsoNoSpacing style='text-indent:15.75pt'><span lang=EN>SRS</span><span
style='font-family:宋体'>可以将</span><span lang=EN>RTMP</span><span
style='font-family:宋体'>流录制成</span><span lang=EN>flv</span><span
style='font-family:宋体'>文件。</span></p>

<p class=MsoNoSpacing style='text-indent:15.75pt'><span lang=EN>DVR</span><span
style='font-family:宋体'>的计划即决定什么时候关闭</span><span lang=EN>flv</span><span
style='font-family:宋体'>文件，打开新的</span><span lang=EN>flv</span><span
style='font-family:宋体'>文件，主要的录制计划包括：</span></p>

<p class=MsoNoSpacing style='text-indent:31.6pt'><b><span lang=EN>session</span></b><b><span
style='font-family:宋体'>：</span></b><span style='font-family:宋体'>按照</span><span
lang=EN>session</span><span style='font-family:宋体'>来关闭</span><span lang=EN>flv</span><span
style='font-family:宋体'>文件，即编码器停止推流时关闭</span><span lang=EN>flv</span><span
style='font-family:宋体'>，整个</span><span lang=EN>session</span><span
style='font-family:宋体'>录制为一个</span><span lang=EN>flv</span><span
style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:31.6pt'><b><span lang=EN>segment</span></b><b><span
style='font-family:宋体'>：</span></b><span style='font-family:宋体'>按照时间分段录制，</span><span
lang=EN>flv</span><span style='font-family:宋体'>文件时长配置为</span><span lang=EN>dvr_duration</span><span
style='font-family:宋体'>和</span><span lang=EN>dvr_wait_keyframe</span><span
style='font-family:宋体'>。注意：若不按关键帧切</span><span lang=EN>flv</span><span
style='font-family:宋体'>（即</span><span lang=EN>dvr_wait_keyframe</span><span
style='font-family:宋体'>配置为</span><span lang=EN>off</span><span
style='font-family:宋体'>），所以会导致后面的</span><span lang=EN>flv</span><span
style='font-family:宋体'>启动时会花屏。</span></p>

<p class=MsoNoSpacing style='text-indent:31.6pt'><b><span lang=EN>time_jitter: </span></b><span
style='font-family:宋体'>时间戳抖动算法。</span><span lang=EN>full</span><span
style='font-family:宋体'>使用完全的时间戳矫正；</span><span lang=EN>zero</span><span
style='font-family:宋体'>只是保证从</span><span lang=EN>0</span><span
style='font-family:宋体'>开始；</span><span lang=EN>off</span><span
style='font-family:宋体'>不矫正时间戳。</span></p>

<p class=MsoNoSpacing style='text-indent:31.6pt'><b><span lang=EN>dvr_path:</span></b><span
lang=EN> </span><span style='font-family:宋体'>录制的路径，</span><span
style='font-family:宋体'>规则如下：</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>按年月日以及流信息生成子目录。便于做软链，或者避免一个目录的文件太多（貌似超过几万<span
lang=EN-US>linux</span>会支持不了）。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US
style='font-family:宋体'>1.</span><span style='font-family:宋体'>按日期和时间以及流信息生成文件名。便于搜索。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US
style='font-family:宋体'>2.</span><span style='font-family:宋体'>提供日期和时间，以及流信息的变量，以中括号代表变量。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US
style='font-family:宋体'>3.</span><span style='font-family:宋体'>保留目前的方式，按照时间戳生成文件名，保存在一个文件夹。若没有指定文件名（只指定了目录），则默认使用<span
lang=EN-US>[stream].[timestamp].flv</span>作为文件名，和目前保持一致。</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>DVR</span><span
style='font-family:宋体'>的</span><span lang=EN-US>apply</span><span
style='font-family:宋体'>决定了是否对某个流开启</span><span lang=EN-US>dvr</span><span
style='font-family:宋体'>，默认的</span><span lang=EN-US>all</span><span
style='font-family:宋体'>是对所有开启。</span> <span style='font-family:宋体'>这个功能是</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>实现</span><span lang=EN-US>nginx</span><span
style='font-family:宋体'>提供的</span><span lang=EN-US>control module</span><span
style='font-family:宋体'>的一个基础，而且更丰富。</span> <span style='font-family:宋体'>也就是可以支持用户调用</span><span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi">http raw
api</a></span><span style='font-family:宋体'>控制是否以及何时</span><span lang=EN-US>DVR</span><span
style='font-family:宋体'>。</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>&nbsp;</span></p>

<h4><a name="_Toc462219458"><span lang=EN>Wiki</span></a></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_DVR"><span lang=EN
style='font-family:"Segoe UI",sans-serif'>https://github.com/ossrs/srs/wiki/v3_CN_DVR</span></a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097959"></a><a name="_Toc462219459"></a><a
name="_Toc456260520"><span style='font-family:宋体'>分发方式比较</span></a></h3>

<p style='text-indent:21.0pt'><span style='font-size:10.5pt'>互联网上的两种主要的分发方式：</span><span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_DeliveryHLS"><span
style='font-size:10.5pt'>HLS</span></a></span><span style='font-size:10.5pt'>和</span><span
lang=EN-US><a href="https://github.com/ossrs/srs/wiki/v1_CN_DeliveryRTMP"><span
style='font-size:10.5pt'>RTMP</span></a></span><span style='font-size:10.5pt'>，什么时候用谁，完全决定于应用场景。还有其他的分发方式，这些分发方式不属于互联网常见和通用的方式，不予以比较：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>UDP</span><span
     style='font-family:宋体'>：譬如</span><span lang=EN-US>YY</span><span
     style='font-family:宋体'>的实时应用，视频会议等等，或者</span><span lang=EN-US>RTSP</span><span
     style='font-family:宋体'>之类。这类应用的特点就是实时性要求特别高，以毫秒计算。</span><span lang=EN-US>TCP</span><span
     style='font-family:宋体'>家族协议根本就满足不了要求，所以</span><span lang=EN-US>HTTP/TCP</span><span
     style='font-family:宋体'>都不靠谱。这类应用没有通用的方案，必须自己实现分发（服务端）和播放（客户端）。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>P2P</span><span
     style='font-family:宋体'>：譬如</span><span lang=EN-US>RTMFP</span><span
     style='font-family:宋体'>或者各家自己的协议。这类应用的特点是节省带宽。目前</span><span lang=EN-US>PC/flash</span><span
     style='font-family:宋体'>上的</span><span lang=EN-US>RTMFP</span><span
     style='font-family:宋体'>比较成熟，</span><span lang=EN-US>Android</span><span
     style='font-family:宋体'>上的</span><span lang=EN-US>P2P</span><span
     style='font-family:宋体'>属于起步群雄纷争标准不一，</span><span lang=EN-US>IOS</span><span
     style='font-family:宋体'>上</span><span lang=EN-US>P2P</span><span
     style='font-family:宋体'>应该没有听说过。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>RTSP</span><span
     style='font-family:宋体'>：这种不是互联网上的主要应用，在其他领域譬如安防等有广泛应用。</span></li>
</ul>

<p><span style='font-size:10.5pt'>另外，<span lang=EN-US>HTTP</span>的也分为几种：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HTTP progressive</span><span
     style='font-family:宋体'>：早期流媒体服务器分发</span><span lang=EN-US>http</span><span
     style='font-family:宋体'>文件时，以普通的</span><span lang=EN-US>http</span><span
     style='font-family:宋体'>文件分发，这种叫做渐进式下载，意思就是如果文件很大譬如</span><span lang=EN-US>1</span><span
     style='font-family:宋体'>小时时长</span><span lang=EN-US> 1GB</span><span
     style='font-family:宋体'>大小，想从中间开始播放是不行的。但这种方式已经是作古了，很多</span><span
     lang=EN-US>http</span><span style='font-family:宋体'>服务器支持</span><span
     lang=EN-US>http</span><span style='font-family:宋体'>文件的</span><span
     lang=EN-US>seek</span><span style='font-family:宋体'>，就是从中间开始播放。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HTTP stream</span><span
     style='font-family:宋体'>：支持</span><span lang=EN-US>seek</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>流，譬如各家视频网站的点播分发方式。或者稍微复杂点的，譬如把一个大文件切几段之后分发。目前在</span><span
     lang=EN-US>pc/flash</span><span style='font-family:宋体'>上点播国内的主流分发是这种方式。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>：这种是现在适配方式最广（除了</span><span lang=EN-US>flash, </span><span
     style='font-family:宋体'>需要额外的</span><span lang=EN-US>as</span><span
     style='font-family:宋体'>库支持），在</span><span lang=EN-US>PC</span><span
     style='font-family:宋体'>上有</span><span lang=EN-US>vlc</span><span
     style='font-family:宋体'>，</span><span lang=EN-US>Android/IOS</span><span
     style='font-family:宋体'>原生播放器就支持播放</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>，</span><span lang=EN-US>HTML5</span><span
     style='font-family:宋体'>里面的</span><span lang=EN-US>url</span><span
     style='font-family:宋体'>可以写</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>地址。总之，在移动端是以</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>为主。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HDS</span><span
     style='font-family:宋体'>：</span><span lang=EN-US>adobe</span><span
     style='font-family:宋体'>自己的</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>DASH</span><span
     style='font-family:宋体'>：各家提出的</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>，目前还没有广泛应用。</span></li>
</ul>

<p><span style='font-size:10.5pt'>对比以下互联网上用的流媒体分发方式：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>：</span><span lang=EN-US>apple</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>，支持点播和直播。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>：即</span><span lang=EN-US>HTTP stream</span><span
     style='font-family:宋体'>，各家自己定义的</span><span lang=EN-US>http</span><span
     style='font-family:宋体'>流，应用于国内点播视频网站。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>：直播应用，对实时性有一定要求，以</span><span lang=EN-US>PC</span><span
     style='font-family:宋体'>为主。</span></li>
</ul>

<h4><a name="_Toc462219460"><span lang=EN-US>RTMP</span></a></h4>

<p><span lang=EN-US>RTMP</span>本质上是流协议，主要的优势是：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>实时性高：</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>的实时性在</span><span
     lang=EN-US>3</span><span style='font-family:宋体'>秒之内，经过多层</span><span
     lang=EN-US>CDN</span><span style='font-family:宋体'>节点分发后，实时性也在</span><span
     lang=EN-US>3</span><span style='font-family:宋体'>秒左右。在一些实时性有要求的应用中以</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>为主。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>支持加密：</span><span
     lang=EN-US>RTMPE</span><span style='font-family:宋体'>和</span><span
     lang=EN-US>RTMPS</span><span style='font-family:宋体'>为加密协议。虽然</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>也有加密，但在</span><span
     lang=EN-US>PC</span><span style='font-family:宋体'>平台上</span><span
     lang=EN-US>flash</span><span style='font-family:宋体'>对</span><span
     lang=EN-US>RTMPE/RTMPS</span><span style='font-family:宋体'>支持应该比较不错。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>稳定性高：在</span><span
     lang=EN-US>PC</span><span style='font-family:宋体'>平台上</span><span
     lang=EN-US>flash</span><span style='font-family:宋体'>播放的最稳定方式是</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>，如果做</span><span
     lang=EN-US>CDN</span><span style='font-family:宋体'>或者大中型集群分发，选择稳定性高的协议一定是必要的。</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>也很稳定，但</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>是在协议上稳定；稳定性不只是服务端的事情，在集群分发，服务器管理，主备切换，客户端的支持上，</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>在</span><span
     lang=EN-US>PC</span><span style='font-family:宋体'>分发这种方式上还是很有优势。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>编码器接入：编码器输出到互联网（还可以输出为</span><span
     lang=EN-US>udp</span><span style='font-family:宋体'>组播之类广电应用），主要是</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>。譬如专业编码器，或者</span><span
     lang=EN-US>flash</span><span style='font-family:宋体'>网页编码器，或者</span><span
     lang=EN-US>FMLE</span><span style='font-family:宋体'>，或者</span><span
     lang=EN-US>ffmpeg</span><span style='font-family:宋体'>，都支持</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>输出。若需要接入多种设备，譬如提供云服务；或者希望网页直接采集摄像头；或者能在不同编码器之间切换，那么</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>作为服务器的输入协议会是最好的选择。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>系统容错：容错有很多种级别，</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>的集群实现时可以指定</span><span
     lang=EN-US>N</span><span style='font-family:宋体'>上层，在错误时切换不会影响到下层或者客户端，另外</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>的流没有标识，切到其他的服务器的流也可以继续播放。</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>的流热备切换没有这么容易。若对于直播的容错要求高，譬如降低出问题的概率，选择</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>会是很好的选择。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>可监控：在监控系统或者运维系统的角度看，流协议应该比较合适监控。</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>的流监控感觉没有那么完善。这个不算绝对优势，但比较有利。</span></li>
</ul>

<p><span lang=EN-US>RTMP</span>的劣势是：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>协议复杂：</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>协议比起</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>复杂很多，导致性能低下。测试发现两台服务器直连</span><span
     lang=EN-US>100Gbps</span><span style='font-family:宋体'>网络中，</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>能跑到</span><span
     lang=EN-US>60Gbps</span><span style='font-family:宋体'>，但是</span><span
     lang=EN-US> RTMP</span><span style='font-family:宋体'>只能跑到</span><span
     lang=EN-US>10Gbps</span><span style='font-family:宋体'>，</span><span
     lang=EN-US>CPU</span><span style='font-family:宋体'>占用率</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>要高很多。复杂协议导致在研发，扩展，维护软件系统时都没有</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>那么方便，所以</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>服务器现在大行其道，</span><span
     lang=EN-US>apache/nginx/tomcat</span><span style='font-family:宋体'>，</span><span
     lang=EN-US>N</span><span style='font-family:宋体'>多</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>服务器；而</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>协议虽然早就公开，但是真正在大规模中分发表现良好的没有，</span><span
     lang=EN-US>adobe</span><span style='font-family:宋体'>自己的</span><span
     lang=EN-US>FMS</span><span style='font-family:宋体'>在</span><span
     lang=EN-US>CDN</span><span style='font-family:宋体'>中都经常出问题。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>Cache</span><span
     style='font-family:宋体'>麻烦：流协议做缓存不方便。譬如点播，若做</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>流协议，边缘缓存</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>会很麻烦。如果是</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>，缓存其实也很麻烦，但是</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>服务器的缓存已经做了很久，所以只需要使用就好。这是为何点播都走</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>的原因。</span></li>
</ul>

<h4><a name="_Toc462219461"><span lang=EN-US>HTTP</span></a></h4>

<p><span lang=EN-US>HTTP</span>说的是<span lang=EN-US>HTTP</span>流，譬如各大视频网站的点播流。</p>

<p><span lang=EN-US>HTTP</span>本质上还是文件分发，主要的优势是：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>性能很高：</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>的性能没得说，协议简单，各种</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>高性能服务器也完善。如果分发的量特别大，譬如点播视频网站，没有直播的实时性要求，</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>协议是最好选择。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>没有碎片：</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>比</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>没有碎片，</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>分发大文件会比小文件分发方便很多。特别是存储，小文件的性能超低，是个硬伤。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>穿墙：互联网不可能不开放</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>协议，否则就不叫互联网。所以任何端口封掉，也不会导致</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>流看不了。（不过</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>也能穿墙，用</span><span
     lang=EN-US>RTMPT</span><span style='font-family:宋体'>协议）。</span></li>
</ul>

<p><span lang=EN-US>HTTP</span>的劣势是：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>实时性差：基本上没有实时性这个说法。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>原生支持不好：就</span><span
     lang=EN-US>PC</span><span style='font-family:宋体'>上</span><span lang=EN-US>flash</span><span
     style='font-family:宋体'>对于</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>流支持还可以，</span><span lang=EN-US>Android/IOS</span><span
     style='font-family:宋体'>上似乎只能</span><span lang=EN-US>mp4</span><span
     style='font-family:宋体'>，总之移动端对于</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>的支持不是很完善。</span></li>
</ul>

<h4><a name="_Toc462219462"><span lang=EN-US>HLS</span></a></h4>

<p><span lang=EN-US>H</span><span lang=EN-US style='font-size:10.5pt'>LS</span><span
style='font-size:10.5pt'>是<span lang=EN-US>Apple</span>的开放标准，在<span lang=EN-US>Android3?</span>以上也原生支持<span
lang=EN-US>.</span></span></p>

<p><span lang=EN-US style='font-size:10.5pt'>HLS</span><span style='font-size:
10.5pt'>的主要优势是：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>性能高：和</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>一样。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>穿墙：和</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>一样。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>原生支持很好：</span><span
     lang=EN-US>IOS</span><span style='font-family:宋体'>上支持完美。</span><span
     lang=EN-US>Android</span><span style='font-family:宋体'>上支持差些。</span><span
     lang=EN-US>PC/flash</span><span style='font-family:宋体'>上现在也有各种</span><span
     lang=EN-US>as</span><span style='font-family:宋体'>插件支持</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>。</span></li>
</ul>

<p><span lang=EN-US style='font-size:10.5pt'>HLS</span><span style='font-size:
10.5pt'>的主要劣势是：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>实时性差：基本上</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>的延迟在</span><span
     lang=EN-US>10</span><span style='font-family:宋体'>秒以上。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>文件碎片：若分发</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>，码流低，切片较小时，小文件分发不是很友好。特别是一些对存储比较敏感的情况，譬如源站的存储，嵌入式的</span><span
     lang=EN-US>SD</span><span style='font-family:宋体'>卡。</span></li>
</ul>

<h4><a name="_Toc462219463"><span style='font-size:10.5pt;line-height:156%;
font-family:宋体'>应用方式</span></a></h4>

<p><span style='font-size:10.5pt'>推荐的方式是：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>编码器输出</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>协议。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>流媒体系统接入使用</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>协议。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>流媒体系统内部直播分发使用</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>PC+</span><span
     style='font-family:宋体'>直播</span><span lang=EN-US>+</span><span
     style='font-family:宋体'>实时性要求高：使用</span><span lang=EN-US>flash</span><span
     style='font-family:宋体'>播放</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>PC+</span><span
     style='font-family:宋体'>直播</span><span lang=EN-US>+</span><span
     style='font-family:宋体'>没有实时性要求：使用</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>或者</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>均可。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>PC+</span><span
     style='font-family:宋体'>点播：使用</span><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>或者</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>Apple IOS/OSX</span><span
     style='font-family:宋体'>：都使用</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>（实时性要求高得自己解析</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>，或者使用外部库，譬如</span><span lang=EN-US><a
     href="https://www.vitamio.org">https://www.vitamio.org</a></span><span
     lang=EN-US>, </span><span style='font-family:宋体'>开源播放器</span><span
     lang=EN-US>ijkplayer : </span><span lang=EN-US><a
     href="https://github.com/Bilibili/ijkplayer">https://github.com/Bilibili/ijkplayer</a></span><span
     style='font-family:宋体'>）</span></li>
</ul>

<p class=MsoNormal><span lang=EN-US>Andorid</span><span style='font-family:
宋体'>：和</span><span lang=EN-US>IOS</span><span style='font-family:宋体'>一样，不过可以确定的是可以自己开发支持</span><span
lang=EN-US>RTMP</span><span style='font-family:宋体'>。</span></p>

<h2><a name="_Toc26097960"></a><a name="_Toc462219464"></a><a
name="_Toc456260521"><span style='font-family:宋体'>集群与</span><span lang=EN-US>CDN</span></a><span
style='font-family:宋体'>相关功能</span></h2>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>SRS</span><span
style='font-family:宋体'>包含支大规模集群如</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>业务的关键特性，譬如</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>多级集群、</span><span lang=EN-US>VHOST</span><span
style='font-family:宋体'>虚拟服务器、无中断服务</span><span lang=EN-US>Reload</span><span
style='font-family:宋体'>、</span><span lang=EN-US>HTTP-FLV</span><span
style='font-family:宋体'>集群、</span><span lang=EN-US>Kafka</span><span
style='font-family:宋体'>对接。</span></p>

<h3><a name="_Toc26097961"></a><a name="_Toc462219465"></a><a
name="_Toc456260522"><span lang=EN-US>RTMP</span></a><span style='font-family:
宋体'>多级集群</span></h3>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>SRS</span><span
style='font-family:宋体'>可以使用</span><span lang=EN-US>edge</span><span
style='font-family:宋体'>搭建大规模集群，使用</span><span lang=EN-US>forward</span><span
style='font-family:宋体'>搭建小规模集群。</span></p>

<h4><a name="_Toc462219466"><span lang=EN-US>Edge</span></a><span
style='font-family:宋体'>边缘服务器</span></h4>

<p><span lang=EN-US>&nbsp;&nbsp;&nbsp; </span><span lang=EN-US
style='font-size:10.5pt'>SRS</span><span style='font-size:10.5pt'>的<span
lang=EN-US>Edge</span>提供访问时回源机制，在<span lang=EN-US>CDN/VDN</span>等流众多的应用场景中有重大意义，<span
lang=EN-US> forward/ingest</span>方案会造成大量带宽浪费。同时，<span lang=EN-US>SRS</span>的<span
lang=EN-US>Edge</span>能对接所有的<span lang=EN-US>RTMP</span>源站服务器， 不像<span
lang=EN-US>FMS</span>的<span lang=EN-US>Edge</span>只能对接<span lang=EN-US>FMS</span>源站（有私有协议）；另外，<span
lang=EN-US>SRS</span>的<span lang=EN-US>Edge</span>支持<span lang=EN-US>SRS</span>源站的所有逻辑
（譬如转码，转发，<span lang=EN-US>HLS</span>，<span lang=EN-US>DVR</span>等等），也就是说可以选择在源站切片<span
lang=EN-US>HLS</span>，也可以直接在边缘切片<span lang=EN-US>HLS</span>。</span></p>

<p><span style='font-size:10.5pt'>备注：<span lang=EN-US>Edge</span>一般负载高，<span
lang=EN-US>SRS</span>支持的并发足够跑满千兆网带宽了。</span></p>

<p><span lang=EN-US style='font-size:10.5pt'>Edge</span><span style='font-size:
10.5pt'>的主要应用场景：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>CDN/VDN</span><span
     style='font-family:宋体'>大规模集群，客户众多流众多需要按需回源。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>小规模集群，但是流比较多，需要按需回源。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>骨干带宽低，边缘服务器强悍，可以使用多层</span><span
     lang=EN-US>edge</span><span style='font-family:宋体'>，降低上层</span><span
     lang=EN-US>BGP</span><span style='font-family:宋体'>带宽。</span></li>
</ul>

<p><span style='font-size:10.5pt'>注意：<span lang=EN-US>edge</span>可以从源站拉流，也可以将流转发给源站。也就是说，播放<span
lang=EN-US>edge</span>上的流时，<span lang=EN-US>edge</span>会回源拉流；推流到<span
lang=EN-US>edge</span>上时，<span lang=EN-US>edge</span>会直接将流转发给源站。</span></p>

<p><span style='font-size:10.5pt'>注意：若只需要中转流给源站，不必用<span lang=EN-US>forward</span>，直接使用<span
lang=EN-US>edge</span>模式即可。可以直接支持推流 和拉流的中转，简单快捷。<span lang=EN-US>Forward</span>应用于目标服务器是多个，譬如将一路流主动送给多路服务器；<span
lang=EN-US>edge</span>虽然配置了多台服务器，但是只用了一台，有故障时才切换。</span></p>

<p><span style='font-size:10.5pt'>注意：优先使用<span lang=EN-US>edge</span>，除非知道必须用<span
lang=EN-US>forward</span>，才使用<span lang=EN-US>forward</span>。</span></p>

<h5><span style='font-family:宋体'>概念</span></h5>

<p><span style='font-size:10.5pt'>所谓边缘<span lang=EN-US>edge</span>服务器，就是边缘直播缓存服务器，配置时指定为<span
lang=EN-US>remote</span>模式和<span lang=EN-US>origin</span>（指定一个或多个源站<span
lang=EN-US>IP</span>），这个边缘<span lang=EN-US>edge</span>服务器就是源站的缓存了。</span></p>

<p><span style='font-size:10.5pt'>当用户推流到边缘服务器时，边缘直接将流转发给源站。譬如源站在北京<span
lang=EN-US>BGP</span>机房，湖南有个电信<span lang=EN-US>ADSL</span>用户要推流发布自己的直播流，要是直接推流到北京<span
lang=EN-US>BGP</span>可能效果不是很好，可以在湖南电信机房部署一个边缘，用户推流到湖南边缘，边缘转发给北京源站<span
lang=EN-US>BGP</span>。</span></p>

<p><span style='font-size:10.5pt'>当用户播放边缘服务器的流时，边缘服务器看有没有缓存，若缓存了就直接将流发给客户端。 若没有缓存，则发起一路回源链接，从源站取数据源源不断放到自己的缓存队列。也就是说，
多个客户端连接到边缘时，只有一路回源。这种结构在<span lang=EN-US>CDN</span>是最典型的部署结构。譬如北京源站，在全国<span
lang=EN-US>32</span>个省每个省都部署了<span lang=EN-US>10</span>台服务器，一共就有<span
lang=EN-US>320</span>台边缘，假设每个省<span lang=EN-US>1</span>台边缘服务器都有<span
lang=EN-US> 2000</span>用户观看，那么就有<span lang=EN-US>64</span>万用户，每秒钟集群发送<span
lang=EN-US>640Gbps</span>数据；而回源链接只有<span lang=EN-US>320</span>个， 实现了大规模分发。</span></p>

<p><span style='font-size:10.5pt'>边缘<span lang=EN-US>edge</span>服务器，实际上是解决大并发问题产生的分布式集群结构。<span
lang=EN-US>SRS</span>的边缘可以指定多个源站， 在源站出现故障时会自动切换到下一个源站，不影响用户观看，具有最佳的容错性，用户完全不会觉察。</span></p>

<h5><span lang=EN-US>HLS</span><span style='font-family:宋体'>边缘</span></h5>

<p><span lang=EN-US style='font-size:10.5pt'>Edge</span><span style='font-size:
10.5pt'>指的是<span lang=EN-US>RTMP</span>边缘，也就是说，配置为<span lang=EN-US>Edge</span>后，流推送到源站（<span
lang=EN-US>Origin</span>）时，<span lang=EN-US>Edge</span>不会切片生成<span lang=EN-US>HLS</span>。</span></p>

<p><span lang=EN-US style='font-size:10.5pt'>HLS</span><span style='font-size:
10.5pt'>切片配置在源站，只有源站会在推流上来就产生<span lang=EN-US>HLS</span>切片。边缘只有在访问时才会回源（这个时候 也会生成<span
lang=EN-US>HLS</span>，但单独访问边缘的<span lang=EN-US>HLS</span>是不行的）。</span></p>

<p><span style='font-size:10.5pt'>也就是说，<span lang=EN-US>HLS</span>的边缘需要使用<span
lang=EN-US>WEB</span>服务器缓存，譬如<span lang=EN-US>nginx</span>反向代理，<span
lang=EN-US>squid</span>，或者<span lang=EN-US>traffic server</span>等。</span></p>

<p><span style='font-size:10.5pt'>补充：</span><span lang=EN-US><a
href="https://github.com/ossrs/srs/issues/466"><span style='font-size:10.5pt'>https://github.com/ossrs/srs/issues/466</span></a></span><span
lang=EN-US style='font-size:10.5pt'> srs</span><span style='font-size:10.5pt'>作者考虑<span
lang=EN-US>hls</span>回源功能也就是<span lang=EN-US>HLS+</span></span></p>

<h5><span style='font-family:宋体'>下行边缘结构设计</span></h5>

<p><span style='font-size:10.5pt'>下行边缘指的是下行加速边缘，即客户端播放边缘服务器的流，边缘服务器从上层或源站取流。</span></p>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>下行边缘是非常重要的功能，需要考虑以下因素：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>以后支持多进程时结构变动最小。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>和目前所有功能的对接良好。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>支持平滑切换，源站和边缘两种角色。</span></li>
</ul>

<p><span style='font-size:10.5pt'>权衡后，<span lang=EN-US>SRS</span>下行边缘的结构设计如下：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>客户端连接到</span><span
     lang=EN-US>SRS</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>开始播放</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>的流</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>若流存在则直接播放。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>若流不存在，则从源站开始取流。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>其他流的功能，譬如转码</span><span
     lang=EN-US>/</span><span style='font-family:宋体'>转发</span><span lang=EN-US>/</span><span
     style='font-family:宋体'>采集等等。</span></li>
</ul>

<p><span style='font-size:10.5pt'>核心原则是：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>边缘服务器在没有流时，向源站拉取流。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>当流建立起来后，边缘完全变成源站服务器，对流的处理逻辑保持一致。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>支持回多个源站，错误时切换。这样可以支持上层服务器热备。</span></li>
</ul>

<p><span style='font-size:10.5pt'>备注：<span lang=EN-US>RTMP</span>多进程（计划中）的核心原则是用多进程作为完全镜像代理，连接到本地的服务器
（源站或边缘），完全不考虑其他业务因素，透明代理。这样可以简单，而且利用多<span lang=EN-US>CPU</span>能力。<span
lang=EN-US> HTTP</span>多进程是不考虑支持的，用<span lang=EN-US>NGINX</span>是最好选择，<span
lang=EN-US>SRS</span>的<span lang=EN-US>HTTP</span>服务器只是用在嵌入式设备中<span
lang=EN-US>,</span>没有性能要求的场合。</span></p>

<h5><span style='font-family:宋体'>上行边缘结构设计</span></h5>

<p><span style='font-size:10.5pt'>上行边缘指的是上行推流加速，客户端推流到边缘服务器，边缘将流转发给源站服务器。</span></p>

<p><span style='font-size:10.5pt'>考虑到下行和上行可能同时发生在一台边缘服务器，所以上行边缘只能用最简单的代理方式， 完全将流代理到上层或源站服务器。也就是说，只有在下行边缘时，边缘服务器才会启用其他的功能，譬如<span
lang=EN-US>HLS</span>转发等等。</span></p>

<p><span style='font-size:10.5pt'>上行边缘主要流程是：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>客户端连接到</span><span
     lang=EN-US>SRS</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>开始推流到</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>开始转发到源站服务器。</span></li>
</ul>

<h5><span style='font-family:宋体'>边缘的难点</span></h5>

<p><span lang=EN-US style='font-size:10.5pt'>RTMP</span><span style='font-size:
10.5pt'>边缘对于<span lang=EN-US>SRS</span>来讲问题不大，主要是混合了<span lang=EN-US>reload</span>和<span
lang=EN-US>HLS</span>功能的边缘服务器，会是一个难点。</span></p>

<p><span style='font-size:10.5pt'>譬如，用户在访问边缘上的<span lang=EN-US>HLS</span>流时，是使用<span
lang=EN-US>nginx</span>反向代理回源，还是使用<span lang=EN-US>RTMP</span>回源后在边缘切片？ 对于前者，需要部署<span
lang=EN-US>srs</span>作为<span lang=EN-US>RTMP</span>边缘，<span lang=EN-US>nginx</span>作为<span
lang=EN-US>HLS</span>边缘，管理两个服务器自然是比一个要费劲。 若使用后者，即<span lang=EN-US>RTMP</span>回源后边缘切片，能节省骨干带宽，只有一路回源，难点在于访问<span
lang=EN-US>HLS</span>时要发起<span lang=EN-US> RTMP</span>回源连接。</span></p>

<p><span style='font-size:10.5pt'>正因为业务逻辑会是边缘服务器的难点，所以<span lang=EN-US>SRS</span>对于上行边缘，采取直接代理方式，并没有采取边缘缓存方式。所谓边缘缓存方式，即推流到边缘时边缘也会当作源站直接缓存（作为源站），
然后转发给源站。边缘缓存方式看起来先进，这个边缘节点不必回源，实际上加大了集群的逻辑难度， 不如直接作为代理方式简单。</span></p>

<h4><a name="_Toc462219467"><span lang=EN-US>Forward</span></a><span
style='font-family:宋体'>小规模集群</span></h4>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>srs</span><span
style='font-family:宋体'>定位为直播服务器，其中一项重要的功能是</span><span lang=EN-US>forward</span><span
style='font-family:宋体'>，即将服务器的流转发到其他服务器。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>forward</span><span
style='font-family:宋体'>本身是用做热备，即用户推一路流上来，可以被</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>转发（或者转码后转发）到多个</span><span lang=EN-US>slave</span><span
style='font-family:宋体'>源站，</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>边缘可以回多个</span><span lang=EN-US>slave</span><span
style='font-family:宋体'>源，实现故障热备的功能，构建强容错系统。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>注意：</span><span
lang=EN-US>edge</span><span style='font-family:宋体'>可以从源站拉流，也可以将流转发给源站。也就是说，播放</span><span
lang=EN-US>edge</span><span style='font-family:宋体'>上的流时，</span><span
lang=EN-US>edge</span><span style='font-family:宋体'>会回源拉流；推流到</span><span
lang=EN-US>edge</span><span style='font-family:宋体'>上时，</span><span lang=EN-US>edge</span><span
style='font-family:宋体'>会直接将流转发给源站。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>若只需要中转流给源站，不必用</span><span
lang=EN-US>forward</span><span style='font-family:宋体'>，直接使用</span><span
lang=EN-US>edge</span><span style='font-family:宋体'>模式即可。可以直接支持推流和拉流的中转，简单快捷。</span><span
lang=EN-US>Forward</span><span style='font-family:宋体'>应用于目标服务器是多个，譬如将一路流主动送给多路服务器；</span><span
lang=EN-US>edge</span><span style='font-family:宋体'>虽然配置了多台服务器，但是只用了一台，有故障时才切换。优先使用</span><span
lang=EN-US>edge</span><span style='font-family:宋体'>，除非知道必须用</span><span
lang=EN-US>forward</span><span style='font-family:宋体'>，才使用</span><span
lang=EN-US>forward</span><span style='font-family:宋体'>。</span></p>

<h5><span lang=EN-US>Keywords</span></h5>

<p><span style='font-size:10.5pt'>为了和<span lang=EN-US>edge</span>方式区分，<span
lang=EN-US>forward</span>定义一次词汇如下：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>master</span><span
     style='font-family:宋体'>：主服务器，编码器推流到这个服务器，或者用</span><span lang=EN-US>ingest</span><span
     style='font-family:宋体'>流到服务器。总之，</span><span lang=EN-US>master</span><span
     style='font-family:宋体'>就是主服务器，负责转发流给其他服务器。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>slave</span><span
     style='font-family:宋体'>：从服务器，主服务器转发流到这个服务器。</span></li>
</ul>

<p><span style='font-size:10.5pt'>如果结合<span lang=EN-US>edge</span>集群方式，一般而言<span
lang=EN-US>master</span>和<span lang=EN-US>slave</span>都是<span lang=EN-US>origin</span>（源站服务器），<span
lang=EN-US>edge</span>边缘服务器可以从<span lang=EN-US>master</span>或者<span lang=EN-US>slave</span>回源取流。</span></p>

<p><span style='font-size:10.5pt'>实际上<span lang=EN-US>master</span>和<span
lang=EN-US>slave</span>也可以是<span lang=EN-US>edge</span>，但是不推荐，这种组合方式太多了，测试没有办法覆盖到。因此，强烈建议简化服务器的结构，只有<span
lang=EN-US>origin</span>（源站服务器）才配置转发，<span lang=EN-US>edge</span>（边缘服务器）只做边缘。</span></p>

<h5><span lang=EN-US>For Small Cluster</span></h5>

<p><span lang=EN-US style='font-size:10.5pt'>forward</span><span
style='font-size:10.5pt'>也可以用作搭建小型集群。架构图如下：</span></p>

<pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img
border=0 width=554 height=306 id="图片 3" src="srs_wiki.files/image005.jpg"></span></pre><pre><span
lang=EN-US>&nbsp;</span></pre>

<h5><span lang=EN-US>Forward VS Edge</span></h5>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>Forward</span><span
style='font-family:宋体'>架构和</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>架构的最大区别在于，</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>属于大规模集群，边缘节点会有成千上万台，源站</span><span lang=EN-US>2</span><span
style='font-family:宋体'>台（做热备），还需要有中间层。</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>的客户很多，流也会有很多。所以假若源站将每个流都转发给边缘，会造成巨大的浪费（有很多流只有少数节点需要）。</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>可见，</span><span lang=EN-US>forward</span><span
style='font-family:宋体'>只适用于所有边缘节点都需要所有的流。</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>是某些边缘节点需要某些流。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>forward</span><span style='font-family:
宋体'>的瓶颈在于流的数目，假设每个</span><span lang=EN-US>SRS</span><span style='font-family:
宋体'>只侦听一个端口：</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>系统中流的数目</span><span
lang=EN-US> = </span><span style='font-family:宋体'>编码器的流数目</span><span
lang=EN-US> × </span><span style='font-family:宋体'>节点数目</span><span lang=EN-US>
× </span><span style='font-family:宋体'>端口数目</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>考虑</span><span lang=EN-US>5</span><span
style='font-family:宋体'>个节点，每个节点起</span><span lang=EN-US>4</span><span
style='font-family:宋体'>个端口，即有</span><span lang=EN-US>20</span><span
style='font-family:宋体'>个</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>边缘。编码器出</span><span lang=EN-US>5</span><span
style='font-family:宋体'>路流，则有</span><code><span lang=EN-US>20 * 5 = 100</span></code><code>路流</code><span
style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>同样的架构，对于</span><span
lang=EN-US>CDN</span><span style='font-family:宋体'>的边缘节点来讲，系统的流数为</span><code>用户访问边缘节点的流</code><span
style='font-family:宋体'>，假设没有用户访问，系统中就没有流量。某个区域的用户访问某个节点上的流，系统中只有一路流，而不是</span><span
lang=EN-US>forward</span><span style='font-family:宋体'>广播式的多路流。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>另外，</span><span
lang=EN-US>forward</span><span style='font-family:宋体'>需要播放器随机访问多个端口，实现负载均衡，或者播放器访问</span><span
lang=EN-US>api</span><span style='font-family:宋体'>服务器，</span><span lang=EN-US>api</span><span
style='font-family:宋体'>服务器实现负载均衡，对于</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>来讲也不合适（需要客户改播放器）。</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>总之，</span><span lang=EN-US>forward</span><span
style='font-family:宋体'>适用于小型规模的集群，不适用于</span><span lang=EN-US>CDN</span><span
style='font-family:宋体'>大规模集群应用。</span></p>

<h5><span style='font-family:宋体'>其他使用场景</span></h5>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>forward</span><span
style='font-family:宋体'>还可以结合</span><span lang=EN-US>hls</span><span
style='font-family:宋体'>和</span><span lang=EN-US>transcoder</span><span
style='font-family:宋体'>功能使用，即在源站将流转码，然后</span><span lang=EN-US>forward</span><span
style='font-family:宋体'>到</span><span lang=EN-US>Slave</span><span
style='font-family:宋体'>节点，</span><span lang=EN-US>Slave</span><span
style='font-family:宋体'>节点支持</span><span lang=EN-US>rtmp</span><span
style='font-family:宋体'>同时切</span><span lang=EN-US>HLS</span><span
style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>因为用户推上来的流，或者编码器（譬如</span><span
lang=EN-US>FMLE</span><span style='font-family:宋体'>）可能不是</span><span
lang=EN-US>h264+aac</span><span style='font-family:宋体'>，需要先转码为</span><span
lang=EN-US>h264+aac</span><span style='font-family:宋体'>（可以只转码音频）后才能切片为</span><span
lang=EN-US>hls</span><span style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>需要结合</span><span
lang=EN-US>vhost</span><span style='font-family:宋体'>，先将流</span><span
lang=EN-US>transcode</span><span style='font-family:宋体'>送到另外一个</span><span
lang=EN-US>vhost</span><span style='font-family:宋体'>，这个</span><span lang=EN-US>vhost</span><span
style='font-family:宋体'>将流转发到</span><span lang=EN-US>Slave</span><span
style='font-family:宋体'>。这样可以只转发转码的流。</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>参考</span><span lang=EN-US>vhost</span><span
style='font-family:宋体'>，</span><span lang=EN-US>hls</span><span
style='font-family:宋体'>和</span><span lang=EN-US>transcoder</span><span
style='font-family:宋体'>相关</span><span lang=EN-US>wiki</span><span
style='font-family:宋体'>。</span></p>

<h4><a name="_Toc462219468"><span lang=EN-US>WIKI</span></a></h4>

<p><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_SampleRTMPCluster">https://github.com/ossrs/srs/wiki/v3_CN_SampleRTMPCluster</a></span></p>

<h4><a name="_Toc462219469"><span style='font-family:宋体'>补充</span><span
lang=EN-US>:</span></a><span style='font-family:宋体'>源站集群问题</span></h4>

<p class=MsoNormal><span lang=EN-US>&nbsp;&nbsp; &nbsp;</span><span
style='font-family:宋体'>目前</span><span lang=EN-US>srs</span><span
style='font-family:宋体;color:#333333'>多个边缘回多个源站时，某一时刻只能选择一个源站。</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'><br>
</span><span style='font-family:宋体;color:#333333'>因此，如果流推到</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>N(N&gt;=3)</span><span
style='font-family:宋体;color:#333333'>个源站中的两个，譬如做热备时，一定有一个源站是没有流的；这个时候边缘如果回源到这个源站，就会导致没有流；而边缘还得等待，因为边缘是无法知道源站没有这个流。</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'><br>
&nbsp;&nbsp; &nbsp;</span><span style='font-family:宋体;color:#333333'>从热备和负载均衡的角度看，应该支持多个源站，这些源站之间需要通信和同步状态，这样边缘在连接到没有流的源站时，源站可以告知边缘正确的源站是谁，也就是源站集群。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>源站集群实现可通过</span><span
lang=EN-US>RTMP</span><span style='font-family:宋体'>重定向和实时动态反馈调度算法让多个彼此独立的源站服务器建立通信，将它们组织成一个松耦合的虚拟“超级源站”，与之的交互，就像与一个超性能、高可用的单台源站交互一样。</span></p>

<p class=MsoNoSpacing><span lang=EN-US><img border=0 width=905 height=309
id="图片 7" src="srs_wiki.files/image006.jpg"></span></p>

<p class=MsoNoSpacing><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span><span style='font-family:宋体'>传统源站结构图</span><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><span
style='font-family:宋体'>源站集群结构图</span></p>

<h3><a name="_Toc26097962"></a><a name="_Toc462219470"></a><a
name="_Toc456260523"><span lang=EN-US>VHOST</span></a><span style='font-family:
宋体'>虚拟服务器</span></h3>

<h4><a name="_Toc462219471"><span lang=EN-US>RTMP</span></a><span
style='font-family:宋体'>的</span><span lang=EN-US>URL/Vhost</span><span
style='font-family:宋体'>规则</span></h4>

<p style='text-indent:21.0pt'><span lang=EN-US style='font-size:10.5pt'>RTMP</span><span
style='font-size:10.5pt'>的<span lang=EN-US>url</span>其实很简单，<span lang=EN-US>vhost</span>其实也没有什么新的概念，但是对于没有使用过的同学来讲，还是很容易混淆。几乎每个新人都必问的问题：<span
lang=EN-US>RTMP</span>那个<span lang=EN-US>URL</span>推流时应该填什么，什么是<span
lang=EN-US>vhost</span>，什么是<span lang=EN-US>app</span>？</span></p>

<h4><a name="_Toc462219472"><span style='font-size:10.5pt;line-height:156%;
font-family:宋体'>应用场景</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>Vhost</span><span
style='font-size:10.5pt'>的主要应用场景包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>一个分发网络支持多个客户：譬如</span><span
     lang=EN-US>CDN</span><span style='font-family:宋体'>，一个分发网络中，有</span><span
     lang=EN-US>N</span><span style='font-family:宋体'>个客户公用一套流媒体系统，如何区分用户，计费，监控等等？通过</span><span
     lang=EN-US>app</span><span style='font-family:宋体'>么？大家可能都叫做</span><span
     lang=EN-US>live</span><span style='font-family:宋体'>之类。最好是通过各自的域名。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>不同的应用配置：譬如</span><span
     lang=EN-US>FMLE</span><span style='font-family:宋体'>推上来的流是</span><span
     lang=EN-US>h264+mp3</span><span style='font-family:宋体'>，可以将音频转码后放到其他的</span><span
     lang=EN-US>vhost</span><span style='font-family:宋体'>分发</span><span
     lang=EN-US>hls</span><span style='font-family:宋体'>，这样接入</span><span
     lang=EN-US>h264+mp3</span><span style='font-family:宋体'>的</span><span
     lang=EN-US>vhost</span><span style='font-family:宋体'>就不用切</span><span
     lang=EN-US>hls</span><span style='font-family:宋体'>。</span></li>
</ul>

<p><span style='font-size:10.5pt'>总之，<span lang=EN-US>vhost</span>作为应用配置的单元，能隔离客户，应用不同的配置。</span></p>

<h4><a name="_Toc462219473"><span style='font-family:宋体'>标准</span><span
lang=EN-US>RTMP URL</span></a></h4>

<p><span style='font-size:10.5pt'>标准<span lang=EN-US>RTMP URL</span>指的是最大兼容的<span
lang=EN-US>RTMP URL</span>，基本上所有的服务器和播放器都能识别的<span lang=EN-US>URL</span>，和<span
lang=EN-US>HTTP URL</span>其实很相似，例如：</span></p>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0 width="100%"
 style='width:100.0%;background:#E5E5E5;border-collapse:collapse;border:none'>
 <thead>
  <tr>
   <td width="34%" style='width:34.84%;border:solid #DDDDDD 1.0pt;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP</span></b></p>
   </td>
   <td width="16%" style='width:16.36%;border:solid #DDDDDD 1.0pt;border-left:
   none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Schema</span></b></p>
   </td>
   <td width=83 style='width:62.15pt;border:solid #DDDDDD 1.0pt;border-left:
   none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Host</span></b></p>
   </td>
   <td width=48 style='width:36.2pt;border:solid #DDDDDD 1.0pt;border-left:
   none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Port</span></b></p>
   </td>
   <td width=58 style='width:43.65pt;border:solid #DDDDDD 1.0pt;border-left:
   none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>App</span></b></p>
   </td>
   <td width=94 style='width:70.15pt;border:solid #DDDDDD 1.0pt;border-left:
   none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Stream</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width="34%" style='width:34.84%;border:solid #DDDDDD 1.0pt;border-top:
  none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='color:black'><a
  href="http://192.168.1.10/players/srs_player.html"><span style='font-family:
  "Segoe UI",sans-serif;color:#4078C0;text-decoration:none'>http://192.168.1.10:80/players/srs_player.html</span></a></span></p>
  </td>
  <td width="16%" style='width:16.36%;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>http</span></p>
  </td>
  <td width=83 style='width:62.15pt;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>192.168.1.10</span></p>
  </td>
  <td width=48 style='width:36.2pt;border-top:none;border-left:none;border-bottom:
  solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>80</span></p>
  </td>
  <td width=58 style='width:43.65pt;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>players</span></p>
  </td>
  <td width=94 style='width:70.15pt;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>srs_player.html</span></p>
  </td>
 </tr>
 <tr>
  <td width="34%" style='width:34.84%;border:solid #DDDDDD 1.0pt;border-top:
  none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>rtmp://192.168.1.10:1935/live/livestream</span></p>
  </td>
  <td width="16%" style='width:16.36%;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>rtmp</span></p>
  </td>
  <td width=83 style='width:62.15pt;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>192.168.1.10</span></p>
  </td>
  <td width=48 style='width:36.2pt;border-top:none;border-left:none;border-bottom:
  solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>1935</span></p>
  </td>
  <td width=58 style='width:43.65pt;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>live</span></p>
  </td>
  <td width=94 style='width:70.15pt;border-top:none;border-left:none;
  border-bottom:solid #DDDDDD 1.0pt;border-right:solid #DDDDDD 1.0pt;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>livestream</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-family:宋体;color:#333333'>其中：</span></p>

<ul type=disc>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Schema</span><span
     style='font-family:宋体'>：协议头，</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>HTTP</span><span
     style='font-family:宋体'>为</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>HTTP</span><span
     style='font-family:宋体'>或</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>HTTPS</span><span
     style='font-family:宋体'>，</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>RTMP</span><span
     style='font-family:宋体'>为</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>RTMP/RTMPS/RTMPE/RTMPT</span><span
     style='font-family:宋体'>等众多协议，还有新出的</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>RTMFP</span><span style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Host</span><span
     style='font-family:宋体'>：主机，表示要连接的主机，可以为主机</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>DNS</span><span
     style='font-family:宋体'>名称或者</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>IP</span><span
     style='font-family:宋体'>地址。商用时，一般不会用</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>IP</span><span style='font-family:宋体'>地址，而是</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>DNS</span><span
     style='font-family:宋体'>名称，这样可以用</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>CDN</span><span style='font-family:宋体'>分发内容（</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>CDN</span><span
     style='font-family:宋体'>一般使用</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>DNS</span><span
     style='font-family:宋体'>调度，即不同网络和地理位置的用户，通过</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>DNS</span><span
     style='font-family:宋体'>解析到的</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>IP</span><span
     style='font-family:宋体'>不一样，实现用户的就近访问）。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Port</span><span
     style='font-family:宋体'>：端口，</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>HTTP</span><span
     style='font-family:宋体'>默认为</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>80</span><span
     style='font-family:宋体'>，</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>RTMP</span><span
     style='font-family:宋体'>默认为</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>1935</span><span
     style='font-family:宋体'>。当端口没有指定时，使用默认端口。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Path</span><span
     style='font-family:宋体'>：路径，</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>HTTP</span><span
     style='font-family:宋体'>访问的文件路径。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>App</span><span
     style='font-family:宋体'>：</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>RTMP</span><span
     style='font-family:宋体'>的</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>Application</span><span
     style='font-family:宋体'>（应用）名称，可以类比为文件夹。以文件夹来分类不同的流，没有特殊约定，可以任意划分。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Stream</span><span
     style='font-family:宋体'>：</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>RTMP</span><span
     style='font-family:宋体'>的</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>Stream</span><span
     style='font-family:宋体'>（流）名称，可以类比为文件。</span></li>
</ul>

<h4><a name="_Toc462219474"><span lang=EN>NoVhost</span></a></h4>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>其实，</span><span
lang=EN>vhost</span><span style='font-family:宋体'>大多数用户都用不到，而且不推荐用，有点复杂。一般的用户用</span><span
lang=EN>app</span><span style='font-family:宋体'>就可以了。因为</span><span lang=EN>vhost/app/stream</span><span
style='font-family:宋体'>，只是一个分类方法而已；</span><span lang=EN>vhost</span><span
style='font-family:宋体'>需要在配置文件中说明，</span><span lang=EN>app/stream</span><span
style='font-family:宋体'>都不需要配置。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>什么时候用</span><span
lang=EN>vhost</span><span style='font-family:宋体'>？如果你是提供服务，譬如你有</span><span
lang=EN>100</span><span style='font-family:宋体'>个客户，都要用一套平台，走同样的流媒体服务器分发。那可以每个客户一个</span><span
lang=EN>vhost</span><span style='font-family:宋体'>，这样他们的</span><span lang=EN>app</span><span
style='font-family:宋体'>和</span><span lang=EN>stream</span><span
style='font-family:宋体'>可以相同都可以。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>一般的用法，举个例子，有个视频网站，自己搭建服务器，所以只有他自己一个客户，就不要用</span><span
lang=EN>vhost</span><span style='font-family:宋体'>了。假设视频网站提供聊天服务，聊天有不同的话题类型，譬如：军事栏目，读书栏目，历史栏目三个分类，每个分类下面有很多聊天室。只要这么配置就好：</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-size:10.0pt;font-family:Consolas;
color:#333333'>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
1935</span><span lang=EN style='font-size:10.0pt;font-family:Consolas;
color:#A71D5D'>;</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-size:10.0pt;font-family:Consolas;
color:#333333'>vhost __defaultVhost__ {</span></p>

<p class=MsoNormal align=left style='text-align:left;background:#F7F7F7'><span
lang=EN style='font-size:10.0pt;font-family:Consolas;color:#333333'>}</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>生成网页时，譬如军事栏目的网页，都用</span><span
lang=EN>app</span><span style='font-family:宋体'>名称为</span><span lang=EN
style='font-size:10.0pt;font-family:Consolas'>military</span><span
style='font-family:宋体'>，某个聊天室叫做</span><span style='font-size:10.0pt;font-family:
宋体'>火箭</span><span style='font-family:宋体'>，这个页面的流可以用：</span><span lang=EN
style='font-size:10.0pt;font-family:Consolas'>rtmp://yourdomain.com/military/rock</span><span
style='font-family:宋体'>，编码器也推这个流，所有观看这个</span><span style='font-size:10.0pt;
font-family:宋体'>军事栏目</span><span lang=EN style='font-size:10.0pt;font-family:
Consolas'>/</span><span style='font-size:10.0pt;font-family:宋体'>火箭</span><span
style='font-family:宋体'>聊天室的页面的人，都播放这个流。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>军事栏目另外的网页，都用同样的</span><span
lang=EN>app</span><span style='font-family:宋体'>名称</span><span lang=EN
style='font-size:10.0pt;font-family:Consolas'>military</span><span
style='font-family:宋体'>，但是流不一样，譬如某个聊天室叫做</span><span style='font-size:10.0pt;
font-family:宋体'>雷达</span><span style='font-family:宋体'>，这个页面的流可以用：</span><span
lang=EN style='font-size:10.0pt;font-family:Consolas'>rtmp://yourdomain.com/military/radar</span><span
style='font-family:宋体'>，推流和观看一样。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>如此类推，军事栏目页面生成时，不用更改</span><span
lang=EN>srs</span><span style='font-family:宋体'>的任何配置。也就是说，新增聊天室，不用改服务器配置；新增分类，譬如加个</span><span
style='font-size:10.0pt;font-family:宋体'>公开课</span><span style='font-family:
宋体'>的聊天室，也不用改服务器配置。足够简单！</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>另外，读书栏目可以用</span><span
lang=EN>app</span><span style='font-family:宋体'>名称为</span><span lang=EN
style='font-size:10.0pt;font-family:Consolas'>reader</span><span
style='font-family:宋体'>，栏目下的某个聊天室叫</span><span style='font-size:10.0pt;
font-family:宋体'>红楼梦</span><span style='font-family:宋体'>，这个页面的流可以用：</span><span
lang=EN style='font-size:10.0pt;font-family:Consolas'>rtmp://yourdomain.com/reader/red_mansion</span><span
style='font-family:宋体'>，所有在这个聊天室的人都是播放这个流。</span></p>

<h4><a name="_Toc462219475"><span lang=EN-US>Vhost</span></a><span
style='font-family:宋体'>的应用</span></h4>

<p style='text-indent:21.0pt'><span lang=EN-US style='font-size:10.5pt'>RTMP</span><span
style='font-size:10.5pt'>的<span lang=EN-US>Vhost</span>和<span lang=EN-US>HTTP</span>的<span
lang=EN-US>Vhost</span>概念是一样的：虚拟主机。详见下表（假设域名<span lang=EN-US>demo.srs.com</span>被解析到<span
lang=EN-US>IP</span>为<span lang=EN-US>192.168.1.10</span>的服务器）：</span></p>

<table class=MsoNormalTable border=0 cellpadding=0 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>HTTP</span></b></p>
   </td>
   <td width=92 style='width:68.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Host</span></b></p>
   </td>
   <td width=45 style='width:33.9pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Port</span></b></p>
   </td>
   <td width=120 style='width:89.9pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Vhost</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'><a
  href="http://demo.srs.com:80/players/srs_player.html">http://demo.srs.com:80/players/srs_player.html</a></span></p>
  </td>
  <td width=92 style='width:68.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>192.168.1.10</span></p>
  </td>
  <td width=45 style='width:33.9pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>80</span></p>
  </td>
  <td width=120 style='width:89.9pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>demo.srs.com</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rtmp://demo.srs.com:1935/live/livestream</span></p>
  </td>
  <td width=92 style='width:68.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>192.168.1.10</span></p>
  </td>
  <td width=45 style='width:33.9pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>1935</span></p>
  </td>
  <td width=120 style='width:89.9pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>demo.srs.com</span></p>
  </td>
 </tr>
</table>

<p><span lang=EN-US style='font-size:10.5pt;color:black'>Vhost</span><span
style='font-size:10.5pt'>主要的作用是：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>支持多用户：当一台服务器需要服务多个客户，譬如</span><span
     lang=EN-US>CDN</span><span style='font-family:宋体'>有</span><span
     lang=EN-US>cctv</span><span style='font-family:宋体'>（央视）和</span><span
     lang=EN-US>wasu</span><span style='font-family:宋体'>（华数传媒）两个客户时，如何隔离他们两个的资源？相当于不同的用户共用一台计算机，他们可以在自己的文件系统建立同样的文件目录结构，但是彼此不会冲突。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>域名调度：</span><span
     lang=EN-US>CDN</span><span style='font-family:宋体'>分发内容时，需要让用户访问离自己最近的边缘节点，边缘节点再从源站或上层节点获取数据，达到加速访问的效果。一般的做法就是</span><span
     lang=EN-US>Host</span><span style='font-family:宋体'>是</span><span
     lang=EN-US>DNS</span><span style='font-family:宋体'>域名，这样可以根据用户的信息解析到不同的节点。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>支持多配置：有时候需要使用不同的配置，考虑一个支持多终端（</span><span
     lang=EN-US>PC/Apple/Android</span><span style='font-family:宋体'>）的应用，</span><span
     lang=EN-US>PC</span><span style='font-family:宋体'>上</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>分发，</span><span lang=EN-US>Apple</span><span
     style='font-family:宋体'>和</span><span lang=EN-US> Android</span><span
     style='font-family:宋体'>是</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>分发，如何让</span><span lang=EN-US>PC</span><span
     style='font-family:宋体'>延迟最低，同时</span><span lang=EN-US>HLS</span><span
     style='font-family:宋体'>也能支持，而且终端播放时尽量地址一致（降低终端开发难度）？可以使用两个</span><span
     lang=EN-US>Vhost</span><span style='font-family:宋体'>，</span><span
     lang=EN-US>PC </span><span style='font-family:宋体'>和</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>；</span><span
     lang=EN-US>PC</span><span style='font-family:宋体'>配置为最低延迟的</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>，并且将流转发给</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>的</span><span
     lang=EN-US>Vhost</span><span style='font-family:宋体'>，可以对音频转码（可能不是</span><span
     lang=EN-US>H264/AAC</span><span style='font-family:宋体'>）后切片为</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>。</span><span
     lang=EN-US>PC</span><span style='font-family:宋体'>和</span><span lang=EN-US>HLS
     </span><span style='font-family:宋体'>这两个</span><span lang=EN-US>Vhost</span><span
     style='font-family:宋体'>的配置肯定是不一样的，播放时，流名称是一样，只需要使用不同的</span><span
     lang=EN-US>Host</span><span style='font-family:宋体'>就可以。</span></li>
</ul>

<h4><a name="_Toc462219476"><span lang=EN-US>Vhost</span></a><span
style='font-family:宋体'>支持多用户</span></h4>

<p style='text-indent:21.0pt'><span style='font-size:10.5pt'>假设<span
lang=EN-US>cctv</span>和<span lang=EN-US>wasu</span>都运行在一台边缘节点<span lang=EN-US>(192.168.1.10)</span>上，用户访问这两个媒体的流时，<span
lang=EN-US>Vhost</span>的作用见下表：</span></p>

<table class=MsoNormalTable border=0 cellpadding=0 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>RTMP</span></b></p>
   </td>
   <td width=86 style='width:64.4pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Host</span></b></p>
   </td>
   <td width=38 style='width:1.0cm;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Port</span></b></p>
   </td>
   <td width=83 style='width:62.3pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Vhost</span></b></p>
   </td>
   <td width=36 style='width:26.85pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>App</span></b></p>
   </td>
   <td width=84 style='width:63.05pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Stream</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rtmp://show.cctv.cn/live/livestream</span></p>
  </td>
  <td width=86 style='width:64.4pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>192.168.1.10</span></p>
  </td>
  <td width=38 style='width:1.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>1935</span></p>
  </td>
  <td width=83 style='width:62.3pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>show.cctv.cn</span></p>
  </td>
  <td width=36 style='width:26.85pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>live</span></p>
  </td>
  <td width=84 style='width:63.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>livestream</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rtmp://show.wasu.cn/live/livestream</span></p>
  </td>
  <td width=86 style='width:64.4pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>192.168.1.10</span></p>
  </td>
  <td width=38 style='width:1.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>1935</span></p>
  </td>
  <td width=83 style='width:62.3pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>show.wasu.cn</span></p>
  </td>
  <td width=36 style='width:26.85pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>live</span></p>
  </td>
  <td width=84 style='width:63.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>livestream</span></p>
  </td>
 </tr>
</table>

<p><span style='font-size:10.5pt;color:white'>在边缘节点（</span><span lang=EN-US
style='font-size:10.5pt'>192.168.1.10</span><span style='font-size:10.5pt'>）上的<span
lang=EN-US>SRS</span>，需要配置<span lang=EN-US>Vhost</span>，例如：</span></p>

<pre><span lang=EN-US style='font-size:10.5pt'>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>vhost show.cctv.cn {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>}</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>vhost show.wasu.cn {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>}</span></pre>

<h4><a name="_Toc462219477"><span style='font-family:宋体'>补充</span><span
lang=EN-US>:Vhost</span></a><span style='font-family:宋体'>域名调度</span></h4>

<p><span lang=EN-US>&nbsp;&nbsp; </span><span style='font-size:10.5pt'>每个客户都有自己的域名。使用这个域名推流或拉流<span
lang=EN-US>,</span>如<span lang=EN-US>rtmp://pull.test.com/live/stream</span>，然后通过下面这些流程，向边缘服务器推流或拉流。</span></p>

<p style='margin-left:72.0pt;text-indent:-18.0pt'><span lang=EN-US
style='font-size:10.5pt'>1.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
style='font-size:10.5pt'>首先<span lang=EN-US>pull.test.com</span>通过本地域名服务器解析到对应运营商的授权服务器，</span></p>

<p style='margin-left:72.0pt;text-indent:-18.0pt'><span lang=EN-US
style='font-size:10.5pt'>2.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
style='font-size:10.5pt'>授权服务器通过<span lang=EN-US>CNAME</span>记录，将请求转向全局负载均衡<span
lang=EN-US>GLBS</span>，<span lang=EN-US>GLBS</span>使用智能调度算法，将请求解析到离用户最近本地负载均衡，获取虚拟服务器地址，</span></p>

<p style='margin-left:72.0pt;text-indent:-18.0pt'><span lang=EN-US
style='font-size:10.5pt'>3.<span style='font:7.0pt "Times New Roman"'>&nbsp; </span></span><span
style='font-size:10.5pt'>用户使用虚拟服务器地址，通过本地负载均衡调试算法，选择一台负载最轻的<span lang=EN-US>srs</span>边缘服务器。用户最终向使用这台服务器推流或拉流。</span></p>

<p><span style='font-size:10.5pt'>大概流程如下图所示</span></p>

<p><span lang=EN-US><img border=0 width=785 height=659
src="srs_wiki.files/image007.png"></span></p>

<h4><a name="_Toc462219478"><span lang=EN-US>Vhost</span></a><span
style='font-family:宋体'>支持多配置</span></h4>

<p style='text-indent:21.0pt'><span style='font-size:10.5pt'>以上面举的例子，若<span
lang=EN-US>cctv</span>需要延迟最低（意味着启动时只有声音，画面是黑屏），而<span lang=EN-US>wasu</span>需要快速启动（打开就能看到视频，服务器<span
lang=EN-US>cache</span>了最后一个<span lang=EN-US>gop</span>，延迟会较大）。</span></p>

<p><span style='font-size:10.5pt'>只需要对这两个<span lang=EN-US>Vhost</span>进行不同的配置，例如：</span></p>

<pre><span lang=EN-US style='font-size:10.5pt'>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>vhost show.cctv.cn {</span></pre><pre
style='text-indent:21.0pt'><span lang=EN-US style='font-size:10.5pt'>chunk_size 128<span
class=pl-k>;</span></span></pre><pre style='text-indent:21.0pt'><span
lang=EN-US style='font-size:10.5pt'>gop_cache&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; off;</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>}</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>vhost show.wasu.cn {</span></pre><pre
style='text-indent:21.0pt'><span lang=EN-US style='font-size:10.5pt'>chunk_size 4906<span
class=pl-k>;</span></span></pre><pre style='text-indent:21.0pt'><span
lang=EN-US style='font-size:10.5pt'>gop_cache&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>}</span></pre>

<p><span style='font-size:10.5pt'>总之，这两个<span lang=EN-US>Vhost</span>的配置完全没有关系，不会相互影响。</span></p>

<h4><a name="_Toc462219479"><span lang=EN-US>__defaultVhost__</span></a></h4>

<p style='text-indent:21.0pt'><span lang=EN-US style='font-size:10.5pt'>FMS</span><span
style='font-size:10.5pt'>的<span lang=EN-US>__defaultVhost__</span>是默认的<span
lang=EN-US>vhost</span>，当用户请求的<span lang=EN-US>vhost</span>没有匹配成功时，若配置了<span
lang=EN-US>defaultVhost</span>，则使用它来提供服务。若匹配失败，也没有<span lang=EN-US>defaultVhost</span>，则返回错误。</span></p>

<p><span style='font-size:10.5pt'>譬如，服务器<span lang=EN-US>192.168.1.10</span>上的<span
lang=EN-US>SRS</span>配置如下：</span></p>

<pre><span lang=EN-US style='font-size:10.5pt'>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>vhost demo.srs.com {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>}</span></pre>

<p><span style='font-size:10.5pt'>那么，当用户访问以下<span lang=EN-US>vhost</span>时：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>rtmp://demo.srs.com/live/livestream</span><span
     style='font-family:宋体'>：成功，匹配</span><span lang=EN-US>vhost</span><span
     style='font-family:宋体'>为</span><span lang=EN-US>demo.srs.com</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>rtmp://192.168.1.10/live/livestream</span><span
     style='font-family:宋体'>：失败，没有找到</span><span lang=EN-US>vhost</span><span
     style='font-family:宋体'>，也没有</span><span lang=EN-US>defaultVhost</span><span
     style='font-family:宋体'>。</span></li>
</ul>

<p><span lang=EN-US style='font-size:10.5pt'>defaultVhost</span><span
style='font-size:10.5pt'>和其他<span lang=EN-US>vhost</span>的规则一样，只是用来匹配那些没有匹配成功的<span
lang=EN-US>vhost</span>的请求的。</span></p>

<h4><a name="_Toc462219480"><span style='font-family:宋体'>访问指定的</span><span
lang=EN-US>Vhost</span></a></h4>

<p><span style='font-size:10.5pt'>如何访问某台服务器上的<span lang=EN-US>Vhost</span>？有两个方法：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>配置</span><span
     lang=EN-US>hosts</span><span style='font-family:宋体'>：因为</span><span
     lang=EN-US>Vhost</span><span style='font-family:宋体'>实际上就是</span><span
     lang=EN-US>DNS</span><span style='font-family:宋体'>解析，所以可以配置客户端的</span><span
     lang=EN-US>hosts</span><span style='font-family:宋体'>，将域名（</span><span
     lang=EN-US>Vhost</span><span style='font-family:宋体'>）解析到指定的服务器，就可以访问这台服务器上的指定的</span><span
     lang=EN-US>vhost</span><span style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>使用</span><span
     lang=EN-US>app</span><span style='font-family:宋体'>的参数：需要服务器支持。在</span><span
     lang=EN-US>app</span><span style='font-family:宋体'>后面带参数指定要访问的</span><span
     lang=EN-US>Vhost</span><span style='font-family:宋体'>。</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>支持</span><span
     lang=EN-US>?vhost=VHOST</span><span style='font-family:宋体'>和</span><span
     lang=EN-US>...vhost...VHOST</span><span style='font-family:宋体'>这两种方式，后面的方式是避免一些播放器不识别？和</span><span
     lang=EN-US>=</span><span style='font-family:宋体'>等特殊字符。</span></li>
</ul>

<p><span style='font-size:10.5pt'>普通用户不用这么麻烦，直接访问<span lang=EN-US>RTMP</span>地址就好了，有时候运维需要看某台机器上的<span
lang=EN-US>Vhost</span>的流是否有问题，就需要这种特殊的访问方式。考虑下面的例子：</span></p>

<pre><span lang=EN-US style='font-size:10.5pt'>RTMP URL: rtmp://demo.srs.com/live/livestream</span></pre><pre><span
style='font-size:10.5pt'>边缘节点数目：<span lang=EN-US>50</span>台</span></pre><pre><span
style='font-size:10.5pt'>边缘节点<span lang=EN-US>IP</span>：<span lang=EN-US>192.168.1.100 </span>至<span
lang=EN-US> 192.168.1.150</span></span></pre><pre><span style='font-size:10.5pt'>边缘节点<span
lang=EN-US>SRS</span>配置：</span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>&nbsp;&nbsp;&nbsp; listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; vhost demo.srs.com {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; mode remote<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; origin: xxxxxxx<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></pre>

<p><span style='font-size:10.5pt'>各种访问方式见下表：</span></p>

<table class=MsoNormalTable border=0 cellpadding=0 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体'>用户</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>RTMP URL</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>hosts</span></b><b><span style='font-family:
   宋体;color:black'>设置</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>目标</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>普通用户</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rtmp://demo.srs.com/live/livestream</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>无</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>由</span><span
  lang=EN-US style='color:black'>DNS<br>
  </span><span style='font-family:宋体;color:black'>解析到指定边缘</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>运维</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rtmp://demo.srs.com/live/livestream</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>192.168.1.100
  demo.srs.com</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>查看</span><span
  lang=EN-US style='color:black'>192.168.1.100</span><span style='font-family:
  宋体;color:black'>上的流</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>运维</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rtmp://192.168.1.100/live?<br>
  vhost=demo.srs.com/livestream</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>无</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>查看</span><span
  lang=EN-US style='color:black'>192.168.1.100</span><span style='font-family:
  宋体;color:black'>上的流</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>运维</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rtmp://192.168.1.100/live<br>
  ...vhost...demo.srs.com/livestream</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>无</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>查看</span><span
  lang=EN-US style='color:black'>192.168.1.100</span><span style='font-family:
  宋体;color:black'>上的流</span></p>
  </td>
 </tr>
</table>

<p><span style='font-size:10.5pt;color:black'>访问其他服务器的流也类似。</span></p>

<h4><a name="_Toc462219481"><span lang=EN>FMLE</span></a><span
style='font-family:宋体'>的奇怪</span><span lang=EN>URL</span><span
style='font-family:宋体'>方式</span></h4>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;color:#333333'>F</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>MLE</span><span
style='font-family:宋体;color:#333333'>推流时，</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>URL</span><span style='font-family:宋体;
color:#333333'>那个地方，有三个可以输入的框，参考</span><span lang=EN-US><a
href="http://help.adobe.com/en_US/FlashMediaLiveEncoder/3.0/Using/WS5b3ccc516d4fbf351e63e3d11c104ba878-7ff7.html"><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#4078C0;text-decoration:
none'>Adobe FMLE</span></a></span><span style='font-family:宋体;color:#333333'>：</span></p>

<ul type=disc>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>FMS URL: </span><span
     style='font-family:宋体'>需要输入</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>rtmp://host:port/app</span><span
     style='font-family:宋体'>，例如：</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>rtmp://demo.srs.com/live</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Backup URL: </span><span
     style='font-family:宋体'>备份的服务器，格式同</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>FMS URL</span><span style='font-family:宋体'>。若指定了备份服务器，</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>FMLE</span><span
     style='font-family:宋体'>会同时推送给这两个服务器。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Stream: </span><span
     style='font-family:宋体'>流名称，例如：</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>livestream</span></li>
</ul>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-family:宋体;color:#333333'>实际上是将</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP URL</span><span
style='font-family:宋体;color:#333333'>分成了两部分，</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>stream</span><span
style='font-family:宋体;color:#333333'>前面那部分和</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>stream</span><span
style='font-family:宋体;color:#333333'>。为何要这么搞？我猜想有以下原因：</span></p>

<ul type=disc>
 <li class=MsoNormal style='color:#333333;text-align:left'><span
     style='font-family:宋体'>支持多级</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>app</span><span
     style='font-family:宋体'>和</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>Stream</span><span
     style='font-family:宋体'>：我们目前举的例子都是一级</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>app</span><span style='font-family:宋体'>和一级</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>stream</span><span
     style='font-family:宋体'>，实际上</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>RTMP</span><span
     style='font-family:宋体'>支持多级</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>app</span><span
     style='font-family:宋体'>和</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>stream</span><span
     style='font-family:宋体'>，就像子文件夹，实际上很少用得到。所以</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>SRS</span><span
     style='font-family:宋体'>的</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>URL</span><span
     style='font-family:宋体'>都是一个地址，默认最后一个</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>/</span><span style='font-family:宋体'>后面就是</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>stream</span><span
     style='font-family:宋体'>，前面是</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>app</span><span
     style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span
     style='font-family:宋体'>支持流名称带参数：</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>Adobe</span><span style='font-family:宋体'>的鬼</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>HLS/HDS</span><span
     style='font-family:宋体'>非常之麻烦，那个地址是个恶心的完全不一致。参考</span><span lang=EN-US
     style='color:windowtext'><a
     href="http://help.adobe.com/en_US/flashmediaserver/devguide/WSd391de4d9c7bd609-52e437a812a3725dfa0-8000.html#WSd391de4d9c7bd609-52e437a812a3725dfa0-7ff5"><span
     lang=EN style='font-family:"Segoe UI",sans-serif;color:#4078C0;text-decoration:
     none'>FMS livepkgr</span></a></span><span style='font-family:宋体'>，例如发布一个</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>rtmp</span><span
     style='font-family:宋体'>，并切片成</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>HLS</span><span
     style='font-family:宋体'>：</span></li>
</ul>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>FMLE:</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>FMS
URL: rtmp://demo.srs.com/livepkgr</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>Stream:
livestream</span><span lang=EN style='font-family:Consolas;color:#A71D5D'>?</span><span
lang=EN style='font-family:Consolas;color:#333333'>adbe-live-event=liveevent</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>&nbsp;</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>Client:</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>RTMP:&nbsp;
rtmp://demo.srs.com/livepkgr/livestream</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>HLS:
http://demo.srs.com/hls-live/livepkgr/_definst_/liveevent/livestream.m3u8</span></p>

<p class=MsoNormal align=left style='text-align:left;background:#F7F7F7'><span
lang=EN style='font-family:Consolas;color:#333333'>HDS: http://demo.srs.com/hds-live/livepkgr/_definst_/liveevent/livestream.f4m</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-family:宋体;color:#333333'>没有比这个更恶心的东西了。比较</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
style='font-family:宋体;color:#333333'>的简洁方案：</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>FMLE:
</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>FMS
URL: rtmp://demo.srs.com/livepkgr</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>Stream:
livestream</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>&nbsp;</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>Client:</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>RTMP:
rtmp://demo.srs.com/livepkgr/livestream</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>HLS:
http://demo.srs.com/livepkgr/livestream.m3u8</span></p>

<p class=MsoNormal align=left style='text-align:left;background:#F7F7F7'><span
lang=EN style='font-family:Consolas;color:#333333'>HDS: not support yet.</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-family:宋体;color:#333333'>既然谈到了</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP URL</span><span
style='font-family:宋体;color:#333333'>中的参数，下一章就说说这个。</span></p>

<h4><a name="_Toc462219482"><span lang=EN>RTMP URL</span></a><span
style='font-family:宋体'>参数</span></h4>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP URL</span><span
style='font-family:宋体;color:#333333'>一般是不带参数，类似于</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>http</span><span
style='font-family:宋体;color:#333333'>的</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>query</span><span style='font-family:宋体;
color:#333333'>，有时候为了特殊的要求，会在</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>RTMP URL</span><span style='font-family:宋体;color:#333333'>中带参数，譬如：</span></p>

<ul type=disc>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Vhost</span><span
     style='font-family:宋体'>：前面讲过，在</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>app</span><span style='font-family:宋体'>后面加参数，可以访问指定服务器的指定</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>Vhost</span><span
     style='font-family:宋体'>。这个</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>SRS</span><span
     style='font-family:宋体'>的特殊约定，方便排错。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>FMLE</span><span
     style='font-family:宋体'>的</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>Stream</span><span
     style='font-family:宋体'>后面的参数，指定</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>event</span><span style='font-family:宋体'>之类的。</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>SRS</span><span
     style='font-family:宋体'>不需要这么麻烦，</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>HLS</span><span style='font-family:宋体'>是内置支持，无需这种复杂的配置。</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>Callback</span><span
     style='font-family:宋体'>也是</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>http</span><span
     style='font-family:宋体'>的，</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>FMS</span><span
     style='font-family:宋体'>为了支持服务器端脚本，需要很复杂的配置和复杂的参数，实在是很麻烦的设计。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>token</span><span
     style='font-family:宋体'>认证：</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>SRS</span><span
     style='font-family:宋体'>还未实现。在连接服务器时，在</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>app</span><span
     style='font-family:宋体'>后面指定</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>token</span><span
     style='font-family:宋体'>（方式和</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>vhost</span><span
     style='font-family:宋体'>一样），例如</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>rtmp://server/live?vhost=xxx&amp;token=xxx/livestream</span><span
     style='font-family:宋体'>，服务器可以取出</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>token</span><span style='font-family:宋体'>，进行验证，若验证失败则断开连接，这种是比</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>Refer</span><span
     style='font-family:宋体'>更高级的防盗链。</span></li>
</ul>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>app</span><span
style='font-family:宋体;color:#333333'>和</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>stream</span><span style='font-family:
宋体;color:#333333'>后面带参数，这两者有何区别，为何</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>SRS</span><span style='font-family:宋体;color:#333333'>把参数放在</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>app</span><span
style='font-family:宋体;color:#333333'>后面？客户端播放流的</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>as3</span><span
style='font-family:宋体;color:#333333'>代码大约是：</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#969896'>//
how to play url: rtmp://demo.srs.com/live/livestream</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>conn
</span><span lang=EN style='font-family:Consolas;color:#A71D5D'>=</span><span
lang=EN style='font-family:Consolas;color:#333333'> </span><span lang=EN
style='font-family:Consolas;color:#A71D5D'>new</span><span lang=EN
style='font-family:Consolas;color:#333333'> </span><span lang=EN
style='font-family:Consolas;color:#0086B3'>NetConnection</span><span lang=EN
style='font-family:Consolas;color:#333333'>()</span><span lang=EN
style='font-family:Consolas;color:#A71D5D'>;</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>conn</span><span
lang=EN style='font-family:Consolas;color:#A71D5D'>.</span><span lang=EN
style='font-family:Consolas;color:#0086B3'>connect</span><span lang=EN
style='font-family:Consolas;color:#333333'>(</span><span lang=EN
style='font-family:Consolas;color:#183691'>&quot;rtmp://demo.srs.com/live&quot;</span><span
lang=EN style='font-family:Consolas;color:#333333'>)</span><span lang=EN
style='font-family:Consolas;color:#A71D5D'>;</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>&nbsp;</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>stream
</span><span lang=EN style='font-family:Consolas;color:#A71D5D'>=</span><span
lang=EN style='font-family:Consolas;color:#333333'> </span><span lang=EN
style='font-family:Consolas;color:#A71D5D'>new</span><span lang=EN
style='font-family:Consolas;color:#333333'> </span><span lang=EN
style='font-family:Consolas;color:#0086B3'>NetStream</span><span lang=EN
style='font-family:Consolas;color:#333333'>(conn)</span><span lang=EN
style='font-family:Consolas;color:#A71D5D'>;</span></p>

<p class=MsoNormal align=left style='text-align:left;background:#F7F7F7'><span
lang=EN style='font-family:Consolas;color:#333333'>stream</span><span lang=EN
style='font-family:Consolas;color:#A71D5D'>.</span><span lang=EN
style='font-family:Consolas;color:#0086B3'>play</span><span lang=EN
style='font-family:Consolas;color:#333333'>(</span><span lang=EN
style='font-family:Consolas;color:#183691'>&quot;livestream&quot;</span><span
lang=EN style='font-family:Consolas;color:#333333'>)</span><span lang=EN
style='font-family:Consolas;color:#A71D5D'>;</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-family:宋体;color:#333333'>从</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>RTMP</span><span style='font-family:宋体;
color:#333333'>协议的角度来看：</span></p>

<ul type=disc>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>NetConnection.connect(vhost+app)</span><span
     style='font-family:宋体'>：这一步会完成握手，</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>connect</span><span style='font-family:宋体'>到</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>vhost</span><span
     style='font-family:宋体'>，切换到</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>app</span><span
     style='font-family:宋体'>。类似于登录到</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>vhost</span><span style='font-family:宋体'>后，</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>cd</span><span
     style='font-family:宋体'>到</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>app</span><span
     style='font-family:宋体'>这个目录。也就是</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>vhost</span><span style='font-family:宋体'>的验证，都可以在这一步做，也就是指定</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>vhost</span><span
     style='font-family:宋体'>也是在一步了，所以</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>app</span><span style='font-family:宋体'>后面跟的参数都是和</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>vhost/app</span><span
     style='font-family:宋体'>相关的。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>NetStream.play(stream)</span><span
     style='font-family:宋体'>：这一步是播放指定的直播流。所以和</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>stream</span><span
     style='font-family:宋体'>相关的事件，都可以传递参数，譬如</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>Adobe</span><span
     style='font-family:宋体'>的</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>event</span><span
     style='font-family:宋体'>。</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>SRS</span><span
     style='font-family:宋体'>是没有这些事件的，流启动时，若配置了</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>HLS</span><span
     style='font-family:宋体'>会自动开始切片。</span></li>
</ul>

<h4><a name="_Toc462219483"><span lang=EN>SRS</span></a><span style='font-family:
宋体'>的</span><span lang=EN>URL</span><span style='font-family:宋体'>规则</span></h4>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
style='font-family:宋体;color:#333333'>只做简化的事情，绝对不把简单的事情搞复杂。</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
style='font-family:宋体;color:#333333'>的</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>RTMP URL</span><span style='font-family:
宋体;color:#333333'>使用标准的</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>RTMP URL</span><span style='font-family:宋体;color:#333333'>，一般不需要对</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>app</span><span
style='font-family:宋体;color:#333333'>和</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>stream</span><span style='font-family:
宋体;color:#333333'>加参数，或者更改他们的意义。除了两个地方：</span></p>

<ul type=disc>
 <li class=MsoNormal style='color:#333333;text-align:left'><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>vhost</span><span
     style='font-family:宋体'>支持参数访问：为了方便运维访问某台服务器的</span><span lang=EN
     style='font-family:"Segoe UI",sans-serif'>vhost</span><span
     style='font-family:宋体'>，不需要设置</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>hosts</span><span
     style='font-family:宋体'>。不影响普通用户。</span></li>
 <li class=MsoNormal style='color:#333333;text-align:left'><span
     style='font-family:宋体'>支持</span><span lang=EN style='font-family:"Segoe UI",sans-serif'>token</span><span
     style='font-family:宋体'>验证：为了支持</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>token</span><span style='font-family:宋体'>验证，在</span><span
     lang=EN style='font-family:"Segoe UI",sans-serif'>app</span><span
     style='font-family:宋体'>后面带参数，这个是</span><span lang=EN style='font-family:
     "Segoe UI",sans-serif'>token</span><span style='font-family:宋体'>验证必须的方式。</span></li>
</ul>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-family:宋体;color:#333333'>另外，</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>SRS</span><span style='font-family:宋体;
color:#333333'>建议用户使用一级</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>app</span><span style='font-family:宋体;color:#333333'>和一级</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>stream</span><span
style='font-family:宋体;color:#333333'>，不使用多级</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>app</span><span
style='font-family:宋体;color:#333333'>和多级</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>stream</span><span style='font-family:
宋体;color:#333333'>。譬如：</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>//
</span><span style='font-family:宋体;color:#333333'>不推荐使用的多级</span><span lang=EN
style='font-family:Consolas;color:#333333'>app</span><span style='font-family:
宋体;color:#333333'>或</span><span lang=EN style='font-family:Consolas;color:#333333'>stream</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>rtmp://demo.srs.com/show/live/livestream</span></p>

<p class=MsoNormal align=left style='text-align:left;background:#F7F7F7'><span
lang=EN style='font-family:Consolas;color:#333333'>rtmp://demo.srs.com/show/live/livestream/2013</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>srs</span><span
style='font-family:宋体;color:#333333'>播放器</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>(srs_player)</span><span style='font-family:
宋体;color:#333333'>和</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>srs</span><span style='font-family:宋体;color:#333333'>编码器</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>(srs_publisher)</span><span
style='font-family:宋体;color:#333333'>不支持多级</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>app</span><span
style='font-family:宋体;color:#333333'>和</span><span lang=EN style='font-family:
"Segoe UI",sans-serif;color:#333333'>stream</span><span style='font-family:
宋体;color:#333333'>，他们认为最后一个斜杠（</span><span lang=EN style='font-family:"Segoe UI",sans-serif;
color:#333333'>/</span><span style='font-family:宋体;color:#333333'>）后面的就是</span><span
lang=EN style='font-family:"Segoe UI",sans-serif;color:#333333'>stream</span><span
style='font-family:宋体;color:#333333'>，前面的是</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>app</span><span
style='font-family:宋体;color:#333333'>。即：</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>//
srs_player</span><span style='font-family:宋体;color:#333333'>和</span><span
lang=EN style='font-family:Consolas;color:#333333'>srs_publisher</span><span
style='font-family:宋体;color:#333333'>的解析方式：</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>//
play or publish the following rtmp URL:</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>rtmp://demo.srs.com/show/live/livestream/2013</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>schema:
rtmp</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>host/vhost:
demo.srs.com</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left;
background:#F7F7F7'><span lang=EN style='font-family:Consolas;color:#333333'>app:
show/live/livestream</span></p>

<p class=MsoNormal align=left style='text-align:left;background:#F7F7F7'><span
lang=EN style='font-family:Consolas;color:#333333'>stream: 2013</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-family:宋体;color:#333333'>做此简化的好处是，</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>srs</span><span
style='font-family:宋体;color:#333333'>播放器和编码器，只需要指定一个</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>url</span><span
style='font-family:宋体;color:#333333'>，而且两者的</span><span lang=EN
style='font-family:"Segoe UI",sans-serif;color:#333333'>url</span><span
style='font-family:宋体;color:#333333'>是一样的。</span></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
style='font-size:12.0pt;font-family:宋体;color:#333333'>常见的三种</span><span
lang=EN style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;color:#333333'>RTMP
URL</span><span style='font-size:12.0pt;font-family:宋体;color:#333333'>，详细见下表：</span></p>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0 width="100%"
 style='width:100.0%;background:#E5E5E5;border-collapse:collapse;border:none'>
 <thead>
  <tr>
   <td style='border:solid #DDDDDD 1.0pt;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>URL</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   style='font-family:宋体;color:#333333'>说明</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>rtmp://demo.srs.com/live/livestream</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>普通用户的标准访问方式，观看直播流</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>rtmp://192.168.1.10/live?vhost=demo.srs.com/livestream</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>运维对特定服务器排错</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>rtmp://demo.srs.com/live?key=ER892ID839KD9D0A1D87D/livestream</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>token</span><span
  style='font-family:宋体;color:#333333'>验证用户，或者带宽测试的</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>key</span><span
  style='font-family:宋体;color:#333333'>验证</span></p>
  </td>
 </tr>
</table>

<h4><a name="_Toc462219484"><span lang=EN-US style='color:black'>WIKI</span></a></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_RtmpUrlVhost">https://github.com/ossrs/srs/wiki/v1_CN_RtmpUrlVhost</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097963"></a><a name="_Toc462219485"></a><a
name="_Toc456260524"><span style='font-family:宋体'>无中断服务</span><span lang=EN-US>Reload</span></a></h3>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>配置完全支持<span lang=EN-US>Reload</span>，即在不中断服务时应用配置的修改。</span></p>

<h4><a name="_Toc462219486"><span lang=EN-US>NotSupportedFeatures</span></a></h4>

<p><span style='font-size:10.5pt'>不支持<span lang=EN-US>reload</span>的功能包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>deamon</span><span
     style='font-family:宋体'>，是否后台启动。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>mode</span><span
     style='font-family:宋体'>，</span><span lang=EN-US>vhost</span><span
     style='font-family:宋体'>的模式。</span></li>
</ul>

<p class=MsoNoSpacing><span lang=EN-US>daemon</span><span style='font-family:
宋体'>选项当然是不支持</span><span lang=EN-US>reload</span><span style='font-family:宋体'>的。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>mode</span><span style='font-family:
宋体'>选项，即决定</span><span lang=EN-US>vhost</span><span style='font-family:宋体'>是源站还是边缘，不支持</span><span
lang=EN-US>reload</span><span style='font-family:宋体'>。若修改</span><span
lang=EN-US>mode</span><span style='font-family:宋体'>之后</span><span lang=EN-US>reload</span><span
style='font-family:宋体'>会导致</span><span lang=EN-US>server</span><span
style='font-family:宋体'>异常退出，由看门狗重启。原因在于：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>源站和边缘角色切换过于复杂。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>一般源站会建立设备组，全部做源站，不会突然变成边缘</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>上层和源站重启后，对最终用户没有影响，只是表现会切换上层的卡顿（客户端缓冲区设为</span><span
     lang=EN-US>3</span><span style='font-family:宋体'>秒以上时，卡顿都不会出现）。</span></li>
</ul>

<p><span style='font-size:10.5pt'>一个修改<span lang=EN-US>vhost</span>的<span
lang=EN-US>mode</span>属性的<span lang=EN-US>workaround</span>：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>删除</span><span
     lang=EN-US>vhost</span><span style='font-family:宋体'>并</span><span
     lang=EN-US>reload</span><span style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>确认</span><span
     lang=EN-US>vhost</span><span style='font-family:宋体'>已经删除了。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>添加</span><span
     lang=EN-US>vhost</span><span style='font-family:宋体'>，使用新的</span><span
     lang=EN-US>mode</span><span style='font-family:宋体'>，并</span><span
     lang=EN-US>reload</span><span style='font-family:宋体'>。</span></li>
</ul>

<h4><a name="_Toc462219487"><span style='font-family:宋体'>应用场景</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>Reload</span><span
style='font-size:10.5pt'>主要应用场景：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>配置快速生效：不用重启服务，修改配置后，只需要</span><code><span
     lang=EN-US>killall -1 srs</span></code><span style='font-family:宋体'>即可生效配置。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>不中断服务：商用服务器往往时时刻刻都在服务用户，如何将一个转码流的码率调低？如何禁用某些频道的</span><span
     lang=EN-US>HLS</span><span style='font-family:宋体'>？如何添加和删除频道？而且还中断现有用户的服务？使用</span><span
     lang=EN-US>Reload</span><span style='font-family:宋体'>。</span></li>
</ul>

<h4><a name="_Toc462219488"><span style='font-family:宋体'>使用方法</span></a></h4>

<p class=MsoNoSpacing><span lang=EN-US>Reload</span><span style='font-family:
宋体'>的方法为：</span><code><span lang=EN-US>killall -1 srs</span></code></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>或者指定发送的</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>进程：</span><code><span
lang=EN-US>kill -1 7635</span></code></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>使用启动脚本：</span><code><span
lang=EN-US>/etc/init.d/srs reload</span></code></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h4><a name="_Toc462219489"><span lang=EN-US>WIKI</span></a></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_Reload">https://github.com/ossrs/srs/wiki/v1_CN_Reload</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097964"></a><a name="_Toc462219490"></a><a
name="_Toc456260525"><span lang=EN-US>HTTP-FLV</span></a><span
style='font-family:宋体'>集群</span></h3>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span class=MsoHyperlink><span
lang=EN-US style='color:windowtext;text-decoration:none'>http-flv</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>集群实际使用</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>edge</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>边缘集群模式，在边缘服务器上启动</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>http-flv</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>功能，当用户通过输入地址如</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>:http://demo.srs.com/live/test.flv</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>使用</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>http-flv</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>访问时，会在边缘转换成</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>rtmp, </span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>然后</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>rtmp</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>回源。结构如下</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>: </span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>用户</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>&lt; -------http-flv------&gt; </span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>边缘</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>&lt; -------rtmp-------- &gt; </span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>源。</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>http-ts http-aac, http-aac</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>集群原理也一样。按原理来说</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>Hls</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>集群也可以采用这种模式来实现，不过目前</span></span><span class=MsoHyperlink><span
lang=EN-US style='color:windowtext;text-decoration:none'>srs</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>开源没有实现</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>hls</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>集群，只能通过反回代理方式</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>,</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>如</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>squid, nginx</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>，</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>SRS</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>商业版实现了</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>hls</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>集群，也就是他们说的</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>hls+</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>。请参考：</span></span><span lang=EN-US><a
href="https://github.com/ossrs/srs/issues/466">https://github.com/ossrs/srs/issues/466</a></span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span class=MsoHyperlink><span
lang=EN-US style='color:windowtext;text-decoration:none'>http-flv</span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>详细内容请参考</span></span><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>“</span></span><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v2_CN_SampleHttpFlv"><span lang=EN-US
style='font-family:宋体;color:windowtext;text-decoration:none'><span lang=EN-US>转封装成</span></span><span
style='color:windowtext;text-decoration:none'>HTTP</span><span lang=EN-US
style='font-family:宋体;color:windowtext;text-decoration:none'><span lang=EN-US>直播流</span></span></a><span
class=MsoHyperlink><span style='color:windowtext;text-decoration:none'>”</span></span></span><span
class=MsoHyperlink><span style='font-family:宋体;color:windowtext;text-decoration:
none'>章节</span></span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>SRS</span><span
style='font-family:宋体'>的</span><span lang=EN-US>HTTP FLV</span><span
style='font-family:宋体'>边缘只能使用单进程，如何做到多进程呢？可以使用</span><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>反向代理，</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>提供了</span><span lang=EN-US>go-sharp</span><span
style='font-family:宋体'>，支持根据</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>边缘的负载均衡以及心跳检测。参考：</span><span lang=EN-US><a
href="https://github.com/simple-rtmp-server/go-sharp">go-sharp</a></span></p>

<h4><a name="_Toc462219491"><span class=MsoHyperlink><span lang=EN-US
style='color:windowtext;text-decoration:none'>WIKI</span></span></a></h4>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_SampleHttpFlvCluster">https://github.com/ossrs/srs/wiki/v3_CN_SampleHttpFlvCluster</a></span></p>

<h3><a name="_Toc26097965"></a><a name="_Toc462219492"></a><a
name="_Toc456260526"><span lang=EN-US>Kafka</span></a><span style='font-family:
宋体'>对接</span></h3>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>SRS</span><span
style='font-family:宋体'>可以将信息以</span><span lang=EN-US>JSON</span><span
style='font-family:宋体'>形式发送到</span><span lang=EN-US>KAFKA</span><span
style='font-family:宋体'>集群，</span><span lang=EN-US>Spark</span><span
style='font-family:宋体'>等大数据系统从</span><span lang=EN-US>Kafka</span><span
style='font-family:宋体'>获取数据并处理。</span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<p class=MsoNormal><span style='font-family:宋体'>目前<span lang=EN-US>SRS</span>会将如下事件写入<span
lang=EN-US>Kafka</span>集群：</span></p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-family:
     宋体'>accept: </span><span style='font-family:宋体'>当收到客户端连接时。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-family:
     宋体'>close: </span><span style='font-family:宋体'>当关闭客户端连接时。</span></li>
</ol>

<h4><a name="_Toc462219493"><span lang=EN-US>WIKI</span></a></h4>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_Kafka"><span style='font-family:
宋体'>https://github.com/ossrs/srs/wiki/v3_CN_Kafka</span></a></span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-family:宋体'>&nbsp;</span></p>

<h2><a name="_Toc26097966"></a><a name="_Toc462219494"></a><a
name="_Toc456260527"><span style='font-family:宋体'>应用接口</span></a></h2>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>SRS</span><span
style='font-family:宋体'>还提供丰富的应用接口，包括</span><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>回调、安全策略</span><span lang=EN-US>Security</span><span
style='font-family:宋体'>、</span><span lang=EN-US>HTTP API</span><span
style='font-family:宋体'>接口、</span><span lang=EN-US>RTMP</span><span
style='font-family:宋体'>测速。</span></p>

<h3><a name="_Toc26097967"></a><a name="_Toc462219495"></a><a
name="_Toc456260528"><span lang=EN-US>HTTP</span></a><span style='font-family:
宋体'>回调</span></h3>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>SRS</span><span
style='font-family:宋体'>不支持服务器脚本，服务器端定制有一个重要的替代功能，就是</span><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>回调。譬如当客户端连接到</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>时，回调指定的</span><span lang=EN-US>http</span><span
style='font-family:宋体'>地址，这样可以实现验证功能。</span></p>

<h4><a name="_Toc462219496"><span style='font-family:宋体'>服务器脚本</span></a></h4>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-family:宋体'>SRS</span><span style='font-family:宋体'>不支持服务器端脚本，所谓服务器端脚本，指的是服务器可以加载外部脚本文件，解释并执行。</span></p>

<p class=MsoNormal align=left style='text-align:left'><span style='font-family:
宋体'>支持服务器脚本的服务器有<span lang=EN-US>FMS</span>，语言是<span lang=EN-US>actionscript1.0</span>；<span
lang=EN-US>nginx</span>支持的是<span lang=EN-US>lua</span>。</span></p>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-family:宋体'>SRS</span><span style='font-family:宋体'>不支持服务器脚本的原因有：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>不<span
     lang=EN-US>Simple</span>：违反了<span lang=EN-US>SRS(Simple RTMP Server)</span>的第一个<span
     lang=EN-US>S</span>，支持扩展脚本，出错的几率也扩展了。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>实际用处很小：我在国内知名的<span
     lang=EN-US>CDN</span>公司工作时，所在部门就是用<span lang=EN-US>FMS</span>，当然<span
     lang=EN-US>FMS</span>不提供源码，所以只能支持服务器脚本来定制。结果商用起来很费劲，基本上每天出问题，而且还没法查原因。所以实际的用处很小。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-family:
     宋体'>SRS</span><span style='font-family:宋体'>支持<span lang=EN-US>HTTP</span>调用：调用外部<span
     lang=EN-US>http</span>，实际上也是一种扩展方式，<span lang=EN-US>SRS</span>支持这种较好的方式。譬如当用户连接上<span
     lang=EN-US>SRS</span>时，会调用<span lang=EN-US>HTTP</span>接口，可以做验证。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-family:
     宋体'>SRS</span><span style='font-family:宋体'>开源：为何要定制脚本？重要的一个原因就是闭源，<span
     lang=EN-US>SRS</span>开源，可以修改源码。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US style='font-family:
     宋体'>SRS</span><span style='font-family:宋体'>代码定制简单：<span lang=EN-US>SRS</span>整个服务器实现代码才<span
     lang=EN-US>2</span>万行，<span lang=EN-US>nginx-rtmp</span>是<span lang=EN-US>3</span>万行<span
     lang=EN-US>+nginx</span>的<span lang=EN-US>14</span>万行，定制<span lang=EN-US>SRS</span>要简单很多。而且<span
     lang=EN-US>SRS</span>是<span lang=EN-US>“</span>同步<span lang=EN-US>”</span>处理的，逻辑很少。</span></li>
</ul>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>综上所述，<span
lang=EN-US>SRS</span>暂时不考虑支持扩展脚本，这个东西没啥用。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>&nbsp;</span></p>

<h4><a name="_Toc462219497"><span lang=EN-US>HTTP callback events</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>的回调事件包括：</span></p>

<table class=MsoNormalTable border=0 cellpadding=0 style='background:#F2F2F2'>
 <thead>
  <tr style='page-break-inside:avoid'>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体'>事件</span></b></p>
   </td>
   <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>数据</span></b></p>
   </td>
   <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   style='font-family:宋体;color:black'>说明</span></b></p>
   </td>
  </tr>
 </thead>
 <tr style='page-break-inside:avoid'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>on_connect</span></p>
  </td>
  <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>{<br>
  &quot;action&quot;: &quot;on_connect&quot;,<br>
  &quot;client_id&quot;: 1985,<br>
  &quot;ip&quot;: &quot;192.168.1.10&quot;, <br>
  &quot;vhost&quot;: &quot;video.test.com&quot;, <br>
  &quot;app&quot;: &quot;live&quot;,<br>
  &quot;tcUrl&quot;: &quot;rtmp://x/x?key=xxx&quot;,<br>
  &quot;pageUrl&quot;: &quot;http://x/x.html&quot;<br>
  }</span></p>
  </td>
  <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>当客户端连接到指定的</span><span
  lang=EN-US style='color:black'>vhost</span><span style='font-family:宋体;
  color:black'>和</span><span lang=EN-US style='color:black'>app</span><span
  style='font-family:宋体;color:black'>时</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>on_close</span></p>
  </td>
  <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>{<br>
  &quot;action&quot;: &quot;on_close&quot;,<br>
  &quot;client_id&quot;: 1985,<br>
  &quot;ip&quot;: &quot;192.168.1.10&quot;, <br>
  &quot;vhost&quot;: &quot;video.test.com&quot;, <br>
  &quot;app&quot;: &quot;live&quot;, <br>
  &quot;send_bytes&quot;: 10240, <br>
  &quot;recv_bytes&quot;: 10240 <br>
  }</span></p>
  </td>
  <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>当客户端关闭连接，或者</span><span
  lang=EN-US style='color:black'>SRS</span><span style='font-family:宋体;
  color:black'>主动关闭连接时</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>on_publish</span></p>
  </td>
  <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>{<br>
  &quot;action&quot;: &quot;on_publish&quot;,<br>
  &quot;client_id&quot;: 1985,<br>
  &quot;ip&quot;: &quot;192.168.1.10&quot;, <br>
  &quot;vhost&quot;: &quot;video.test.com&quot;, <br>
  &quot;app&quot;: &quot;live&quot;,<br>
  &quot;stream&quot;: &quot;livestream&quot;<br>
  }</span></p>
  </td>
  <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>当客户端发布流时，譬如</span><span
  lang=EN-US style='color:black'>flash/FMLE</span><span style='font-family:
  宋体;color:black'>方式推流到服务器</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>on_unpublish</span></p>
  </td>
  <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>{<br>
  &quot;action&quot;: &quot;on_unpublish&quot;,<br>
  &quot;client_id&quot;: 1985,<br>
  &quot;ip&quot;: &quot;192.168.1.10&quot;, <br>
  &quot;vhost&quot;: &quot;video.test.com&quot;, <br>
  &quot;app&quot;: &quot;live&quot;,<br>
  &quot;stream&quot;: &quot;livestream&quot;<br>
  }</span></p>
  </td>
  <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>当客户端停止发布流时</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>on_play</span></p>
  </td>
  <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>{<br>
  &quot;action&quot;: &quot;on_play&quot;,<br>
  &quot;client_id&quot;: 1985,<br>
  &quot;ip&quot;: &quot;192.168.1.10&quot;, <br>
  &quot;vhost&quot;: &quot;video.test.com&quot;, <br>
  &quot;app&quot;: &quot;live&quot;,<br>
  &quot;stream&quot;: &quot;livestream&quot;,<br>
  &quot;pageUrl&quot;: &quot;</span><span lang=EN-US style='color:black'><a
  href="http://www.test.com/live.html">http://www.test.com/live.html</a></span><span
  lang=EN-US style='color:black'>&quot;<br>
  }</span></p>
  </td>
  <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>当客户端开始播放流时</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>on_stop</span></p>
  </td>
  <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>{<br>
  &quot;action&quot;: &quot;on_stop&quot;,<br>
  &quot;client_id&quot;: 1985,<br>
  &quot;ip&quot;: &quot;192.168.1.10&quot;, <br>
  &quot;vhost&quot;: &quot;video.test.com&quot;, <br>
  &quot;app&quot;: &quot;live&quot;,<br>
  &quot;stream&quot;: &quot;livestream&quot;<br>
  }</span></p>
  </td>
  <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>当客户端停止播放时。备注：停止播放可能不会关闭连接，还能再继续播放。</span></p>
  </td>
 </tr>
 <tr style='page-break-inside:avoid'>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>on_dvr</span></p>
  </td>
  <td width=192 style='width:144.2pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>{<br>
  &quot;action&quot;: &quot;on_dvr&quot;,<br>
  &quot;client_id&quot;: 1985,<br>
  &quot;ip&quot;: &quot;192.168.1.10&quot;, <br>
  &quot;vhost&quot;: &quot;video.test.com&quot;, <br>
  &quot;app&quot;: &quot;live&quot;,<br>
  &quot;stream&quot;: &quot;livestream&quot;,<br>
  &quot;cwd&quot;: &quot;/opt&quot;,<br>
  &quot;file&quot;: &quot;./l.xxx.flv&quot;<br>
  }</span></p>
  </td>
  <td width=280 style='width:209.75pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>当</span><span
  lang=EN-US style='color:black'>DVR</span><span style='font-family:宋体;
  color:black'>录制关闭一个</span><span lang=EN-US style='color:black'>flv</span><span
  style='font-family:宋体;color:black'>文件时</span></p>
  </td>
 </tr>
</table>

<p><span style='font-size:10.5pt'>其中，</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>事件：发生该事件时，即回调指定的</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>地址。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>HTTP</span><span
     style='font-family:宋体'>地址：可以支持多个，以空格分隔，</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>会依次回调这些接口。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>数据：</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>将数据</span><span
     lang=EN-US>POST</span><span style='font-family:宋体'>到</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>接口。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>返回值：</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>要求</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>服务器返回</span><span
     lang=EN-US>HTTP200</span><span style='font-family:宋体'>并且</span><span
     lang=EN-US>response</span><span style='font-family:宋体'>内容为整数错误码（</span><span
     lang=EN-US>0</span><span style='font-family:宋体'>表示成功），其他错误码会断开客户端连接。</span></li>
</ul>

<h4><a name="_Toc462219498"><span style='font-family:宋体'>基于</span><span
lang=EN-US>http</span></a><span style='font-family:宋体'>回调的认证</span></h4>

<h5><span lang=EN-US>DRM</span></h5>

<p><span lang=EN-US>DRM</span>重要的功能就是防盗链，只有允许的用户，才能访问服务器的流。有多种<span lang=EN-US>DRM</span>的方式：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>refer</span><span
     style='font-family:宋体'>防盗链：检查用户从哪个网站过来的。譬如不是从公司的页面过来的人都不让看。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>token</span><span
     style='font-family:宋体'>防盗链：用户在播放时，必须先申请</span><span lang=EN-US>token</span><span
     style='font-family:宋体'>，</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>会回调</span><span lang=EN-US>http</span><span
     style='font-family:宋体'>检查这个</span><span lang=EN-US>token</span><span
     style='font-family:宋体'>合法性。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>FMS token
     tranverse</span><span style='font-family:宋体'>：边缘</span><span lang=EN-US>RTMP</span><span
     style='font-family:宋体'>服务器收到每个连接，都去上行节点验证，即</span><span lang=EN-US>token</span><span
     style='font-family:宋体'>穿越认证。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>Access</span><span
     style='font-family:宋体'>服务器：专门的</span><span lang=EN-US>access</span><span
     style='font-family:宋体'>服务器负责</span><span lang=EN-US>DRM</span><span
     style='font-family:宋体'>。譬如</span><span lang=EN-US>adobe</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>access</span><span
     style='font-family:宋体'>服务器。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>推流认证：</span><span
     lang=EN-US>adobe</span><span style='font-family:宋体'>的</span><span
     lang=EN-US>RTMP</span><span style='font-family:宋体'>推流时，支持几种认证方式，这个也可以归于防盗链概念。</span></li>
</ul>

<h5><span lang=EN-US>Refer Authentication</span></h5>

<p><span lang=EN-US>SRS</span>支持<span lang=EN-US>refer</span>防盗链，<span
lang=EN-US>adobe</span>的<span lang=EN-US>flash</span>在播放<span lang=EN-US>RTMP</span>流时，会把页面的<span
lang=EN-US>http url</span>放在请求中，<span lang=EN-US> as</span>客户端代码不可以更改。当然如果用自己的客户端，不用<span
lang=EN-US>flash</span>播放流，就可以随意伪造了； 尽管如此，<span lang=EN-US>refer</span>防盗链还是能防住相当一部分盗链。</p>

<p>配置<span lang=EN-US>Refer</span>防盗链，在<span lang=EN-US>vhost</span>中开启<span
lang=EN-US>refer</span>即可，可以指定<span lang=EN-US>publish</span>和<span lang=EN-US>play</span>的<span
lang=EN-US>refer</span>：</p>

<pre><span class=pl-c><span lang=EN-US># the vhost for antisuck.</span></span></pre><pre><span
lang=EN-US>vhost refer.anti_suck.com {</span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp; <span
class=pl-c># refer hotlink-denial.</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp; refer {</span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># whether enable the refer hotlink-denial.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># default: off.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># the common refer for play and publish.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># if the page url of client not in the refer, access denied.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># if not specified this field, allow all.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># default: not specified.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; all&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; github.com github.io<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># refer for publish clients specified.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># the common refer is not overrided by this.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># if not specified this field, allow all.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># default: not specified.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; publish&nbsp;&nbsp; github.com github.io<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># refer for play clients specified.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># the common refer is not overrided by this.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># if not specified this field, allow all.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-c># default: not specified.</span></span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; play&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; github.com github.io<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp; }</span></pre><pre><span
lang=EN-US>}</span></pre>

<p>备注：<span lang=EN-US>SRS1/2</span>的<span lang=EN-US>Refer</span>配置方法和<span
lang=EN-US>SRS3</span>不一致，<span lang=EN-US>SRS3</span>兼容<span lang=EN-US>SRS1/2</span>的配置方法。</p>

<h5><span lang=EN-US>Token Authentication</span></h5>

<p><span lang=EN-US>token</span>类似于<span lang=EN-US>refer</span>，不过是放在<span
lang=EN-US>RTMP url</span>中，或者在<span lang=EN-US>connect</span>的请求参数中：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>token</span><span
     style='font-family:宋体'>在</span><span lang=EN-US>RTMP url</span><span
     style='font-family:宋体'>，譬如：</span><code><span lang=EN-US style='font-size:
     12.0pt'>rtmp://vhost/app?token=xxxx/stream</span></code><span
     style='font-family:宋体'>，这样服务器在</span><span lang=EN-US>on_connect</span><span
     style='font-family:宋体'>回调接口中，</span> <span style='font-family:宋体'>就会把</span><span
     lang=EN-US>url</span><span style='font-family:宋体'>带过去验证。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>token</span><span
     style='font-family:宋体'>在</span><span lang=EN-US>connect</span><span
     style='font-family:宋体'>的参数中：</span><span lang=EN-US>as</span><span
     style='font-family:宋体'>函数</span><span lang=EN-US>NetConnection.connect(url,
     token)</span><span style='font-family:宋体'>，服务器也可以拿到这个</span><span
     lang=EN-US>token</span><span style='font-family:宋体'>。注意：</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>目前不支持。</span></li>
</ul>

<p><span lang=EN-US>token</span>比<span lang=EN-US>refer</span>更强悍，可以指定超时时间，可以变更<span
lang=EN-US>token</span>之类。可惜就是需要服务器端做定制，做验证。<span lang=EN-US> SRS</span>提供<span
lang=EN-US>http</span>回调来做验证，已经有人用这种方式做了，比较简单靠谱。</p>

<p>举个常用的<span lang=EN-US>token</span>认证的例子：</p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>用户在</span><span
     lang=EN-US>web</span><span style='font-family:宋体'>页面登录，服务器可以生成一个</span><span
     lang=EN-US>token</span><span style='font-family:宋体'>，譬如</span><span
     lang=EN-US>token=md5(time+id+</span><span style='font-family:宋体'>私钥</span><span
     lang=EN-US>+</span><span style='font-family:宋体'>有效期</span><span
     lang=EN-US>)=88195f8943e5c944066725df2b1706f8</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>服务器返回给用户一个地址，带</span><span
     lang=EN-US>token</span><span style='font-family:宋体'>，譬如：</span><span
     lang=EN-US>rtmp://192.168.1.10/live?time=1402307089&amp;
     expire=3600&amp;token=88195f8943e5c944066725df2b1706f8/livestream</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>配置</span><span
     lang=EN-US>srs</span><span style='font-family:宋体'>的</span><span
     lang=EN-US>http</span><span style='font-family:宋体'>回调，</span><code><span
     lang=EN-US style='font-size:12.0pt'>on_connect
     http://127.0.0.1:8085/api/v1/clients;</span></code></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>用户播放时，</span><span
     lang=EN-US>srs</span><span style='font-family:宋体'>会回调那个地址，解析请求的内容，里面的</span><span
     lang=EN-US>tcUrl</span><span style='font-family:宋体'>就有那些认证信息。</span> <span
     style='font-family:宋体'>按同样的算法验证，如果</span><span lang=EN-US>md5</span><span
     style='font-family:宋体'>变了就返回错误，</span><span lang=EN-US>srs</span><span
     style='font-family:宋体'>就会拒绝连接。如果返回</span><span lang=EN-US>0</span><span
     style='font-family:宋体'>就会接受连接。</span></li>
</ol>

<h5><span lang=EN-US>TokenTraverse</span></h5>

<p><span lang=EN-US>Token</span>防盗链的穿越，指的是在<span lang=EN-US>origin-edge</span>集群中，客户播放<span
lang=EN-US>edge</span>边缘服务器的流时， 边缘将认证的<span lang=EN-US>token</span>发送给源站进行验证，即<span
lang=EN-US>token</span>穿越。</p>

<p><span lang=EN-US>FMS</span>的<span lang=EN-US>edge</span>和<span lang=EN-US>FMS</span>的<span
lang=EN-US>origin</span>使用私有协议，使用一个连接回源取数据，一个连接回源传输控制命令， 譬如<span lang=EN-US>token</span>穿越就是在这个连接做的。</p>

<p><span lang=EN-US>token</span>认证建议使用<span lang=EN-US>http</span>方式，也就是说客户端连接到边缘时，边缘使用<span
lang=EN-US>http</span>回调方式验证<span lang=EN-US>token</span>。 像<span lang=EN-US>fms</span>那种<span
lang=EN-US>token</span>穿越，是需要走<span lang=EN-US>RTMP</span>协议，其他开源服务器一般都不支持这种方式（中国特色）。</p>

<p><span lang=EN-US>SRS</span>可以支持类似<span lang=EN-US>fms</span>的<span
lang=EN-US>token</span>穿越，不过实现方式稍微有区别，不是采用<span lang=EN-US>fms edge</span>的私有协议，
而是每次新开一个连接回源验证，验证通过后边缘才提供服务。也就是边缘先做一个完全的代理。</p>

<p><span lang=EN-US>SRS</span>这种方式的特点是：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>在</span><span
     lang=EN-US>token</span><span style='font-family:宋体'>认证上，能和</span><span
     lang=EN-US>fms</span><span style='font-family:宋体'>源站对接，</span><span
     lang=EN-US>fms</span><span style='font-family:宋体'>源站感觉不到什么区别。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>每次边缘都会新开连接去验证，开销会大一些；而且只限于</span><span
     lang=EN-US>connect</span><span style='font-family:宋体'>事件验证，马上验证过后就会收到</span><span
     lang=EN-US>disconnect</span><span style='font-family:宋体'>事件。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>会导致源站的短连接过多（连接验证</span><span
     lang=EN-US>token</span><span style='font-family:宋体'>，断开），不过可以加一层</span><span
     lang=EN-US>fms edge</span><span style='font-family:宋体'>解决，这样比所有都是</span><span
     lang=EN-US>fms edge</span><span style='font-family:宋体'>要好。</span></li>
</ul>

<p>对于源站短连接过多的问题，可以加一层<span lang=EN-US>fms</span>边缘缓解，假设<span lang=EN-US>1000</span>个客户端连接到边缘：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>srs =&gt; </span><span
     style='font-family:宋体'>客户</span><span lang=EN-US>fms </span><span
     style='font-family:宋体'>这种方案，会有</span><span lang=EN-US>1000</span><span
     style='font-family:宋体'>个连接去回源验证，然后断开。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>srs =&gt; cdn-fms
     =&gt; </span><span style='font-family:宋体'>客户</span><span lang=EN-US>fms </span><span
     style='font-family:宋体'>这种方案，会有</span><span lang=EN-US>1000</span><span
     style='font-family:宋体'>个连接去</span><span lang=EN-US>cdn</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>fms</span><span
     style='font-family:宋体'>去验证，只有</span><span lang=EN-US>1</span><span
     style='font-family:宋体'>个连接去客户那边验证。</span></li>
</ul>

<p><span lang=EN-US>SRS</span>的<span lang=EN-US>token</span>穿越<span lang=EN-US>(traverse)</span>的配置，参考<code><span
lang=EN-US>edge.token.traverse.conf</span></code>：</p>

<pre><span lang=EN-US>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>vhost __defaultVhost__ {</span></pre><pre><span
lang=EN-US>&nbsp;&nbsp;&nbsp; cluster {</span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; mode&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; remote<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; origin&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 127.0.0.1:19350<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; token_traverse&nbsp; on<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US>&nbsp;&nbsp;&nbsp; }</span></pre><pre><span
lang=EN-US>}</span></pre>

<h5><span lang=EN-US>Access</span><span style='font-family:宋体'>服务器</span></h5>

<p><span lang=EN-US>SRS</span>暂时不支持。</p>

<h5><span style='font-family:宋体'>推流认证</span></h5>

<p><span lang=EN-US>SRS</span>暂时不支持，是<span lang=EN-US>RTMP</span>特殊的握手协议。</p>

<h4><a name="_Toc462219499"><span style='font-family:宋体'>默认的</span><span
lang=EN-US>HTTP</span></a><span style='font-family:宋体'>服务器</span></h4>

<p><span lang=EN-US>SRS</span>自带了一个默认的处理<span lang=EN-US>HTTP Callback</span>的服务器，启动时需要指定端口，譬如<span
lang=EN-US>8085</span>端口。</p>

<p>启动方法：<code><span lang=EN-US>python research/api-server/server.py 8085</span></code></p>

<h4><a name="_Toc462219500"><span lang=EN-US>Wiki</span></a></h4>

<p><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPCallback">https://github.com/ossrs/srs/wiki/v3_CN_HTTPCallback</a></span></p>

<h3><a name="_Toc26097968"></a><a name="_Toc462219501"></a><a
name="_Toc456260529"><span style='font-family:宋体'>安全策略</span><span lang=EN-US>Security</span></a></h3>

<h4><a name="_Toc462219502"><span lang=EN-US>Security</span></a></h4>

<p><span lang=EN-US>SRS</span>提供了禁用或允许客户端的简单安全策略。</p>

<h4><a name="_Toc462219503"><span lang=EN-US>Config</span></a></h4>

<p><span lang=EN-US>Vhost</span>中安全策略的配置：</p>

<pre><code><span lang=EN-US>vhost your_vhost {</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp; # security for host to allow or deny clients.</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp; # @see https://github.com/ossrs/srs/issues/211&nbsp;&nbsp; </span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;security {</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # whether enable the security for vhost.</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: off</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # the security list, each item format as:</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow|deny&nbsp;&nbsp;&nbsp; publish|play&nbsp;&nbsp;&nbsp; all|&lt;ip&gt;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # for example:</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; publish&nbsp;&nbsp;&nbsp;&nbsp; all;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; deny&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; publish&nbsp;&nbsp;&nbsp;&nbsp; all;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; publish&nbsp;&nbsp;&nbsp;&nbsp; 127.0.0.1;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; deny&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; publish&nbsp;&nbsp;&nbsp;&nbsp; 127.0.0.1;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;#&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; play&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; all;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; deny&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; play&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; all;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; play&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 127.0.0.1;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; deny&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; play&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 127.0.0.1;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # SRS apply the following simple strategies one by one:</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. allow all if security disabled.</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 2. default to deny all when security enabled.</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3. allow if matches allow strategy.</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 4. deny if matches deny strategy.</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; play&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; all;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; publish&nbsp;&nbsp;&nbsp;&nbsp; all;</span></code></pre><pre><code><span
lang=EN-US>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span lang=EN-US>}</span></code></pre>

<p><span lang=EN-US>SRS</span>应用安全策略的方式是<span lang=EN-US>:</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>若</span><span
     lang=EN-US>securty</span><span style='font-family:宋体'>没有开启，则允许所有。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>若</span><span
     lang=EN-US>security</span><span style='font-family:宋体'>开启了，默认禁止所有。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>允许客户端，若找到了匹配的允许策略。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>禁用客户端，若找到了匹配的禁用策略。</span></li>
</ul>

<p>参考配置文件<code><span lang=EN-US>conf/security.deny.publish.conf</span></code><span
lang=EN-US>.</span></p>

<h4><a name="_Toc462219504"><span lang=EN-US>Kickoff Client</span></a></h4>

<p><span style='font-size:10.5pt'>可以踢掉连接的用户，<span lang=EN-US>SRS</span>提供了<span
lang=EN-US>HTTP RESTful</span>接口：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>DELETE /api/v1/clients/{id}</span></code></pre>

<p><span style='font-size:10.5pt'>可以先查询到需要踢掉的<span lang=EN-US>Client</span>的<span
lang=EN-US>ID</span>：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>GET /api/v1/clients</span></code></pre>

<p><span style='font-size:10.5pt'>若需要踢掉推流的<span lang=EN-US>Client</span>，可以从<span
lang=EN-US>streams</span>接口中查询推流<span lang=EN-US>client</span>的<span
lang=EN-US>id</span>：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>GET /api/v1/streams</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>or GET /api/v1/streams/6745</span></code></pre>

<p><span style='font-size:10.5pt'>流信息中的<code><span lang=EN-US>stream.publish.cid</span></code>就是推流的客户端<span
lang=EN-US>id</span>：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>1. GET http://192.168.1.170:1985/api/v1/streams/6745</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>2. Response stream.publish.cid:</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>stream: {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; publish: {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; active: true,</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; cid: 107</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>}</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>3. DELETE http://192.168.1.170:1985/api/v1/clients/107</span></code></pre>

<p><span style='font-size:10.5pt'>备注：<span lang=EN-US>HTTP</span>请求可以使用</span><span
lang=EN-US><a href="http://ossrs.net/srs.release/http-rest/index.html"><span
style='font-size:10.5pt'>HTTP REST Tool</span></a></span></p>

<p><span style='font-size:10.5pt'>备注：<span lang=EN-US>HTTP</span>请求还可以使用<span
lang=EN-US>Linux</span>的工具<code><span lang=EN-US>curl</span></code>，常见的请求如下：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>curl -v -X GET http://192.168.1.170:1985/api/v1/clients/426 &amp;&amp; echo &quot;&quot;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>curl -v -X DELETE http://192.168.1.170:1985/api/v1/clients/426 &amp;&amp; echo &quot;&quot;</span></code></pre>

<h4><a name="_Toc462219505"><span lang=EN-US>Reload</span></a></h4>

<p>当<span lang=EN-US>Reload</span>改变<span lang=EN-US>security</span>配置后，只影响新连接的客户端，已经连接的客户端不受影响。</p>

<h4><a name="_Toc462219506"><span lang=EN-US>Wiki</span></a></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v2_CN_Security">https://github.com/ossrs/srs/wiki/v2_CN_Security</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097969"></a><a name="_Toc462219507"></a><a
name="_Toc456260530"><span lang=EN-US>HTTP API</span></a><span
style='font-family:宋体'>接口</span></h3>

<p class=MsoNormal style='text-indent:10.5pt'><span lang=EN-US>SRS</span><span
style='font-family:宋体'>提供</span><span lang=EN-US>HTTP</span><span
style='font-family:宋体'>接口，供外部程序管理服务器，并支持跨域（</span><span lang=EN-US>js</span><span
style='font-family:宋体'>可以直接控制和获取服务器的各种信息）。</span></p>

<h4><a name="_Toc462219508"><span style='font-family:宋体'>设计原则</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>的<span lang=EN-US>HTTP</span>接口遵循最简单原则，主要包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>只提供</span><span
     lang=EN-US>json</span><span style='font-family:宋体'>数据格式接口，要求请求和响应的数据全都是</span><span
     lang=EN-US>json</span><span style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>不提供</span><span
     lang=EN-US>html</span><span style='font-family:宋体'>数据，譬如运行</span><span
     lang=EN-US>SRS</span><span style='font-family:宋体'>后，浏览器打开</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>接口或</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>服务地址，看到的是</span><span
     lang=EN-US>json</span><span style='font-family:宋体'>，不是</span><span
     lang=EN-US>html</span><span style='font-family:宋体'>。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>发生错误时，支持</span><span
     lang=EN-US>HTTP</span><span style='font-family:宋体'>错误码，或者</span><span
     lang=EN-US>json</span><span style='font-family:宋体'>中的</span><span
     lang=EN-US>code</span><span style='font-family:宋体'>错误码。</span></li>
</ul>

<h4><a name="_Toc462219509"><span lang=EN-US>Config</span></a></h4>

<p>配置文件需要开启<span lang=EN-US>http-api</span>：</p>

<pre><span lang=EN-US style='font-size:9.0pt'>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1935<span
class=pl-k>;</span></span></pre><pre><span class=pl-c><span lang=EN-US
style='font-size:9.0pt'># system statistics section.</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># the main cycle will retrieve the system stat,</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># for example, the cpu/mem/network/disk-io data,</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># the http api, for instance, /api/v1/summaries will show these data.</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># @remark the heartbeat depends on the network,</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'>#&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; for example, the eth0 maybe the device which index is 0.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>stats {</span></pre><pre><span lang=EN-US
style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># the index of device ip.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># we may retrieve more than one network device.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># default: 0</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; network&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span
class=pl-c># the device name to stat the disk iops.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># ignore the device of /proc/diskstats if not configed.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; disk&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sda sdb xvda xvdb<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>}</span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># api of srs.</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># the http api config, export for external program to manage srs.</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># user can access http api of srs in browser directly, for instance, to access by:</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'>#&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; curl http://192.168.1.170:1985/api/v1/reload</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># which will reload srs, like cmd killall -1 srs, but the js can also invoke the http api,</span></span></pre><pre><span
class=pl-c><span lang=EN-US style='font-size:9.0pt'># where the cli can only be used in shell/terminate.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>http_api {</span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># whether http api is enabled.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># default: off</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span
class=pl-c># the http api listen entry is &lt;[ip:]port&gt;</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># for example, 192.168.1.100:1985</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># where the ip is optional, default to 0.0.0.0, that is 1985 equals to 0.0.0.0:1985</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># default: 1985</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1985<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span
class=pl-c># whether enable crossdomain request.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span class=pl-c># default: on</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; crossdomain&nbsp;&nbsp;&nbsp;&nbsp; on<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; <span
class=pl-c># the HTTP RAW API is more powerful api to change srs state and reload.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; raw_api {</span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># whether enable the HTTP RAW API.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># default: off</span></span></pre><pre><span lang=EN-US
style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; off<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># whether enable rpc reload.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># default: off</span></span></pre><pre><span lang=EN-US
style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow_reload&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; off<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># whether enable rpc query.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># default: off</span></span></pre><pre><span lang=EN-US
style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow_query&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; off<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># whether enable rpc update.</span></span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-c># default: off</span></span></pre><pre><span lang=EN-US
style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow_update&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; off<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>}</span></pre><pre><span lang=EN-US
style='font-size:9.0pt'>vhost __defaultVhost__ {</span></pre><pre><span
lang=EN-US style='font-size:9.0pt'>}</span></pre>

<p>其中，<code><span lang=EN-US>http_api</span></code>开启了<span lang=EN-US>HTTP API</span>，<code><span
lang=EN-US>stats</span></code>配置了<span lang=EN-US>SRS</span>后台统计的信息，包括：</p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>network: </span><span
     style='font-family:宋体'>这个配置了</span><span lang=EN-US>heartbeat</span><span
     style='font-family:宋体'>使用的网卡</span><span lang=EN-US>ip</span><span
     style='font-family:宋体'>，即</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>主动汇报的网卡信息。参考</span><span lang=EN-US><a
     href="https://github.com/ossrs/srs/wiki/v1_CN_Heartbeat">Heartbeat</a> </span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>disk: </span><span
     style='font-family:宋体'>这个配置了需要统计的磁盘的</span><span lang=EN-US>IOPS</span><span
     style='font-family:宋体'>，可以通过</span><code><span lang=EN-US
     style='font-size:12.0pt'>cat /proc/diskstats</span></code><span
     style='font-family:宋体'>命令获得名称，譬如阿里云的磁盘名称叫</span><span lang=EN-US>xvda.</span></li>
</ul>

<h4><a name="_Toc462219510"><span style='font-family:宋体'>访问</span><span
lang=EN-US>api</span></a></h4>

<p><span style='font-size:10.5pt'>直接在浏览器中就可以访问，或者用<span lang=EN-US>curl</span>发起<span
lang=EN-US>http</span>请求。</span></p>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>提供了<span lang=EN-US>api</span>的面包屑，可以从根目录开始导航，不需要任何记忆。一般的字段包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>code</span><span
     style='font-family:宋体'>表示错误码，按照</span><span lang=EN-US>linux</span><span
     style='font-family:宋体'>惯例，</span><span lang=EN-US>0</span><span
     style='font-family:宋体'>表示成功。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>urls</span><span
     style='font-family:宋体'>表示是面包屑导航，该</span><span lang=EN-US>api</span><span
     style='font-family:宋体'>下面的子</span><span lang=EN-US>api</span><span
     style='font-family:宋体'>（链接）。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>data</span><span
     style='font-family:宋体'>表示最后一级提供服务的</span><span lang=EN-US>api</span><span
     style='font-family:宋体'>，返回的数据。</span></li>
</ul>

<p><span style='font-size:10.5pt'>另外，提供服务的<span lang=EN-US>api</span>按照<span
lang=EN-US>HTTP RESTful</span>规则是复数，譬如<span lang=EN-US>versions/authors</span>，表示资源。<span
lang=EN-US>HTTP</span>的各种方法表示操作，譬如<span lang=EN-US>GET</span>查询，<span
lang=EN-US>PUT</span>更新，<span lang=EN-US>DELETE</span>删除。参考：</span><span
lang=EN-US><a href="http://www.redmine.org/projects/redmine/wiki/Rest_api"><span
style='font-size:10.5pt'>Redmine HTTP Rest api</span></a></span></p>

<p><span style='font-size:10.5pt'>根目录：</span></p>

<pre><span class=pl-c><span lang=EN-US style='font-size:10.5pt'># curl http://192.168.1.170:1985/</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; <span class=pl-pds>&quot;</span><span
class=pl-s>urls</span><span class=pl-pds>&quot;</span>: {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>api</span><span class=pl-pds>&quot;</span>: <span
class=pl-pds>&quot;</span><span class=pl-s>the api root</span><span
class=pl-pds>&quot;</span></span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>&nbsp;&nbsp;&nbsp; }</span></pre>

<p><span style='font-size:10.5pt'>返回的<span lang=EN-US>urls</span>表示子链接可以访问。接着访问：</span></p>

<pre><span class=pl-c><span lang=EN-US style='font-size:10.5pt'># curl http://192.168.1.170:1985/api/</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; <span class=pl-pds>&quot;</span><span
class=pl-s>urls</span><span class=pl-pds>&quot;</span>: {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>v1</span><span class=pl-pds>&quot;</span>: <span
class=pl-pds>&quot;</span><span class=pl-s>the api version 1.0</span><span
class=pl-pds>&quot;</span></span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>&nbsp;&nbsp;&nbsp; }</span></pre>

<p><span style='font-size:10.5pt'>继续：</span></p>

<pre><span class=pl-c><span lang=EN-US style='font-size:10.5pt'># curl http://192.168.1.170:1985/api/v1/</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; <span class=pl-pds>&quot;</span><span
class=pl-s>urls</span><span class=pl-pds>&quot;</span>: {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>versions</span><span class=pl-pds>&quot;</span>: <span
class=pl-pds>&quot;</span><span class=pl-s>the version of SRS</span><span
class=pl-pds>&quot;</span>,</span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-pds>&quot;</span><span
class=pl-s>authors</span><span class=pl-pds>&quot;</span>: <span class=pl-pds>&quot;</span><span
class=pl-s>the primary authors and contributors</span><span class=pl-pds>&quot;</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></pre>

<p><span style='font-size:10.5pt'>继续：</span></p>

<pre><span class=pl-c><span lang=EN-US style='font-size:10.5pt'># curl http://192.168.1.170:1985/api/v1/versions</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>major</span><span class=pl-pds>&quot;</span>: 0,</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>minor</span><span class=pl-pds>&quot;</span>: 9,</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>revision</span><span class=pl-pds>&quot;</span>: 43,</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>version</span><span class=pl-pds>&quot;</span>: <span
class=pl-pds>&quot;</span><span class=pl-s>0.9.43</span><span class=pl-pds>&quot;</span></span></pre>

<p><span style='font-size:10.5pt'>或者：</span></p>

<pre><span class=pl-c><span lang=EN-US style='font-size:10.5pt'># curl http://192.168.1.170:1985/api/v1/authors</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>primary_authors</span><span
class=pl-pds>&quot;</span>: <span class=pl-pds>&quot;</span><span class=pl-s>winlin,wenjie.zhao</span><span
class=pl-pds>&quot;</span>,</span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-pds>&quot;</span><span
class=pl-s>contributors_link</span><span class=pl-pds>&quot;</span>: <span
class=pl-pds>&quot;</span><span class=pl-s>https://github.com/ossrs/srs/blob/master/AUTHORS.txt</span><span
class=pl-pds>&quot;</span>,</span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class=pl-pds>&quot;</span><span
class=pl-s>contributors</span><span class=pl-pds>&quot;</span>: <span
class=pl-pds>&quot;</span><span class=pl-s>winlin&lt;winlin@vip.126.com&gt; wenjie.zhao&lt;740936897@qq.com&gt; xiangcheng.liu&lt;liuxc0116@foxmail.com&gt; naijia.liu&lt;youngcow@youngcow.net&gt; alcoholyi&lt;alcoholyi@qq.com&gt; </span><span
class=pl-pds>&quot;</span></span></pre>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>的<span lang=EN-US>API</span>属于<span lang=EN-US>“</span>自解释型，<span
lang=EN-US>HTTP RESTful API”</span></span></p>

<h4><a name="_Toc462219511"><span lang=EN-US>Error Code</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>可能返回<span lang=EN-US>HTTP</span>错误，即<span lang=EN-US>Status</span>不等于<span
lang=EN-US>200</span>；或者在<span lang=EN-US>HTTP Status</span>为<span lang=EN-US>200</span>时，响应的<span
lang=EN-US>json</span>的<span lang=EN-US>code</span>不为<span lang=EN-US>0.</span></span></p>

<p><span style='font-size:10.5pt'>譬如，返回<span lang=EN-US>HTTP</span>错误：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>winlin:~ winlin$ curl -v http://127.0.0.1:1985 &amp;&amp; echo &quot;&quot;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; HTTP/1.1 404 Not Found</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Connection: Keep-Alive</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Content-Length: 9</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Content-Type: text/plain; charset=utf-8</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Server: SRS/2.0.184</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>Not Found</span></code></pre>

<p><span style='font-size:10.5pt'>譬如，<span lang=EN-US>HTTP200</span>时内容中<span
lang=EN-US>code</span>不等于<span lang=EN-US>0</span>：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>winlin:~ winlin$ curl -v http://127.0.0.1:1985/api/v1/tests/errors &amp;&amp; echo &quot;&quot;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; HTTP/1.1 200 OK</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Connection: Keep-Alive</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Content-Length: 12</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Content-Type: application/json</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; Server: SRS/2.0.184</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&lt; </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>{&quot;code&quot;:100}</span></code></pre>

<p><span style='font-size:10.5pt'>用户应该处理这两种错误。</span></p>

<h4><a name="_Toc462219512"><span lang=EN-US>Crossdomain</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS HTTP API</span><span
style='font-size:10.5pt'>支持跨域，<span lang=EN-US>js</span>可以直接调用<span lang=EN-US>srs</span>的<span
lang=EN-US>http api</span>。</span></p>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>支持两种跨域方式：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>OPTIONS: jquery</span><span
     style='font-family:宋体'>可以直接跨域请求</span><span lang=EN-US>API</span><span
     style='font-family:宋体'>，浏览器会发送一个</span><span lang=EN-US>OPTIONS</span><span
     style='font-family:宋体'>跨域请求，</span><span lang=EN-US>SRS</span><span
     style='font-family:宋体'>允许跨域后，浏览器再次发起</span><span lang=EN-US>API</span><span
     style='font-family:宋体'>请求。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>JSONP:
     jquery/angularjs</span><span style='font-family:宋体'>可以发起</span><span
     lang=EN-US>JSONP</span><span style='font-family:宋体'>跨域请求，服务器会将响应作为</span><span
     lang=EN-US>js</span><span style='font-family:宋体'>文件，内容是调用一个函数，函数名由</span><span
     lang=EN-US>QueryString</span><span style='font-family:宋体'>中的</span><span
     lang=EN-US>callback</span><span style='font-family:宋体'>指定。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>JSONP-DELETE:
     JSONP</span><span style='font-family:宋体'>只能</span><span lang=EN-US>GET</span><span
     style='font-family:宋体'>，因此</span><span lang=EN-US>DELETE</span><span
     style='font-family:宋体'>方法是由</span><span lang=EN-US>QueryString</span><span
     style='font-family:宋体'>的</span><span lang=EN-US>method</span><span
     style='font-family:宋体'>指定的。</span></li>
</ul>

<p><span lang=EN-US style='font-size:10.5pt'>JSONP</span><span
style='font-size:10.5pt'>实例，例如：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>GET http://localhost:1985/api/v1/vhosts/?callback=JSON_CALLBACK</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>JSON_CALLBACK({&quot;code&quot;:0,&quot;server&quot;:13449})</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>GET http://localhost:1985/api/v1/vhosts/100?callback=JSON_CALLBACK&amp;method=DELETE</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>JSON_CALLBACK({&quot;code&quot;:0})</span></code></pre>

<h4><a name="_Toc462219513"><span lang=EN-US>Server ID</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>返回的<span lang=EN-US>api</span>中都会带有<code><span lang=EN-US>server</span></code>的信息，即<span
lang=EN-US>Server</span>的<span lang=EN-US>ID</span>，用来标识服务器。客户端在获取信息时，必须检查<span
lang=EN-US>ServerID</span>是否改变，改变时就是服务器重启，之前所有的数据都应该作废了。</span></p>

<h4><a name="_Toc462219514"><span lang=EN-US>API</span></a><span
style='font-family:宋体'>及描述</span></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>提供了<span lang=EN-US>API</span>的导航，即所有支持的<span lang=EN-US>API</span>及描述。</span></p>

<p><span style='font-size:10.5pt'>地址是：<code><span lang=EN-US>http://192.168.1.170:1985/api/v1</span></code>，主要包含的子<span
lang=EN-US>api</span>有：</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>API</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Example</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>Description</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>server</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>4481</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>服务器标识</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>versions</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/versions</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器版本信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>summaries</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/summaries</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器的摘要信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>rusages</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/rusages</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器资源使用信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>self_proc_stats</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/self_proc_stats</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器进程信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>system_proc_stats</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/system_proc_stats</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器所有进程情况</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>meminfos</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/meminfos</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器内存使用情况</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>authors</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/authors</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取作者、版权和</span><span
  lang=EN-US style='color:black'>License</span><span style='font-family:宋体;
  color:black'>信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>features</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/features</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取系统支持的功能列表</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>requests</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/requests</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取请求的信息，即当前发起的请求的详细信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>vhosts</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/vhosts</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器上的</span><span
  lang=EN-US style='color:black'>vhosts</span><span style='font-family:宋体;
  color:black'>信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>streams</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/streams</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器的</span><span
  lang=EN-US style='color:black'>streams</span><span style='font-family:宋体;
  color:black'>信息</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>clients</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/clients</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>获取服务器的</span><span
  lang=EN-US style='color:black'>clients</span><span style='font-family:宋体;
  color:black'>信息，默认获取前</span><span lang=EN-US style='color:black'>10</span><span
  style='font-family:宋体;color:black'>个</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>configs</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>/api/v1/configs</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>CUID</span><span
  style='font-family:宋体;color:black'>配置，</span><span lang=EN-US
  style='color:black'>RAW API</span></p>
  </td>
 </tr>
</table>

<h4><a name="_Toc462219515"><span lang=EN-US>Summaries</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>提供系统的摘要信息接口，譬如当前的内存、<span lang=EN-US>CPU</span>、网络、负载使用率。</span></p>

<p><span style='font-size:10.5pt'>地址为：<code><span lang=EN-US>http://192.168.1.170:1985/api/v1/summaries</span></code></span></p>

<h4><a name="_Toc462219516"><span lang=EN-US>Vhosts</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>提供获取所有<span lang=EN-US>vhost</span>的接口，<span lang=EN-US>vhost</span>中的<span
lang=EN-US>server</span>为<span lang=EN-US>srs</span>的<span lang=EN-US>id</span>，用来标识是否服务器重启了。</span></p>

<p><span style='font-size:10.5pt'>地址为：<code><span lang=EN-US>http://192.168.1.170:1985/api/v1/vhosts</span></code></span></p>

<p><span style='font-size:10.5pt'>还可以继续处理某个<span lang=EN-US>vhost</span>的信息，譬如<code><span
lang=EN-US>http://192.168.1.170:1985/api/v1/vhosts/3756</span></code></span></p>

<h4><a name="_Toc462219517"><span lang=EN-US>Streams</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>提供获取所有<span lang=EN-US>stream</span>的接口，<span lang=EN-US>stream</span>中的<span
lang=EN-US>server</span>为<span lang=EN-US>srs</span>的<span lang=EN-US>id</span>，用来标识是否服务器重启了。<span
lang=EN-US>vhost</span>为<span lang=EN-US>stream</span>所属的<span lang=EN-US>vhost</span>的<span
lang=EN-US>id</span>。</span></p>

<p><span style='font-size:10.5pt'>地址为：<code><span lang=EN-US>http://192.168.1.170:1985/api/v1/streams</span></code></span></p>

<p><span style='font-size:10.5pt'>还可以继续处理某个<span lang=EN-US>stream</span>的信息，譬如<code><span
lang=EN-US>http://192.168.1.170:1985/api/v1/streams/3756</span></code></span></p>

<h4><a name="_Toc462219518"><span lang=EN-US>Clients</span></a></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>提供查询客户端信息的接口，和<span lang=EN-US>Vhosts</span>或<span lang=EN-US>Streams</span>不一样的是，<span
lang=EN-US>Clients</span>查询时需要指定<span lang=EN-US>start</span>和<span lang=EN-US>count(</span>默认<span
lang=EN-US>start</span>为<span lang=EN-US>0</span>，<span lang=EN-US>count</span>为<span
lang=EN-US>10</span>，即查询头<span lang=EN-US>10</span>个<span lang=EN-US>clients)</span>。</span></p>

<p><span style='font-size:10.5pt'>地址为：<code><span lang=EN-US>http://192.168.1.170:1985/api/v1/clients</span></code></span></p>

<p><span style='font-size:10.5pt'>还可以继续处理某个<span lang=EN-US>client</span>的信息，譬如<code><span
lang=EN-US>http://192.168.1.170:1985/api/v1/clients/3756</span></code></span></p>

<h4><a name="_Toc462219519"><span lang=EN-US>Kickoff Client</span></a></h4>

<p><span style='font-size:10.5pt'>可以踢掉连接的用户，<span lang=EN-US>SRS</span>提供了<span
lang=EN-US>HTTP RESTful</span>接口：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>DELETE /api/v1/clients/{id}</span></code></pre>

<p><span style='font-size:10.5pt'>可以先查询到需要踢掉的<span lang=EN-US>Client</span>的<span
lang=EN-US>ID</span>：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>GET /api/v1/clients</span></code></pre>

<p><span style='font-size:10.5pt'>若需要踢掉推流的<span lang=EN-US>Client</span>，可以从<span
lang=EN-US>streams</span>接口中查询推流<span lang=EN-US>client</span>的<span
lang=EN-US>id</span>：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>GET /api/v1/streams</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>or GET /api/v1/streams/6745</span></code></pre>

<p><span style='font-size:10.5pt'>流信息中的<code><span lang=EN-US>stream.publish.cid</span></code>就是推流的客户端<span
lang=EN-US>id</span>：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>1. GET http://192.168.1.170:1985/api/v1/streams/6745</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>2. Response stream.publish.cid:</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>stream: {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; publish: {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; active: true,</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; cid: 107</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>}</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>3. DELETE http://192.168.1.170:1985/api/v1/clients/107</span></code></pre>

<p><span style='font-size:10.5pt'>备注：<span lang=EN-US>HTTP</span>请求可以使用</span><span
lang=EN-US><a href="http://ossrs.net/srs.release/http-rest/index.html"><span
style='font-size:10.5pt'>HTTP REST Tool</span></a></span></p>

<p><span style='font-size:10.5pt'>备注：<span lang=EN-US>HTTP</span>请求还可以使用<span
lang=EN-US>Linux</span>的工具<code><span lang=EN-US>curl</span></code>，常见的请求如下：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>curl -v -X GET http://192.168.1.170:1985/api/v1/clients/426 &amp;&amp; echo &quot;&quot;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>curl -v -X DELETE http://192.168.1.170:1985/api/v1/clients/426 &amp;&amp; echo &quot;&quot;</span></code></pre>

<h4><a name="_Toc462219520"><span lang=EN-US>Persistence Config</span></a></h4>

<p><span style='font-size:10.5pt'>可以发送信号<code><span lang=EN-US>SIGUSR1</span></code>给<span
lang=EN-US>SRS</span>，用来将当前系统的配置写入配置文件。主要用于：</span></p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>去掉注释，没有用的配置，格式化配置。</span></li>
 <li class=MsoNormal style='text-align:left'><span style='font-family:宋体'>支持</span><span
     lang=EN-US>HTTP API</span><span style='font-family:宋体'>写入配置，通过</span><span
     lang=EN-US>HTTP API</span><span style='font-family:宋体'>改变配置后写入然后</span><span
     lang=EN-US>Reload</span><span style='font-family:宋体'>，参考：</span><span
     lang=EN-US><a href="https://github.com/ossrs/srs/issues/319">HTTP RAW API</a></span><span
     lang=EN-US>.</span></li>
</ol>

<p><span style='font-size:10.5pt'>命令实例：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>killall -s SIGUSR1 srs</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>killall -30 srs</span></code></pre>

<p><span style='font-size:10.5pt'>写出来的配置文件可能是：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>listen 1935;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>max_connections 1000;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>daemon off;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>srs_log_tank console;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>pithy_print_ms 1000;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>http_api {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; enabled on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; listen 1985;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>}</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>http_server {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; enabled on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; listen 8080;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>}</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>stream_caster {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; enabled off;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; caster flv;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; output rtmp://127.0.0.1/[app]/[stream];</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; listen 8936;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>}</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; ingest livestream {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; input {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; type file;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; url doc/source.200kbps.768x320.flv;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ffmpeg ./objs/ffmpeg/bin/ffmpeg;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; engine {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled off;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; output rtmp://127.0.0.1:[port]/live?vhost=[vhost]/livestream;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; http_remux {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled off;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; mount [vhost]/[app]/[stream].flv;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; hstrs on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>}</span></code></pre>

<h4><a name="_Toc462219521"><span lang=EN-US>HTTP RAW API</span></a></h4>

<p style='text-indent:15.75pt'><span lang=EN-US style='font-size:10.5pt'>SRS</span><span
style='font-size:10.5pt'>支持<span lang=EN-US>RAW API</span>，一般的服务器只能提供读<span
lang=EN-US>(Read)</span>形式的<span lang=EN-US>API</span>，譬如获取系统状态之类，但是<span
lang=EN-US>SRS</span>提供写<span lang=EN-US>(Write)</span>形式的<span lang=EN-US>API</span>，譬如<span
lang=EN-US>Reload</span>和修改系统配置等所有改写系统的行为。</span></p>

<p><b><span style='font-size:10.5pt'>注意<span lang=EN-US>:</span></span></b><span
lang=EN-US style='font-size:10.5pt'> </span><span style='font-size:10.5pt'>必须在<code><span
lang=EN-US>http_api</span></code>配置中，开启<code><span lang=EN-US>http_api.raw_api.enabled</span></code>才能允许<span
lang=EN-US>HTTP RAW API</span>，否则会返回错误代码是<span lang=EN-US>1061</span>。</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>http_api {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1985;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; raw_api {</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow_reload&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow_query&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; allow_update&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>}</span></code></pre>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>支持的<span lang=EN-US>HTTP RAW API</span>包括：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US><a
     href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi#raw">Raw</a></span><span
     lang=EN-US>: </span><span style='font-family:宋体'>查看</span><span
     lang=EN-US>HTTP RAW API</span><span style='font-family:宋体'>的配置。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US><a
     href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi#reload">Reload</a></span><span
     lang=EN-US>: </span><span style='font-family:宋体'>支持</span><span
     lang=EN-US>reload</span><span style='font-family:宋体'>配置。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US><a
     href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi#raw-query">Query</a></span><span
     lang=EN-US>: </span><span style='font-family:宋体'>查询全局和</span><span
     lang=EN-US>Vhost</span><span style='font-family:宋体'>配置。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US><a
     href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi#raw-update">Update</a></span><span
     lang=EN-US>: </span><span style='font-family:宋体'>更新全局和</span><span
     lang=EN-US>Vhost</span><span style='font-family:宋体'>配置。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US><a
     href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi#raw-vhost">Vhost</a></span><span
     lang=EN-US>: Vhost</span><span style='font-family:宋体'>操作是</span><span
     lang=EN-US>Update</span><span style='font-family:宋体'>的子集。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US><a
     href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi#raw-dvr">DVR</a></span><span
     lang=EN-US>: DVR</span><span style='font-family:宋体'>操作是</span><span
     lang=EN-US>Update</span><span style='font-family:宋体'>的子集。</span></li>
</ul>

<h5><span lang=EN-US>Raw</span></h5>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>查询服务器端</span><span
  lang=EN-US style='color:black'>HTTP RAW API</span><span style='font-family:
  宋体;color:black'>的配置</span></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:12.0pt;color:black'>/api/v1/raw?rpc=raw</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:12.0pt;color:black'>curl
  http://127.0.0.1:1985/api/v1/raw?rpc=raw</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>不需要</span></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>无参数</span></p>
  </td>
 </tr>
</table>

<h5><span lang=EN-US>RAW Reload</span></h5>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>可以重新加载配置，和</span><code><span
  lang=EN-US style='font-size:12.0pt;color:black'>killall -1 srs</span></code><span
  style='font-family:宋体;color:black'>的效果是一样的</span></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:12.0pt;color:black'>/api/v1/raw?rpc=reload</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:12.0pt;color:black'>curl
  http://127.0.0.1:1985/api/v1/raw?rpc=reload</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:12.0pt;color:black'>allow_reload
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=85 style='width:63.8pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=460 style='width:345.05pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>无参数</span></p>
  </td>
 </tr>
</table>

<h5><span lang=EN-US>RAW Query</span></h5>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0 width=570
 style='width:427.5pt;background:#E5E5E5'>
 <thead>
  <tr>
   <td width=57 style='width:42.55pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-size:9.0pt'>Key</span></b></p>
   </td>
   <td width=507 style='width:380.45pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-size:9.0pt;color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=57 style='width:42.55pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>feature</span></p>
  </td>
  <td width=507 style='width:380.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-size:9.0pt;font-family:宋体;color:black'>查询服务器全局配置</span></p>
  </td>
 </tr>
 <tr>
  <td width=57 style='width:42.55pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>url</span></p>
  </td>
  <td width=507 style='width:380.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>/api/v1/raw?rpc=query&amp;scope=global</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=57 style='width:42.55pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>curl</span></p>
  </td>
  <td width=507 style='width:380.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=query&amp;scope=global'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=57 style='width:42.55pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>config</span></p>
  </td>
  <td width=507 style='width:380.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>allow_query
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=57 style='width:42.55pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>params</span></p>
  </td>
  <td width=507 style='width:380.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>scope=global</span></code><span
  style='font-size:9.0pt;font-family:宋体;color:black'>，查询服务器的全局配置</span></p>
  </td>
 </tr>
 <tr>
  <td width=57 style='width:42.55pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt'>&nbsp;</span></p>
  </td>
  <td width=507 style='width:380.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt'>&nbsp;</span></code></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0 width=570
 style='width:427.5pt;background:#F2F2F2'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-size:9.0pt'>Key</span></b></p>
   </td>
   <td width=520 style='width:389.95pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-size:9.0pt;color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>feature</span></p>
  </td>
  <td width=520 style='width:389.95pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-size:9.0pt;font-family:宋体;color:black'>查询服务器最小全局配置</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>url</span></p>
  </td>
  <td width=520 style='width:389.95pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>/api/v1/raw?rpc=query&amp;scope=minimal</span></code></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>curl</span></p>
  </td>
  <td width=520 style='width:389.95pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=query&amp;scope=minimal'</span></code></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>config</span></p>
  </td>
  <td width=520 style='width:389.95pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>allow_query
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>params</span></p>
  </td>
  <td width=520 style='width:389.95pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>scope=minimal</span></code><span
  style='font-size:9.0pt;font-family:宋体;color:black'>，查询服务器的最小全局配置</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=47 style='width:35.45pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-size:9.0pt'>Key</span></b></p>
   </td>
   <td width=506 style='width:379.85pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-size:9.0pt;color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=47 style='width:35.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>feature</span></p>
  </td>
  <td width=506 style='width:379.85pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-size:9.0pt;font-family:宋体;color:black'>查询服务器指定的</span><span
  lang=EN-US style='font-size:9.0pt;color:black'>Vhost</span><span
  style='font-size:9.0pt;font-family:宋体;color:black'>配置</span></p>
  </td>
 </tr>
 <tr>
  <td width=47 style='width:35.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>url</span></p>
  </td>
  <td width=506 style='width:379.85pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>/api/v1/raw?rpc=query&amp;scope=vhost&amp;vhost=__defaultVhost__</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=47 style='width:35.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>curl</span></p>
  </td>
  <td width=506 style='width:379.85pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=query&amp;scope=vhost&amp;vhost=__defaultVhost__'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=47 style='width:35.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>config</span></p>
  </td>
  <td width=506 style='width:379.85pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>allow_query
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=47 style='width:35.45pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='font-size:9.0pt;color:black'>params</span></p>
  </td>
  <td width=506 style='width:379.85pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='font-size:9.0pt;color:black'>scope=vhost&amp;vhost=xxx</span></code><span
  style='font-size:9.0pt;font-family:宋体;color:black'>，查询服务器的指定的</span><span
  lang=EN-US style='font-size:9.0pt;color:black'>Vhost</span><span
  style='font-size:9.0pt;font-family:宋体;color:black'>的配置</span></p>
  </td>
 </tr>
</table>

<h5><span lang=EN-US>RAW Update</span></h5>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>更新服务器侦听端口</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=listen&amp;value=1935,1936</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=listen&amp;value=1935,1936'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=listen&amp;value=1935,1936</span></code><span
  style='font-family:宋体;color:black'>，指定侦听的端口列表</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>参数必须是整数端口列表，多个端口时以逗号分割，譬如：</span><span
  lang=EN-US style='color:black'>1935,1936,1937</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>更新服务器</span><span
  lang=EN-US style='color:black'>PID</span><span style='font-family:宋体;
  color:black'>文件</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=pid&amp;value=./objs/srs.pid</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=pid&amp;value=./objs/srs.pid'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=pid&amp;value=./objs/srs.pid</span></code><span
  style='font-family:宋体;color:black'>，指定新的</span><span lang=EN-US
  style='color:black'>PID</span><span style='font-family:宋体;color:black'>文件</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>文件路径必须以</span><span
  lang=EN-US style='color:black'>./</span><span style='font-family:宋体;
  color:black'>，</span><span lang=EN-US style='color:black'>/tmp/</span><span
  style='font-family:宋体;color:black'>或</span><span lang=EN-US style='color:
  black'>/var/</span><span style='font-family:宋体;color:black'>开头，并且扩展名必须是</span><span
  lang=EN-US style='color:black'>.pid</span><span style='font-family:宋体;
  color:black'>，譬如：</span><span lang=EN-US style='color:black'>/var/srs.pid</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>设置</span><span
  lang=EN-US style='color:black'>RTMP</span><span style='font-family:宋体;
  color:black'>全局</span><span lang=EN-US style='color:black'>chunk_size</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=chunk_size&amp;value=60000</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=chunk_size&amp;value=60000'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=chunk_size&amp;value=60000</span></code><span
  style='font-family:宋体;color:black'>，指定新的全局</span><span lang=EN-US
  style='color:black'>chunk_size</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>chunk_size</span><span
  style='font-family:宋体;color:black'>必须是数字，并且在</span><span lang=EN-US
  style='color:black'>[128, 65535]</span><span style='font-family:宋体;
  color:black'>中，譬如：</span><span lang=EN-US style='color:black'>60000</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>设置</span><span
  lang=EN-US style='color:black'>ffmpeg</span><span style='font-family:宋体;
  color:black'>的全局日志路径</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=ff_log_dir&amp;value=./objs</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=ff_log_dir&amp;value=./objs'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=ff_log_dir&amp;value=./objs</span></code><span
  style='font-family:宋体;color:black'>，指定新的全局</span><span lang=EN-US
  style='color:black'>ff_log_dir</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ff_log_dir</span><span
  style='font-family:宋体;color:black'>必须以</span><span lang=EN-US
  style='color:black'>./, /tmp/</span><span style='font-family:宋体;color:black'>或</span><span
  lang=EN-US style='color:black'>/var/</span><span style='font-family:宋体;
  color:black'>开头。譬如：</span><span lang=EN-US style='color:black'>./objs</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>设置</span><span
  lang=EN-US style='color:black'>SRS</span><span style='font-family:宋体;
  color:black'>的日志容器</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=srs_log_tank&amp;value=file</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=srs_log_tank&amp;value=file'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=srs_log_tank&amp;value=file</span></code><span
  style='font-family:宋体;color:black'>，设置新的日志容器</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>srs_log_tank</span><span
  style='font-family:宋体;color:black'>必须是</span><span lang=EN-US
  style='color:black'>file</span><span style='font-family:宋体;color:black'>或</span><span
  lang=EN-US style='color:black'>console</span><span style='font-family:宋体;
  color:black'>。譬如：</span><span lang=EN-US style='color:black'>file</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>设置</span><span
  lang=EN-US style='color:black'>SRS</span><span style='font-family:宋体;
  color:black'>的日志级别</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=srs_log_level&amp;value=trace</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=srs_log_level&amp;value=trace'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=srs_log_level&amp;value=trace</span></code><span
  style='font-family:宋体;color:black'>，设置新的日志级别</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>srs_log_level</span><span
  style='font-family:宋体;color:black'>必须是</span><span lang=EN-US
  style='color:black'>verbose,info,trace,warn,error</span><span
  style='font-family:宋体;color:black'>。譬如：</span><span lang=EN-US
  style='color:black'>trace</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>设置</span><span
  lang=EN-US style='color:black'>SRS</span><span style='font-family:宋体;
  color:black'>的日志文件路径</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=srs_log_file&amp;value=./objs/srs.log</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=srs_log_file&amp;value=./objs/srs.log'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=srs_log_file&amp;value=./objs/srs.log</span></code><span
  style='font-family:宋体;color:black'>，设置新的日志文件路径</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>srs_log_file</span><span
  style='font-family:宋体;color:black'>必须是</span><span lang=EN-US
  style='color:black'>.log</span><span style='font-family:宋体;color:black'>类型，并且在</span><span
  lang=EN-US style='color:black'>./, /var/, /tmp/</span><span style='font-family:
  宋体;color:black'>开头。譬如：</span><span lang=EN-US style='color:black'>./objs/srs.log</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>设置</span><span
  lang=EN-US style='color:black'>SRS</span><span style='font-family:宋体;
  color:black'>能服务的最大连接数，包含</span><span lang=EN-US style='color:black'>RTMP</span><span
  style='font-family:宋体;color:black'>和</span><span lang=EN-US style='color:
  black'>HTTP</span><span style='font-family:宋体;color:black'>连接</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=max_connections&amp;value=1000</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=max_connections&amp;value=1000'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=max_connections&amp;value=1000</span></code><span
  style='font-family:宋体;color:black'>，设置新的最大连接数</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>max_connections</span><span
  style='font-family:宋体;color:black'>必须是整型，并且在</span><span lang=EN-US
  style='color:black'>[10, 65535]</span><span style='font-family:宋体;color:black'>范围内。譬如：</span><span
  lang=EN-US style='color:black'>1000</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>是否开启</span><span
  lang=EN-US style='color:black'>utc</span><span style='font-family:宋体;
  color:black'>时间，影响日志和包含时间的路径，譬如</span><span lang=EN-US style='color:black'>DVR</span><span
  style='font-family:宋体;color:black'>和</span><span lang=EN-US style='color:
  black'>HLS</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=utc_time&amp;value=false</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=utc_time&amp;value=false'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=utc_time&amp;value=false</span></code><span
  style='font-family:宋体;color:black'>，设置是否开启</span><span lang=EN-US
  style='color:black'>utc</span><span style='font-family:宋体;color:black'>时间</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>utc_time</span><span
  style='font-family:宋体;color:black'>是</span><span lang=EN-US style='color:
  black'>bool</span><span style='font-family:宋体;color:black'>，必须是</span><span
  lang=EN-US style='color:black'>true</span><span style='font-family:宋体;
  color:black'>或</span><span lang=EN-US style='color:black'>false</span><span
  style='font-family:宋体;color:black'>。譬如：</span><span lang=EN-US
  style='color:black'>false</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>设置全局的</span><span
  lang=EN-US style='color:black'>pithy</span><span style='font-family:宋体;
  color:black'>打印时间间隔</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=pithy_print_ms&amp;value=10000</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=pithy_print_ms&amp;value=10000'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=pithy_print_ms&amp;value=10000</span></code><span
  style='font-family:宋体;color:black'>，设置新的</span><span lang=EN-US
  style='color:black'>pithy</span><span style='font-family:宋体;color:black'>打印时间间隔</span></p>
  </td>
 </tr>
 <tr style='height:22.85pt'>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt;height:
  22.85pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt;
  height:22.85pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>pithy_print_ms</span><span
  style='font-family:宋体;color:black'>单位是毫秒，在</span><span lang=EN-US
  style='color:black'>[100,300000]</span><span style='font-family:宋体;
  color:black'>范围内。譬如：</span><span lang=EN-US style='color:black'>10000</span></p>
  </td>
 </tr>
</table>

<h5><span lang=EN-US>RAW Vhost</span></h5>

<p><span lang=EN-US style='font-size:10.5pt'>Vhost</span><span
style='font-size:10.5pt'>操作是<span lang=EN-US>Update</span>的一个子集。</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>新增</span><span
  lang=EN-US style='color:black'>vhost</span><span style='font-family:宋体;
  color:black'>，指定</span><span lang=EN-US style='color:black'>vhost</span><span
  style='font-family:宋体;color:black'>名称</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=create</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=create'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=vhost&amp;value=ossrs.net&amp;param=create</span></code><span
  style='font-family:宋体;color:black'>，创建新的</span><span lang=EN-US
  style='color:black'>vhost</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>新创建的</span><span
  lang=EN-US style='color:black'>vhost</span><span style='font-family:宋体;
  color:black'>必须是不存在的。注意禁用的</span><span lang=EN-US style='color:black'>vhost</span><span
  style='font-family:宋体;color:black'>也算是存在的</span><span lang=EN-US
  style='color:black'>vhost</span><span style='font-family:宋体;color:black'>。</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>修改禁用的</span><span
  lang=EN-US style='color:black'>vhost</span><span style='font-family:宋体;
  color:black'>名称</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=update&amp;data=new.ossrs.net</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=update&amp;data=new.ossrs.net'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=vhost&amp;value=ossrs.net&amp;param=update&amp;data=new.ossrs.net</span></code><span
  style='font-family:宋体;color:black'>，修改</span><span lang=EN-US
  style='color:black'>vhost</span><span style='font-family:宋体;color:black'>名称为新名称</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>需要修改的</span><span
  lang=EN-US style='color:black'>vhost</span><span style='font-family:宋体;
  color:black'>必须存在，并且是禁用状态。</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>禁用</span><span
  lang=EN-US style='color:black'>vhost</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=disable</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=disable'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=vhost&amp;value=ossrs.net&amp;param=disable</span></code><span
  style='font-family:宋体;color:black'>，禁用</span><span lang=EN-US
  style='color:black'>vhost</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>要禁用的</span><span
  lang=EN-US style='color:black'>vhost</span><span style='font-family:宋体;
  color:black'>必须存在并且是启用状态。</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US style='display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Key</span></b></p>
   </td>
   <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>feature</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>启用</span><span
  lang=EN-US style='color:black'>vhost</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>url</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=enable</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>curl</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>curl
  'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=vhost&amp;value=ossrs.net&amp;param=enable'</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>config</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>allow_update
  on;</span></code></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>params</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><code><span lang=EN-US style='color:black'>scope=vhost&amp;value=ossrs.net&amp;param=enable</span></code><span
  style='font-family:宋体;color:black'>，启用</span><span lang=EN-US
  style='color:black'>vhost</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 style='width:49.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>require</span></p>
  </td>
  <td width=488 style='width:365.65pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span style='font-family:宋体;color:black'>要启用的</span><span
  lang=EN-US style='color:black'>vhost</span><span style='font-family:宋体;
  color:black'>必须存在并且是禁用状态。</span></p>
  </td>
 </tr>
</table>

<h5><span lang=EN-US>RAW DVR</span></h5>

<p><span lang=EN-US style='font-size:10.5pt'>DVR</span><span style='font-size:
10.5pt'>操作是<span lang=EN-US>Update</span>的一个子集。</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-family:宋体'>Key</span></b></p>
   </td>
   <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-family:宋体;color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>feature</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>开启<span lang=EN-US>Vhost</span>的某个流的<span lang=EN-US>DVR</span></span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>url</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>/api/v1/raw?rpc=update&amp;scope=dvr&amp;value=ossrs.net&amp;param=enable&amp;data=live/livestream</span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>curl</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=dvr&amp;value=ossrs.net&amp;param=enable&amp;data=live/livestream'</span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>config</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>allow_update on;</span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>params</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>scope=dvr&amp;value=ossrs.net&amp;param=enable&amp;data=live/livestream</span><span
  style='font-family:宋体;color:black'>，对<span lang=EN-US>Vhost</span>的<span
  lang=EN-US>Stream</span>开启<span lang=EN-US>DVR</span></span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>require</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>必须<span lang=EN-US>Vhost</span>的<span lang=EN-US>DVR</span>是开启状态。</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
style='font-family:宋体;display:none'>&nbsp;</span></p>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#F2F2F2'>
 <thead>
  <tr>
   <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-family:宋体'>Key</span></b></p>
   </td>
   <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='font-family:宋体;color:black'>DESC</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>feature</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>关闭<span lang=EN-US>Vhost</span>的某个流的<span lang=EN-US>DVR</span></span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>url</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>/api/v1/raw?rpc=update&amp;scope=dvr&amp;value=ossrs.net&amp;param=disable&amp;data=live/livestream</span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>curl</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>curl 'http://127.0.0.1:1985/api/v1/raw?rpc=update&amp;scope=dvr&amp;value=ossrs.net&amp;param=disable&amp;data=live/livestream'</span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>config</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>allow_update on;</span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>params</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>scope=dvr&amp;value=ossrs.net&amp;param=disable&amp;data=live/livestream</span><span
  style='font-family:宋体;color:black'>，对<span lang=EN-US>Vhost</span>的<span
  lang=EN-US>Stream</span>关闭<span lang=EN-US>DVR</span></span></p>
  </td>
 </tr>
 <tr>
  <td width=76 style='width:2.0cm;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:宋体;color:black'>require</span></p>
  </td>
  <td width=478 style='width:358.6pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>必须<span lang=EN-US>Vhost</span>的<span lang=EN-US>DVR</span>是开启状态。</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h4><a name="_Toc462219522"><span lang=EN-US>WIKI</span></a></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi">https://github.com/ossrs/srs/wiki/v3_CN_HTTPApi</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097970"></a><a name="_Toc462219523"></a><a
name="_Toc456260531"><span lang=EN-US>RTMP</span></a><span style='font-family:
宋体'>测速</span></h3>

<p><span style='font-size:10.5pt'>视频很卡，播放不了，缓冲区突然很大，推流上不来，都有可能是带宽过低，<span
lang=EN-US>SRS</span>支持测试客户端到服务器的带宽。</span></p>

<h4><a name="_Toc462219524"><span lang=EN-US>SRS</span></a><span
style='font-family:宋体'>配置</span></h4>

<p><span lang=EN-US style='font-size:10.5pt'>SRS</span><span style='font-size:
10.5pt'>配置一般是单独加一个<span lang=EN-US>vhost</span>支持测速。<span lang=EN-US>SRS</span>的配置<code><span
lang=EN-US>conf/bandwidth.conf</span></code>。譬如：</span></p>

<pre><span lang=EN-US style='font-size:10.5pt'>listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;1935<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>vhost __defaultVhost__ {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>}</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>&nbsp;</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>vhost bandcheck.srs.com {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; chunk_size&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 65000<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; bandcheck {</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; key&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span
class=pl-pds>&quot;</span><span class=pl-s>35c9b402c12a7246868752e2878f7e0e</span><span
class=pl-pds>&quot;</span><span class=pl-k>;</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; interval&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 30<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; limit_kbps&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 4000<span
class=pl-k>;</span></span></pre><pre><span lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp;&nbsp; }</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>}</span></pre>

<p><span style='font-size:10.5pt'>其中：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>key</span><span
     style='font-family:宋体'>：服务器的</span><span lang=EN-US>key</span><span
     style='font-family:宋体'>，若客户端给出的</span><span lang=EN-US>key</span><span
     style='font-family:宋体'>和配置的不一致，断开连接。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>interval</span><span
     style='font-family:宋体'>：测速的间隔，单位为秒，可为小数。若连续发起测速，时间间隔小于</span><span
     lang=EN-US>interval</span><span style='font-family:宋体'>，服务器拒绝连接。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>limit_kbps</span><span
     style='font-family:宋体'>：测速的最大带宽，即可以测出来的最大带宽，防止服务器收到攻击。</span></li>
</ul>

<p><strong><span style='font-size:10.5pt;font-family:宋体'>假设服务器的<span
lang=EN-US>IP</span>是：<span lang=EN-US>192.168.1.170</span></span></strong></p>

<h4><a name="_Toc462219525"><span lang=EN-US>Flash</span></a><span
style='font-family:宋体'>测速工具</span></h4>

<p><span style='font-size:10.5pt'>启动后用带宽测试客户端就可以查看：</span><span lang=EN-US><a
href="http://winlinvip.github.io/srs.release/trunk/research/players/srs_bwt.html?server=192.168.1.170"><span
style='font-size:10.5pt'>http://winlinvip.github.io/srs.release/trunk/research/players/srs_bwt.html?server=192.168.1.170</span></a></span></p>

<p><span style='font-size:10.5pt'>备注：请将所有实例的<span lang=EN-US>IP</span>地址<span
lang=EN-US>192.168.1.170</span>都换成部署的服务器<span lang=EN-US>IP</span>地址。</span></p>

<p><span style='font-size:10.5pt'>检测完毕后会提示带宽，譬如：</span></p>

<pre><span style='font-size:10.5pt'>检测结束<span lang=EN-US>: 192.168.1.170 </span>上行<span
lang=EN-US>: 1965 kbps </span>下行<span lang=EN-US>: 3631 kbps </span>测试时间<span
lang=EN-US>: 6.0 </span>秒</span></pre><pre><span lang=EN-US style='font-size:
10.5pt'>server:SRS 0.9.156 (github.com/winlinvip/simple-rtmp-server), </span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>authors:winlin,wenjie.zhao, srs_id:123, srs_pid:32057, ip:192.168.1.170</span></pre>

<h4><a name="_Toc462219526"><span style='font-family:宋体'>测速库</span></a></h4>

<p><span style='font-size:10.5pt'>我提供了<span lang=EN-US>AS</span>和<span
lang=EN-US>JS</span>的库，可以直接调用来和服务器测速。</span></p>

<p><span lang=EN-US style='font-size:10.5pt'>AS</span><span style='font-size:
10.5pt'>的库，直接拷贝文件<code><span lang=EN-US>SrsBandwidth.as</span></code>到工程，调用即可（参考注释说明）：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>AS</span><span
     style='font-family:宋体'>库对象：</span><span lang=EN-US><a
     href="https://github.com/ossrs/srs/blob/master/trunk/research/players/srs_bwt/src/SrsBandwidth.as">SrsBandwidth.as</a></span><span
     lang=EN-US> </span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>AS</span><span
     style='font-family:宋体'>调用对象（主对象）：</span><span lang=EN-US><a
     href="https://github.com/ossrs/srs/blob/master/trunk/research/players/srs_bwt/src/srs_bwt.as">srs_bwt.as</a></span><span
     style='font-family:宋体'>，如何调用</span><code><span lang=EN-US>SrsBandwidth.as</span></code><span
     style='font-family:宋体'>的实例。</span></li>
</ul>

<p><span lang=EN-US style='font-size:10.5pt'>JS</span><span style='font-size:
10.5pt'>的库，需要拷贝<code><span lang=EN-US>srs_bwt.swf</span></code>和<code><span
lang=EN-US>srs.bandwidth.js</span></code>，调用方法参考<span lang=EN-US>js</span>说明：</span></p>

<ul type=disc>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>JS</span><span
     style='font-family:宋体'>库对象：</span><span lang=EN-US><a
     href="https://github.com/ossrs/srs/blob/master/trunk/research/players/srs_bwt/src/srs.bandwidth.js">srs.bandwidth.js</a></span><span
     lang=EN-US> </span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>JS</span><span
     style='font-family:宋体'>调用对象（页面）：</span><span lang=EN-US><a
     href="https://github.com/ossrs/srs/blob/master/trunk/research/players/srs_bwt.html">srs_bwt.html</a></span><span
     style='font-family:宋体'>，如何调用</span><code><span lang=EN-US>srs.bandwidth.js</span></code><span
     style='font-family:宋体'>的实例。</span></li>
</ul>

<p><span style='font-size:10.5pt'>备注：<span lang=EN-US>JS</span>需要调用<span
lang=EN-US>swf</span>导出的<span lang=EN-US>js</span>函数，由<span lang=EN-US>Flash</span>发送<span
lang=EN-US>RTMP</span>包测速，因此<span lang=EN-US>js</span>库依赖于<span lang=EN-US>as</span>。可以导入<span
lang=EN-US>Flex</span>工程自己编译，或者使用已经编译好的</span><span lang=EN-US><a
href="https://github.com/ossrs/srs/blob/master/trunk/research/players/srs_bwt/release/srs_bwt.swf"><span
style='font-size:10.5pt'>srs_bwt.swf</span></a></span></p>

<h4><a name="_Toc462219527"><span lang=EN-US>Linux</span></a><span
style='font-family:宋体'>工具测速</span></h4>

<p><span style='font-size:10.5pt'>另外，<span lang=EN-US>SRS</span>还提供了带宽检测命令行工具：</span></p>

<pre><span lang=EN-US style='font-size:10.5pt'>[winlin@dev6 srs]$ <span
class=pl-c1>cd</span> objs/research/librtmp/</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>[winlin@dev6 librtmp]$ ./srs_bandwidth_check </span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>RTMP bandwidth check/test with server.</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>Usage: ./srs_bandwidth_check <span
class=pl-k>&lt;</span>rtmp_url<span class=pl-k>&gt;</span></span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp; rtmp_url&nbsp;&nbsp;&nbsp;&nbsp; RTMP bandwidth url to check. format: rtmp://server:port/app<span
class=pl-k>?</span>key=xxx,vhost=xxx</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>For example:</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>&nbsp;&nbsp; ./srs_bandwidth_check rtmp://127.0.0.1:1935/app<span
class=pl-k>?</span>key=35c9b402c12a7246868752e2878f7e0e,vhost=bandcheck.srs.com</span></pre><pre><span
lang=EN-US style='font-size:10.5pt'>&nbsp;&nbsp; ./srs_bandwidth_check rtmp://127.0.0.1:1935/app<span
class=pl-k>?</span>key=35c9b402c12a7246868752e2878f7e0e,vhost=bandcheck.srs.com<span
class=pl-k>&gt;</span>/dev/null</span></pre><pre><span lang=EN-US
style='font-size:10.5pt'>@remark, output text to stdout, <span class=pl-k>while</span> json to stderr.</span></pre>

<p><span style='font-size:10.5pt'>直接执行将打印文本和<span lang=EN-US>json</span>信息：</span></p>

<pre><code><span lang=EN-US style='font-size:10.5pt'>[winlin@dev6 librtmp]$ ./srs_bandwidth_check rtmp://127.0.0.1:1935/app?key=35c9b402c12a7246868752e2878f7e0e,vhost=bandcheck.srs.com</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>RTMP bandwidth check/test with server.</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>srs(simple-rtmp-server) client librtmp library.</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>version: 0.9.158</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>bandwidth check/test url: rtmp://127.0.0.1:1935/app?key=35c9b402c12a7246868752e2878f7e0e,vhost=bandcheck.srs.com</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>simple handshake success</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>connect vhost/app success</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>bandwidth check/test success</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>SRS 0.9.158 (github.com/winlinvip/simple-rtmp-server), winlin,wenjie.zhao</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>127.0.0.1, 0.9.158, srs_pid=15264, srs_id=107</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>duration: 6395ms(3165+3148)</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>play: 3578kbps</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>publish: 4035kbps</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>terminate with ret=0</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&nbsp;</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>{&quot;code&quot;:0,</span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;srs_server&quot;:&quot;SRS 0.9.158 (github.com/winlinvip/simple-rtmp-server)&quot;, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;srs_primary_authors&quot;:&quot;winlin,wenjie.zhao&quot;, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;srs_server_ip&quot;:&quot;127.0.0.1&quot;, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;srs_version&quot;:&quot;0.9.158&quot;, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;srs_pid&quot;:15264, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;srs_id&quot;:107, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;duration&quot;:6395, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;play_duration&quot;:3165, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;play_kbps&quot;:3148, </span></code></pre><pre><code><span
lang=EN-US style='font-size:10.5pt'>&quot;publish_kbps&quot;:3578}</span></code></pre>

<p>可以只打印<span lang=EN-US>json</span>信息，将<span lang=EN-US>stdout</span>定向到<span
lang=EN-US>/dev/null</span>：</p>

<pre><code><span lang=EN-US>[winlin@dev6 librtmp]$ ./srs_bandwidth_check rtmp://127.0.0.1:1935/app?key=35c9b402c12a7246868752e2878f7e0e,vhost=bandcheck.srs.com&gt;/dev/null </span></code></pre><pre><code><span
lang=EN-US>{&quot;code&quot;:0,</span></code></pre><pre><code><span lang=EN-US>&quot;srs_server&quot;:&quot;SRS 0.9.158 (github.com/winlinvip/simple-rtmp-server)&quot;, </span></code></pre><pre><code><span
lang=EN-US>&quot;srs_primary_authors&quot;:&quot;winlin,wenjie.zhao&quot;, </span></code></pre><pre><code><span
lang=EN-US>&quot;srs_server_ip&quot;:&quot;127.0.0.1&quot;, </span></code></pre><pre><code><span
lang=EN-US>&quot;srs_version&quot;:&quot;0.9.158&quot;, </span></code></pre><pre><code><span
lang=EN-US>&quot;srs_pid&quot;:15264, </span></code></pre><pre><code><span
lang=EN-US>&quot;srs_id&quot;:109, </span></code></pre><pre><code><span
lang=EN-US>&quot;duration&quot;:6354, </span></code></pre><pre><code><span
lang=EN-US>&quot;play_duration&quot;:3092, </span></code></pre><pre><code><span
lang=EN-US>&quot;play_kbps&quot;:3177, </span></code></pre><pre><code><span
lang=EN-US>&quot;publish_kbps&quot;:3662}</span></code></pre>

<h4><a name="_Toc462219528"><span lang=EN-US>WIKI</span></a></h4>

<p class=MsoNormal><span lang=EN-US><a
href="https://github.com/ossrs/srs/wiki/v1_CN_BandwidthTestTool">https://github.com/ossrs/srs/wiki/v1_CN_BandwidthTestTool</a></span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h2><a name="_Toc26097971"></a><a name="_Toc462219529"><span style='font-family:
宋体'>其他功能</span></a></h2>

<p><span lang=EN-US>SRS</span>提供了一些特殊的配置，主要用来和各种系统对接的设置。</p>

<h3><a name="_Toc26097972"></a><a name="_Toc462219530"><span lang=EN-US>Send
Minimal Interval</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # for play client, both RTMP and other stream clients,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # for instance, the HTTP FLV stream clients.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; play {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # the minimal packets send interval in ms,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # used to control the ndiff of stream by srs_rtmp_dump,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # for example, some device can only accept some stream which</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # delivery packets in constant interval(not cbr).</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # @remark 0 to disable the minimal interval.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # @remark &gt;0 to make the srs to send message one by one.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # @remark user can get the right packets interval in ms by srs_rtmp_dump.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: 0</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; send_min_interval&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 10.0;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097973"></a><a name="_Toc462219531"><span lang=EN-US>Reduce
Sequence Header</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # for play client, both RTMP and other stream clients,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # for instance, the HTTP FLV stream clients.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; play {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # whether reduce the sequence header,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # for some client which cannot got duplicated sequence header,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # while the sequence header is not changed yet.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: off</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; reduce_sequence_header&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097974"></a><a name="_Toc462219532"><span lang=EN-US>Publish
1st Packet Timeout</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # the config for FMLE/Flash publisher, which push RTMP to SRS.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; publish {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # the 1st packet timeout in ms for encoder.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: 20000</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; firstpkt_timeout&nbsp;&nbsp;&nbsp; 20000;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097975"></a><a name="_Toc462219533"><span lang=EN-US>Publish
Normal Timeout</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # the config for FMLE/Flash publisher, which push RTMP to SRS.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; publish {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # the normal packet timeout in ms for encoder.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: 5000</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; normal_timeout&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 7000;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097976"></a><a name="_Toc462219534"><span lang=EN-US>Debug
SRS Upnode</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # when upnode(forward to, edge push to, edge pull from) is srs,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # it's strongly recommend to open the debug_srs_upnode,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # when connect to upnode, it will take the debug info, </span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;# for example, the id, source id, pid.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # please see: https://github.com/ossrs/srs/wiki/v1_CN_SrsLog</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # default: on</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; debug_srs_upnode&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097977"></a><a name="_Toc462219535"><span lang=EN-US>UTC
Time</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'># whether use utc_time to generate the time struct,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'># if off, use localtime() to generate it,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'># if on, use gmtime() instead, which use UTC time.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'># default: off</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>utc_time&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;off;</span></code></pre>

<h3><a name="_Toc26097978"></a><a name="_Toc462219536"><span lang=EN-US>HLS TS
Floor</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; hls {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # whether use floor for the hls_ts_file path generation.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # if on, use floor(timestamp/hls_fragment) as the variable [timestamp],</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; and use enahanced algorithm to calc deviation for segment.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # @remark when floor on, recommend the hls_segment&gt;=2*gop.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: off</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; hls_ts_floor&nbsp;&nbsp;&nbsp; off;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097979"></a><a name="_Toc462219537"><span lang=EN-US>HLS
Wait Keyframe</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; hls {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # whether wait keyframe to reap segment,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # if off, reap segment when duration exceed the fragment,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # if on, reap segment when duration exceed and got keyframe.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: on</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; hls_wait_keyframe&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097980"></a><a name="_Toc462219538"><span lang=EN-US>HttpHooks
On HLS Notify</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; http_hooks {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # when srs reap a ts file of hls, call this hook,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # used to push file to cdn network, by get the ts file from cdn network.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # so we use HTTP GET and use the variable following:</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [app], replace with the app.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [stream], replace with the stream.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [ts_url], replace with the ts url.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # ignore any return data of server.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # @remark random select a url to report, not report all.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; on_hls_notify&nbsp;&nbsp; http://127.0.0.1:8085/api/v1/hls/[app]/[stream][ts_url];</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097981"></a><a name="_Toc462219539"><span lang=EN-US>TCP
NoDelay</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # whether enable the TCP_NODELAY</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # if on, set the nodelay of fd by setsockopt</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # default: off</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; tcp_nodelay&nbsp;&nbsp;&nbsp;&nbsp; on;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097982"></a><a name="_Toc462219540"><span lang=EN-US>ATC Auto</span></a></h3>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # for play client, both RTMP and other stream clients,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # for instance, the HTTP FLV stream clients.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; play {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # whether enable the auto atc,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # if enabled, detect the bravo_atc=&quot;true&quot; in onMetaData packet,</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # set atc to on if matched.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # always ignore the onMetaData if atc_auto is off.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: off</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; atc_auto&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; off;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<h3><a name="_Toc26097983"></a><a name="_Toc462219541"><span lang=EN-US>NGINX
RTMP EXEC</span></a></h3>

<p><span lang=EN-US style='font-size:10.5pt'>NGINX-RTMP</span><span
style='font-size:10.5pt'>支持的<span lang=EN-US>EXEC</span>方式，参考</span><span
lang=EN-US><a
href="https://github.com/arut/nginx-rtmp-module/wiki/Directives#exec"><span
style='font-size:10.5pt'>nginx exec</span></a></span><span style='font-size:
10.5pt'>，<span lang=EN-US>SRS</span>只支持常用的几种。下面是<span lang=EN-US>exec</span>的支持情况：</span></p>

<ol start=1 type=1>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>exec/exec_publish:
     </span><span style='font-family:宋体'>当发布流时调用，支持。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>exec_pull: </span><span
     style='font-family:宋体'>不支持。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>exec_play: </span><span
     style='font-family:宋体'>不支持。</span></li>
 <li class=MsoNormal style='text-align:left'><span lang=EN-US>exec_record_done:
     </span><span style='font-family:宋体'>不支持。</span></li>
</ol>

<h4><a name="_Toc462219542"><span lang=EN-US>Config</span></a></h4>

<p><span lang=EN-US style='font-size:9.0pt'>SRS EXEC</span><span
style='font-size:9.0pt'>的配置参考<code><span lang=EN-US>conf/exec.conf</span></code>，如下：</span></p>

<pre><code><span lang=EN-US style='font-size:9.0pt'>vhost __defaultVhost__ {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; # the exec used to fork process when got some event.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; exec {</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # whether enable the exec.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # default: off.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; enabled&nbsp;&nbsp;&nbsp;&nbsp; off;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # when publish stream, exec the process with variables:</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [vhost] the input stream vhost.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [port] the intput stream port.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [app] the input stream app.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [stream] the input stream name.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [engine] the tanscode engine name.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # other variables for exec only:</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;#&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [url] the rtmp url which trigger the publish.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [tcUrl] the client request tcUrl.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [swfUrl] the client request swfUrl.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; #&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [pageUrl] the client request pageUrl.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # @remark empty to ignore this exec.</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; publish&nbsp;&nbsp;&nbsp;&nbsp; ./objs/ffmpeg/bin/ffmpeg -f flv -i [url] -c copy -y ./[stream].flv;</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>&nbsp;&nbsp;&nbsp; }</span></code></pre><pre><code><span
lang=EN-US style='font-size:9.0pt'>}</span></code></pre>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h2><a name="_Toc26097984"></a><a name="_Toc462219543"><span lang=EN-US>SRS</span></a><span
style='font-family:宋体'>与其他流媒体比较</span></h2>

<h3><a name="_Toc26097985"></a><a name="_Toc462219544"><span style='font-family:
宋体'>流发分</span> <span lang=EN-US>Stream Delivery</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>RTMP</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HLS</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HDS</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Experiment</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HTTP FLV</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HLS(aonly)</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HTTP Server</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc26097986"></a><a name="_Toc462219545"><span style='font-family:
宋体;color:white'>集群</span> <span lang=EN-US>Cluster</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td width=72 style='width:54.1pt;padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>RTMP Edge</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td width=72 style='width:54.1pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>RTMP Backup</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td width=72 style='width:54.1pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>VHOST</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td width=72 style='width:54.1pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Reload</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td width=72 style='width:54.1pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Forward</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td width=72 style='width:54.1pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ATC</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td width=72 style='width:54.1pt;padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc26097987"></a><a name="_Toc462219546"><span style='font-family:
宋体;color:white'>流处理服务</span> <span lang=EN-US>Stream Service</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>DVR</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Transcode</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HTTP API</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HTTP hooks</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>GopCache</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Security</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Token Traverse</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc26097988"></a><a name="_Toc462219547"><span lang=EN-US
style='color:white'>Efficiency</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Concurrency</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>7.5k</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>3k</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>2k</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>2k</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>3k</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>MultipleProcess</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Experiment</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>RTMP Latency</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>0.1s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>3s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>3s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>3s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>3s</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>HLS Latency</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>10s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>30s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>30s</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>30s</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc26097989"></a><a name="_Toc462219548"><span lang=EN-US
style='color:white'>Stream Caster</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Ingest</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Push MPEGTS</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Experiment</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Push RTSP</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Experiment</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Push HTTP FLV</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Experiment</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc26097990"></a><a name="_Toc462219549"><span lang=EN-US
style='color:white'>Debug System</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>BW check</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Tracable Log</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc26097991"></a><a name="_Toc462219550"><span lang=EN-US
style='color:white'>Docs</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Demos</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>WIKI(EN+CN)</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>EN only</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
 </tr>
</table>

<h3><a name="_Toc26097992"></a><a name="_Toc462219551"><span lang=EN-US
style='color:white'>Others</span></a></h3>

<table class=MsoNormalTable border=0 cellspacing=30 cellpadding=0
 style='background:#E5E5E5'>
 <thead>
  <tr>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US>Feature</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>SRS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>NGINX</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>CRTMPD</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>FMS</span></b></p>
   </td>
   <td style='padding:.75pt .75pt .75pt .75pt'>
   <p class=MsoNormal align=center style='text-align:center'><b><span
   lang=EN-US style='color:black'>WOWZA</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>ARM/MIPS</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
 <tr>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Client Library</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>Stable</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
  <td style='padding:.75pt .75pt .75pt .75pt'>
  <p class=MsoNormal><span lang=EN-US style='color:black'>X</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h3><a name="_Toc26097993"></a><a name="_Toc462219552"><span style='font-family:
宋体;color:black;background:white'>市面主要的流媒体服务器对比</span></a></h3>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>目前市面上主流的流媒体服务器，有以</span><span
lang=EN-US>Adobe&nbsp;FMS</span><span style='font-family:宋体'>、</span><span
lang=EN-US>Real&nbsp;Helix</span><span style='font-family:宋体'>、</span><span
lang=EN-US>Wowza</span><span style='font-family:宋体'>为代表的第一代产品，它们的特点是单进程多线程。基于</span><span
lang=EN-US>Linux2.7&nbsp;epoll</span><span style='font-family:宋体'>技术，出现了以多进程单线程为特点的第二代流媒体服务器，</span><span
lang=EN-US>NginxRTMP</span><span style='font-family:宋体'>、</span><span
lang=EN-US>Crtmpd</span><span style='font-family:宋体'>为其优秀的代表，另外还有基于</span><span
lang=EN-US>JAVA</span><span style='font-family:宋体'>的流媒体祖先</span><span
lang=EN-US>Red5</span><span style='font-family:宋体'>等。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>开源流媒体服务器</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>（</span><span lang=EN-US>Simple&nbsp;RTMP&nbsp;Server</span><span
style='font-family:宋体'>），凭借其功能强大、轻量易用、特别适合互动直播等诸多特点备受海内外视频从业者的青睐。蓝汛</span><span
lang=EN-US>Chiancache</span><span style='font-family:宋体'>曾用</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>承载其直播边缘分发业务，高升</span><span
lang=EN-US>CDN</span><span style='font-family:宋体'>基于</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>搭建其流媒体基础平台，其它还有赛维安讯、</span><span lang=EN-US>VeryCDN</span><span
style='font-family:宋体'>、</span><span lang=EN-US>VeryCloud</span><span
style='font-family:宋体'>、云博视等也将</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>应用到了自身的业务当中。各家视频云、云计算平台在源站的对接上也非常注重对</span><span
lang=EN-US>SRS</span><span style='font-family:宋体'>的支持。</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>作为纯国产的开源</span><span lang=EN-US>Server</span><span
style='font-family:宋体'>，在中国流媒体业界实属难能可贵。</span></p>

<p class=MsoNormal align=center style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:center;line-height:15.75pt'><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'><img border=0
width=698 height=678 id="图片 16" src="srs_wiki.files/image008.jpg"
alt="https://h5.weiyun.com/tx_tls_gate=img7.wtoutiao.com/?url=http://mmbiz.qpic.cn/mmbiz/ibqXNcZwc8ZficAW5LaxzmE8WU7RSHXA8zy8gXvr2LPX5gRznHLTGYyUwuSfREpQ8gBM3Y6p6UT0WXkAxL2fx4mQ/0?wx_fmt=jpeg"></span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>BMS</span><span
style='font-family:宋体'>（</span><span lang=EN-US>Bravo Media Server</span><span
style='font-family:宋体'>）是</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>的商业版，</span><span lang=EN-US>BMS</span><span
style='font-family:宋体'>在</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>基础上增强了</span><span lang=EN-US>11</span><span
style='font-family:宋体'>项大功能，新增了</span><span lang=EN-US>9</span><span
style='font-family:宋体'>个大功能：</span> <b><span style='font-family:宋体;color:red'>注意</span><span
lang=EN-US style='color:red'>:</span></b><b><span style='font-family:宋体;
color:red'>表中比较是</span><span lang=EN-US style='color:red'>srs 1.0 release</span></b><b><span
style='font-family:宋体;color:red'>版本，有些功能在</span><span lang=EN-US
style='color:red'>srs2.0,srs3.0</span></b><b><span style='font-family:宋体;
color:red'>中以及实现，只是没有</span><span lang=EN-US style='color:red'>release</span></b><b><span
style='font-family:宋体;color:red'>版本，</span><span lang=EN-US style='color:red'>
BMS</span></b><b><span style='font-family:宋体;color:red'>是结合</span><span
lang=EN-US style='color:red'>srs2.0 </span></b><b><span style='font-family:
宋体;color:red'>与</span><span lang=EN-US style='color:red'>srs3.0</span></b><b><span
style='font-family:宋体;color:red'>是在这个基础出发出来的。</span></b></p>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
lang=EN style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span><span
style='font-size:12.0pt;font-family:宋体;color:#333333'>和</span><span lang=EN
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
style='font-size:12.0pt;font-family:宋体;color:#333333'>的主要区别如下：</span></p>

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0 width="100%"
 style='width:100.0%;border-collapse:collapse'>
 <thead>
  <tr>
   <td style='border:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Feature</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Remark</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>级别</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>工业级</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>工业级</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>发行版本都是工业级集群标准</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>开源</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>是</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>否</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span><span
  style='font-family:宋体;color:#333333'>为闭源商业软件，提供售前咨询和售后服务，</span><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'><br>
  </span><span style='font-family:宋体;color:#333333'>以及定制化开发，系统对接等</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>发行版</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>1.0</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>3.0</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
  style='font-family:宋体;color:#333333'>目前发行版为</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>1.0</span><span
  style='font-family:宋体;color:#333333'>，</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS2</span><span
  style='font-family:宋体;color:#333333'>为</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>alpha</span><span
  style='font-family:宋体;color:#333333'>测试版。</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'><br>
  BMS</span><span style='font-family:宋体;color:#333333'>合并了</span><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS2</span><span
  style='font-family:宋体;color:#333333'>和</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS3</span><span
  style='font-family:宋体;color:#333333'>的功能，为发行版</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>周期</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>1-2</span><span
  style='font-family:宋体;color:#333333'>年</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>3-6</span><span
  style='font-family:宋体;color:#333333'>个月</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
  style='font-family:宋体;color:#333333'>的版本发行周期为</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>1</span><span
  style='font-family:宋体;color:#333333'>到</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>2</span><span
  style='font-family:宋体;color:#333333'>年</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>代码量</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>5.95</span><span
  style='font-family:宋体;color:#333333'>万行</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>13.3</span><span
  style='font-family:宋体;color:#333333'>万行</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>包含服务器的注释和单元测试</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'><br>
  BMS</span><span style='font-family:宋体;color:#333333'>是</span><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span><span
  style='font-family:宋体;color:#333333'>代码量的</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>2.23</span><span
  style='font-family:宋体;color:#333333'>倍。</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>自动测试</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>无</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span><span
  style='font-family:宋体;color:#333333'>包含自动化测试系统，每次提交自动回归测试</span></p>
  </td>
 </tr>
</table>

<p class=MsoNoSpacing><span lang=EN style='color:black'>BMS</span><span
style='font-family:宋体'>除了有</span><span lang=EN>SRS</span><span
style='font-family:宋体'>的</span><span lang=EN>10</span><span style='font-family:
宋体'>个基础功能，还增强了</span><span lang=EN>13</span><span style='font-family:宋体'>项大功能，新增了</span><span
lang=EN>22</span><span style='font-family:宋体'>个大功能。详细对比如下（注意对比的是发行版，即</span><span
lang=EN>SRS1</span><span style='font-family:宋体'>和</span><span lang=EN>BMS3</span><span
style='font-family:宋体'>）。</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>以下是</span><span lang=EN>BMS</span><span
style='font-family:宋体'>和</span><span lang=EN>SRS</span><span style='font-family:
宋体'>都有的功能：</span></p>

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0 width="100%"
 style='width:100.0%;border-collapse:collapse'>
 <thead>
  <tr>
   <td style='border:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Feature</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Remark</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP</span><span
  style='font-family:宋体;color:#333333'>回调</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>和外部业务系统对接</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>测速</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持服务器上行和下行速度测试</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>TS</span><span
  style='font-family:宋体;color:#333333'>矫正</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持时间戳矫正，避免重推和跳变引起播放器卡死</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Gop</span><span
  style='font-family:宋体;color:#333333'>合并</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>按照</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>GOP</span><span
  style='font-family:宋体;color:#333333'>输出切片</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>ATC</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持绝对时间戳</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>边缘</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>源站和边缘组成流媒体分发集群</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>日志</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>提供可追溯的排错日志</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>采集</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>将外部流采集到服务器</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>转发</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>将流转发给其他服务器</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HDS</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>实验性</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>实验性</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Adobe HDS</span><span
  style='font-family:宋体;color:#333333'>分发</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-size:12.0pt;font-family:宋体;color:#333333'>以下为</span><span lang=EN
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span><span
style='font-size:12.0pt;font-family:宋体;color:#333333'>增强的功能：</span></p>

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0 width="100%"
 style='width:100.0%;border-collapse:collapse'>
 <thead>
  <tr>
   <td style='border:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Feature</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Remark</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>输入</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP, <b><i>FLV,
  RTSP, UDP</i></b> </span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>推流到服务器的输入方式</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>输出</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP, HLS</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP, HLS,
  <b><i>FLV, TS, MP3, HLS+, FLS</i></b> </span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>服务器分发给客户端的方式</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>边缘回源</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP, <b><i>FLV,
  HLS, HLS CUP</i></b> </span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>边缘支持以</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP</span><span
  style='font-family:宋体;color:#333333'>或</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP FLV/HLS</span><span
  style='font-family:宋体;color:#333333'>方式回源</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>DVR</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>FLV</span><span
  style='font-family:宋体;color:#333333'>文件</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>对接观止收录系统</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持录制</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP</span><span
  style='font-family:宋体;color:#333333'>到</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>FLV</span><span
  style='font-family:宋体;color:#333333'>文件</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>低延迟</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP(3s+)</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP/<i>FLV(1s+)</i></span></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>低延迟模式</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>转码</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>FFMPEG</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>对接观止转码云</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>转码消耗非常多的系统资源</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP API</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>简版</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>完善的</span></i></b><b><i><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>API</span></i></b><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>API</span><span
  style='font-family:宋体;color:#333333'>为服务器提供给外部的接口</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>下行并发</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>2.7K</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>7K</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>下行</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP/FLV</span><span
  style='font-family:宋体;color:#333333'>的并发</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>上行并发</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>1.2K</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>4K</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>上行推流</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP</span><span
  style='font-family:宋体;color:#333333'>的并发</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>热备</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>RTMP, <b><i>HLS</i></b>
  </span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>边缘在上层服务器故障时，切换到备用服务器</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>实验性</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>商用服务器</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>内置</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP</span><span
  style='font-family:宋体;color:#333333'>服务器，实现</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP</span><span
  style='font-family:宋体;color:#333333'>流、</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>API</span><span
  style='font-family:宋体;color:#333333'>、内存</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>的分发</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Gop Cache</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>多</span></i></b><b><i><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>GOP</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>缓存最近的</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>Gop</span><span
  style='font-family:宋体;color:#333333'>，让播放器快速启动</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>(&lt;0.1s)</span><span
  style='font-family:宋体;color:#333333'>，</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>cache</span><span
  style='font-family:宋体;color:#333333'>多个</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>gop</span><span
  style='font-family:宋体;color:#333333'>，更快启动</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>回源切换</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>错误时切换</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>错误时切换，</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'><br>
  <b><i>API</i></b></span><b><i><span style='font-family:宋体;color:#333333'>无缝切换</span></i></b><span
  style='font-family:"Segoe UI",sans-serif;color:#333333'> </span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS/BMS</span><span
  style='font-family:宋体;color:#333333'>在错误时切换源站，</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>API</span><span
  style='font-family:宋体;color:#333333'>调用切换源站</span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
style='font-size:12.0pt;font-family:宋体;color:#333333'>以下为</span><span lang=EN
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span><span
style='font-size:12.0pt;font-family:宋体;color:#333333'>新增的功能：</span></p>

<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0 width="100%"
 style='width:100.0%;border-collapse:collapse'>
 <thead>
  <tr>
   <td style='border:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Feature</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>SRS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>BMS</span></b></p>
   </td>
   <td style='border:solid #DDDDDD 1.0pt;border-left:none;background:white;
   padding:4.5pt 9.75pt 4.5pt 9.75pt'>
   <p class=MsoNormal align=center style='margin-bottom:12.0pt;text-align:center'><b><span
   lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Remark</span></b></p>
   </td>
  </tr>
 </thead>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>源站集群</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>无</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>基于</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>Redis</span><span
  style='font-family:宋体;color:#333333'>的源站集群，边缘自动负载均衡和容错</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS+</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>无</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持流模式分发</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>切片，边缘转封装，同一套流媒体分发（不用走</span><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP</span><span
  style='font-family:宋体;color:#333333'>集群）</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>时移</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>无</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>对接观止时移系统</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>在时移的基础上可以做高级收录和</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>P2P</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>CDN</span><span
  style='font-family:宋体;color:#333333'>预推</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>无</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>将</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>预推到</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>CDN</span><span
  style='font-family:宋体;color:#333333'>节点</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>计费</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>无</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持对接计费系统</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>计费系统做定制和对接</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>纯音频</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b><b><i><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>MP3</span></i></b><b><i><span
  style='font-family:宋体;color:#333333'>和</span></i></b><b><i><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>AAC</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>纯音频即没有视频流</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Vhost</span><span
  style='font-family:宋体;color:#333333'>转换</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>边缘回源，以及复杂业务系统需要转换</span><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Vhost</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Kafka</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>对接到</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>Kafka</span><span
  style='font-family:宋体;color:#333333'>大数据集群，参考</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>BIG</span><span
  style='font-family:宋体;color:#333333'>技术</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>动态配置</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>通过</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HTTP API</span><span
  style='font-family:宋体;color:#333333'>从业务系统动态加载配置</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>日志切割</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>nginx</span><span
  style='font-family:宋体;color:#333333'>风格的日志切割</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>LogRotate</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS CUP</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>多源站并发回源</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>毫秒开</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>FastStartup</span><span
  style='font-family:宋体;color:#333333'>毫秒级灌满播放器缓冲区，比秒开更快</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>内存转储</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持分析当前服务器的内存消耗</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>MemoryApi</span><span
  style='font-family:宋体;color:#333333'>，方便运维</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>软矩阵</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>M</span><span
  style='font-family:宋体;color:#333333'>组每组</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>N</span><span
  style='font-family:宋体;color:#333333'>路输入一路输出，即</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>M*N</span><span
  style='font-family:宋体;color:#333333'>输入</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>M</span><span
  style='font-family:宋体;color:#333333'>输出</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>延播</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持延迟播出</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>(</span><span
  style='font-family:宋体;color:#333333'>流审核</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>)</span><span
  style='font-family:宋体;color:#333333'>和时移，支持内存和磁盘</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>FLS</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>FLV Live Streaming</span><span
  style='font-family:宋体;color:#333333'>将</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>HLS</span><span
  style='font-family:宋体;color:#333333'>的</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>TS</span><span
  style='font-family:宋体;color:#333333'>换成</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>FLV</span><span
  style='font-family:宋体;color:#333333'>切片，去掉</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>M3u8</span><span
  style='font-family:宋体;color:#333333'>索引</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>Security</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>支持</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>Referer</span><span
  style='font-family:宋体;color:#333333'>和</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>Token</span><span
  style='font-family:宋体;color:#333333'>防盗链，踢流和禁播等</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>BAR</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>已规划</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持应用层回源智能路由</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>截图</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>已规划</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持快速截图</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>Snapshot</span><span
  style='font-family:宋体;color:#333333'>，供鉴黄和预览等</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>音频转码</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>已规划</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>AT</span><span
  style='font-family:宋体;color:#333333'>音频转码，</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>speex</span><span
  style='font-family:宋体;color:#333333'>转</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>aac</span><span
  style='font-family:宋体;color:#333333'>，拓展</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>flash</span><span
  style='font-family:宋体;color:#333333'>页面推流方式</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>混音</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>已规划</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>AM</span><span
  style='font-family:宋体;color:#333333'>多路音频混合，支持连麦和会议等业务</span></p>
  </td>
 </tr>
 <tr>
  <td style='border:solid #DDDDDD 1.0pt;border-top:none;background:white;
  padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  lang=EN-US style='font-family:"Segoe UI",sans-serif;color:#333333'>UDP</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>不支持</span></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><b><i><span
  style='font-family:宋体;color:#333333'>已规划</span></i></b></p>
  </td>
  <td style='border-top:none;border-left:none;border-bottom:solid #DDDDDD 1.0pt;
  border-right:solid #DDDDDD 1.0pt;background:white;padding:4.5pt 9.75pt 4.5pt 9.75pt'>
  <p class=MsoNormal align=left style='margin-bottom:12.0pt;text-align:left'><span
  style='font-family:宋体;color:#333333'>支持</span><span lang=EN-US
  style='font-family:"Segoe UI",sans-serif;color:#333333'>UDP</span><span
  style='font-family:宋体;color:#333333'>传输，更低级别的系统延迟</span></p>
  </td>
 </tr>
</table>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体;
color:black'>流媒体</span><span lang=EN-US>Server</span><span style='font-family:
宋体'>的话说来也不短，上述列举的目前市面上主流流媒体服务器中，有名副其实的先烈</span><span lang=EN-US>RED5</span><span
style='font-family:宋体'>，有生不逢时的</span><span lang=EN-US>CRTMPD</span><span
style='font-family:宋体'>，都未大规模商用就不过于讨论了。其中应用最为广泛莫属</span><span lang=EN-US>nginx-rtmp</span><span
style='font-family:宋体'>，以下是</span><span lang=EN-US>nginx-rtmp</span><span
style='font-family:宋体'>几个盛行于世的重要因素：</span></p>

<p class=MsoNormal align=left style='margin-left:24.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US style='font-size:10.0pt;font-family:Symbol;
color:black'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>2012</span><span
style='font-family:"微软雅黑",sans-serif;color:black'>年<span lang=EN-US>CDN</span>业务开始极增长，随之直播需求也多了起来，彼时业界都还没有一套公认的特别满意的流媒体服务器；</span></p>

<p class=MsoNormal align=left style='margin-left:24.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US style='font-size:10.0pt;font-family:Symbol;
color:black'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>Nginx</span><span
style='font-family:"微软雅黑",sans-serif;color:black'>是<span lang=EN-US>HTTP</span>领域绝对的霸主，大家（尤其是<span
lang=EN-US>CDN</span>运维）对<span lang=EN-US>Nginx</span>熟悉程度很高，便于上手维护；</span></p>

<p class=MsoNormal align=left style='margin-left:24.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US style='font-size:10.0pt;font-family:Symbol;
color:black'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span style='font-family:"微软雅黑",sans-serif;color:black'>基于<span
lang=EN-US>Nginx</span>，直播点播使用一套服务器，这也极具诱惑力，一套管理起来总比多套要简单；</span></p>

<p class=MsoNormal align=left style='margin-left:24.0pt;text-align:left;
text-indent:-18.0pt'><span lang=EN-US style='font-size:10.0pt;font-family:Symbol;
color:black'>·<span style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</span></span><span lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>CDN</span><span
style='font-family:"微软雅黑",sans-serif;color:black'>是靠运维的行当，运维的信心都是长年运出来的，<span
lang=EN-US>Nginx</span>在图文上那么优秀，<span lang=EN-US>Nginx RTMP</span>也差不了。</span></p>

<p class=MsoNormal align=left style='margin-top:3.75pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>&nbsp;</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>nginx-rtmp</span><span
style='font-family:宋体'>确实生来就自带光环外，性能也的确是高，比</span><span lang=EN-US>Crtmpd</span><span
style='font-family:宋体'>还要高。然而，时过境迁，随着互动直播、移动直播的强势兴起的大直播时代，选择</span><span
lang=EN-US>nginx-rtmp</span><span style='font-family:宋体'>到底是福还是祸？</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>下面小编将从<b><span
style='color:#FF6827'>协议支持、体系架构、核心功能支持、配置运维、性能、服务器日志、数据</span></b>这七大维度将目前市面主流的流媒体</span><span
lang=EN-US>Server</span><span style='font-family:宋体'>做一个横向对比，供视频从业者根据自身业务场景特性择优选用。</span></p>

<h4><a name="_Toc462219553"><span class=4><span style='font-family:宋体;
font-weight:normal'>网络协议对比</span></span></a></h4>

<p class=MsoNormal align=center style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:center;line-height:15.75pt'><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'><img border=0
width=549 height=349 id="图片 13" src="srs_wiki.files/image009.jpg"
alt="https://h5.weiyun.com/tx_tls_gate=img7.wtoutiao.com/?url=http://mmbiz.qpic.cn/mmbiz/ibqXNcZwc8ZficAW5LaxzmE8WU7RSHXA8z68Zy3Aw6zC7VQKv74JHq2vkGt67XBrXwDSZbUTgEmqUtB5ueoWoqQQ/0?wx_fmt=png"></span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>BMS</span><span
style='font-family:宋体'>支持</span><span lang=EN-US>HDS</span><span
style='font-family:宋体'>、</span><span lang=EN-US>DASH</span><span
style='font-family:宋体'>、</span><span lang=EN-US>RTMPE/S/T</span><span
style='font-family:宋体'>等协议的分发，这将支持更多业务应用场景，</span><span lang=EN-US>FLASH P2P</span><span
style='font-family:宋体'>的支持能够显著降低网络带宽成本。</span></p>

<h4><a name="_Toc462219554"><span style='font-family:宋体'>体系架构对比</span></a></h4>

<p class=MsoNormal align=center style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:center;line-height:15.75pt'><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'><img border=0
width=567 height=325 id="图片 12" src="srs_wiki.files/image010.jpg"
alt="https://h5.weiyun.com/tx_tls_gate=img7.wtoutiao.com/?url=http://mmbiz.qpic.cn/mmbiz/ibqXNcZwc8ZficAW5LaxzmE8WU7RSHXA8zFTLCrZwgEhxUCFSDgXZl4316jZqzNUeq5Sg9iavz270lJZNFmmVXcMQ/0?wx_fmt=png"></span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>架构方面，较之于</span><span
lang=EN-US>nginx-rtmp</span><span style='font-family:宋体'>的</span><span
lang=EN-US>16</span><span style='font-family:宋体'>万行代码，</span><b><span
lang=EN-US style='color:#FF6827'>SRS</span></b><b><span style='font-family:
宋体;color:#FF6827'>仅用了</span><span lang=EN-US style='color:#FF6827'>6.5</span></b><b><span
style='font-family:宋体;color:#FF6827'>万行代码就实现了比</span><span lang=EN-US
style='color:#FF6827'>nginx-rtmp&nbsp;</span></b><b><span style='font-family:
宋体;color:#FF6827'>多了</span><span lang=EN-US style='color:#FF6827'>230%</span></b><b><span
style='font-family:宋体;color:#FF6827'>的功能</span></b><span style='font-family:
宋体;color:#FF6827'>，</span><span lang=EN-US>nginx-rtmp</span><span
style='font-family:宋体'>注释率为</span><span lang=EN-US>3%</span><span
style='font-family:宋体'>，而</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>是</span><span lang=EN-US>23.7%</span><span
style='font-family:宋体'>。由此可见</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>在体系架构上的轻，</span><span lang=EN-US>Simple</span><span
style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span lang=EN-US>BMS</span><span
style='font-family:宋体'>在</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>的基础上新增了<b><span style='color:#FF6827'>多进程支持、源站集群、动态配置、可追溯日志</span></b>等方面能力。源站集群子系统打通了跨网跨地区的源站分布式部署难题；动态配置子系统从业务系统读取配置，依据更新机制动态更新配置，保证直播业务配置变化时依然不中断；端到端的可追溯日志及监控排错子系统将直播故障定位时间缩短到了分钟级别。</span></p>

<h4><a name="_Toc462219555"><span style='font-family:宋体'>核心功能对比</span></a></h4>

<p class=MsoNormal align=center style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:center;line-height:15.75pt'><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'><img border=0
width=563 height=441 id="图片 11" src="srs_wiki.files/image011.jpg"
alt="https://h5.weiyun.com/tx_tls_gate=img7.wtoutiao.com/?url=http://mmbiz.qpic.cn/mmbiz/ibqXNcZwc8ZficAW5LaxzmE8WU7RSHXA8zVhL4zicvUfzS1RicNYk7iccVVAyfiaDK6WqcBRXiciasokULxG77HDO3j6Ug/0?wx_fmt=png"></span></p>

<p class=MsoNoSpacing style='text-indent:21.0pt'><span style='font-family:宋体'>核心功能方面，</span><span
lang=EN-US>BMS</span><span style='font-family:宋体'>支持了<b><span style='color:
#FF6827'>当期互动直播、移动直播急需的大规模直播流实时转码、大规模录制、秒级低延迟、</span></b></span><b><span
lang=EN-US style='color:#FF6827'>HLS+</span></b><b><span style='font-family:
宋体;color:#FF6827'>、并发回源</span></b><span style='font-family:宋体'>等其它所有流媒体系统不具备的功能。</span><span
lang=EN-US>HLS+</span><span style='font-family:宋体'>基于每个播放请求实现了流媒体的“虚拟连接</span><span
lang=EN-US>&nbsp;</span><span style='font-family:宋体'>”（</span><span lang=EN-US>UUID</span><span
style='font-family:宋体'>标识），在减小回源量、排错、防盗链、移动</span><span lang=EN-US>Web</span><span
style='font-family:宋体'>端低延迟等方面具有诸多优势。并发回源能够解决回源网络状况差、跨国传输丢包严重等方面能够显著提升回源质量。</span></p>

<h4><a name="_Toc462219556"><span style='font-family:宋体'>配置运维对比</span></a></h4>

<p class=MsoNormal style='margin-top:12.0pt;margin-right:0cm;margin-bottom:
12.0pt;margin-left:0cm;line-height:15.75pt'><span style='font-family:"微软雅黑",sans-serif;
color:black'>以下仅是流媒体众多配置之中几个常用例子，运维日常工作中，需要操作的配置数量更多。</span></p>

<h5><span style='font-family:宋体'>（</span><span lang=EN-US>1</span><span
style='font-family:宋体'>）</span><span lang=EN-US>vhost</span><span
style='font-family:宋体'>配置</span></h5>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>FMS</span></b></p>

<p class=MsoNormal align=left style='text-align:left;line-height:15.75pt;
background:#EEEEEE;vertical-align:baseline'><span style='font-size:9.0pt;
font-family:"微软雅黑",sans-serif;color:#3E3E3E'>拷贝默认<span lang=EN-US>vhost</span>目录：<span
lang=EN-US>sudo cp -r conf/_defaultRoot_/_defaultVHost_ conf/_defaultRoot_/bravo.sina.com</span></span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>nginx-rtmp</span></b></p>

<p class=MsoNormal align=left style='text-align:left;line-height:15.75pt;
background:#EEEEEE;vertical-align:baseline'><span style='font-size:9.0pt;
font-family:"微软雅黑",sans-serif;color:#3E3E3E'>不支持</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>SRS/BMS</span></b></p>

<p class=MsoNormal align=left style='text-align:left;line-height:15.75pt;
background:#EEEEEE;vertical-align:baseline'><span style='font-size:9.0pt;
font-family:"微软雅黑",sans-serif;color:black'>动态获取配置文件：<span lang=EN-US>vhost&nbsp;bravo.sina.com&nbsp;{&nbsp;}</span></span></p>

<p class=MsoNormal align=left style='margin-top:11.25pt;margin-right:0cm;
margin-bottom:3.75pt;margin-left:0cm;text-align:left;line-height:15.75pt'><span
style='font-family:"微软雅黑",sans-serif;color:#FF6827'>结论：<span lang=EN-US>BMS</span>动态获取配置最简单</span></p>

<h5><span style='font-family:宋体'>（</span><span lang=EN-US>2</span><span
style='font-family:宋体'>）</span><span lang=EN-US>app</span><span
style='font-family:宋体'>配置</span></h5>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>&nbsp;FMS</span></b></p>

<p class=MsoNormal align=left style='text-align:left;line-height:15.75pt;
background:#EEEEEE;vertical-align:baseline'><span style='font-size:9.0pt;
font-family:"微软雅黑",sans-serif;color:black'>拷贝默认<span lang=EN-US>app</span>目录：<span
lang=EN-US>cp&nbsp;applications/live&nbsp;applications/mylive&nbsp;-r</span></span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>nginx-rtmp</span></b></p>

<p class=MsoNormal align=left style='text-align:left;line-height:15.75pt;
background:#EEEEEE;vertical-align:baseline'><span style='font-size:9.0pt;
font-family:"微软雅黑",sans-serif;color:black'>修改配置文件，增加如下内容：<span lang=EN-US>application&nbsp;live&nbsp;{&nbsp;&nbsp;live&nbsp;on;&nbsp;}</span></span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>SRS/BMS</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>无需配置</span></p>

<p class=MsoNormal align=left style='margin-top:7.5pt;margin-right:0cm;
margin-bottom:3.75pt;margin-left:0cm;text-align:left;line-height:15.75pt'><span
style='font-family:"微软雅黑",sans-serif;color:#FF6827'>结论：<span lang=EN-US>BMS</span>无需配置，最简单</span><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:#3E3E3E'>&nbsp;</span></p>

<h5><span style='font-family:宋体'>（</span><span lang=EN-US>3</span><span
style='font-family:宋体'>）</span><span lang=EN-US>http</span><span
style='font-family:宋体'>配置</span></h5>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><span
style='font-family:"微软雅黑",sans-serif;color:black'>在输出为<span lang=EN-US>hls</span>、<span
lang=EN-US>http-flv</span>等基于<span lang=EN-US>http</span>协议的直播流时，需要配置<span
lang=EN-US>http</span>服务</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>FMS</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>配置<span lang=EN-US>FMS</span>内置的<span lang=EN-US>Apache</span>服务器文件：<span
lang=EN-US>Apache2.2/conf/httpd.conf</span></span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>再修改如下字段：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&lt;Location&nbsp;/hds-live&gt;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;HttpStreamingEnabled&nbsp;true</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;HttpStreamingLiveEventPath&nbsp;&quot;../applications&quot;&nbsp;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;HttpStreamingContentPath&nbsp;&quot;../applications&quot;&nbsp;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;HttpStreamingF4MMaxAge&nbsp;2</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;HttpStreamingBootstrapMaxAge&nbsp;2</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;HttpStreamingFragMaxAge&nbsp;-1</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;Options&nbsp;-Indexes&nbsp;FollowSymLinks</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&lt;/Location</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>nginx-rtmp</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"微软雅黑",sans-serif;color:black'>nginx</span><span style='font-size:9.0pt;
font-family:"微软雅黑",sans-serif;color:black'>本身就是一个<span lang=EN-US>http</span>服务器，</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>修改其配置文件：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>conf/nginx.conf</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>设置端口和根目录：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>http&nbsp;{</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;include&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;mime.types;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;default_type&nbsp;&nbsp;application/octet-stream;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;sendfile&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;on;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;keepalive_timeout&nbsp;&nbsp;65;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;server&nbsp;{</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;80;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;server_name&nbsp;&nbsp;localhost;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;location&nbsp;/dash&nbsp;{</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;root&nbsp;/tmp;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;add_header&nbsp;Cache-Control&nbsp;no-cache;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;}</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>}</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>SRS/BMS</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>修改其配置文件：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>conf/http.hls.conf</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>设置端口和根目录：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>http_stream&nbsp;{</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;enabled&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;on;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;listen&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;8080;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>&nbsp;&nbsp;&nbsp;&nbsp;dir&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;./objs/nginx/html;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>}</span></p>

<p class=MsoNormal align=left style='margin-top:7.5pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
style='font-family:"微软雅黑",sans-serif;color:#FF6827'>结论：<span lang=EN-US>nginx-rtmp</span>需指定与<span
lang=EN-US>app</span>对应的<span lang=EN-US>ts</span>文件存放目录，<span lang=EN-US>SRS/BMS</span>会自动生成，更简单。</span></b></p>

<h5><span style='font-family:宋体'>（</span><span lang=EN-US>4</span><span
style='font-family:宋体'>）推流、播放</span><span lang=EN-US>URL</span><span
style='font-family:宋体'>配置</span></h5>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>RTMP</span><span
style='font-family:"微软雅黑",sans-serif;color:black'>直播时，各大服务器推流、播流<span
lang=EN-US>URL</span>均为：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;text-indent:24.0pt;
line-height:15.75pt'><span lang=EN-US style='font-family:"微软雅黑",sans-serif;
color:black'>rtmp://server_ip_or_dns/app/stream</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><span
style='font-family:"微软雅黑",sans-serif;color:black'>用作<span lang=EN-US>HLS</span>直播时，</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>FMS&nbsp;</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>推流域名：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>rtmp://fms-ip-or-dns/app/stream?adbe-live-event=liveevent</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>播流域名：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>http://fms-ip-or-dns/hds-live/app/_definst_/liveevent/stream.f4m</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>nginx-rtmp</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>推流域名：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>rtmp://server_ip_or_dns/app/stream</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>播流域名：</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"Simsun",serif;color:black'>http://server_ip_or_dns/app/stream.m3u8</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>SRS/BMS</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span style='font-size:9.0pt;font-family:"微软雅黑",sans-serif;
color:black'>同</span><span lang=EN-US style='font-size:9.0pt;font-family:"Simsun",serif;
color:black'>nginx-rtmp</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:3.75pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
style='font-family:"微软雅黑",sans-serif;color:#FF6827'>结论：<span lang=EN-US>nginx-rtmp</span>、<span
lang=EN-US>SRS/BMS</span>均简单，<span lang=EN-US>FMS</span>较复杂。</span></b></p>

<h4><a name="_Toc462219557"><span style='font-family:宋体'>性能</span></a></h4>

<p class=MsoNormal align=left style='margin-top:3.75pt;margin-right:0cm;
margin-bottom:3.75pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
style='font-family:"微软雅黑",sans-serif;color:black'>先说结论：</span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><b><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:#FF6827'>SRS</span></b><b><span
style='font-family:"微软雅黑",sans-serif;color:#FF6827'>单进程能支持<span lang=EN-US>9000</span>并发，<span
lang=EN-US>nginx-rtmp</span>单进程最多支持<span lang=EN-US>3000</span>个，单进程的性能<span
lang=EN-US>SRS</span>是<span lang=EN-US>nginx-rtmp</span>的三倍。单进程性能<span
lang=EN-US>SRS&nbsp;&gt;&nbsp;nginx-rtmp&nbsp;&gt;&nbsp;crtmpd&nbsp;&gt;&nbsp;wowza&nbsp;&gt;&nbsp;fms&nbsp;&gt;&nbsp;RED5</span></span></b></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;line-height:15.75pt'><span
lang=EN-US style='font-family:"微软雅黑",sans-serif;color:black'>&nbsp;</span><span
style='font-family:"微软雅黑",sans-serif;color:black'>再例举<span lang=EN-US>SRS</span>性能如此高的几个原因：</span></p>

<p class=MsoNoSpacing><span lang=EN-US>1.&nbsp;st-load</span><span
style='font-family:宋体'>，这个是</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>能做到高性能的最重要的原因，一个</span><span lang=EN-US>st-load</span><span
style='font-family:宋体'>可以模拟</span><span lang=EN-US>2000+</span><span
style='font-family:宋体'>的客户端，如果没有</span><span lang=EN-US>st-load</span><span
style='font-family:宋体'>，如何知道系统的性能瓶颈在哪里？总不能打开</span><span lang=EN-US>3000</span><span
style='font-family:宋体'>个</span><span lang=EN-US>flash</span><span
style='font-family:宋体'>页面播放</span><span lang=EN-US>rtmp</span><span
style='font-family:宋体'>流吧？开启</span><span lang=EN-US>3000</span><span
style='font-family:宋体'>个</span><span lang=EN-US>ffmpeg</span><span
style='font-family:宋体'>来抓流？高性能不是想象和猜测出来的，而是反复测试、调试和改进出来的。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>2.&nbsp;gperf/gprof</span><span
style='font-family:宋体'>性能，编译</span><span lang=EN-US>SRS</span><span
style='font-family:宋体'>时，就可以打开</span><span lang=EN-US>gcp</span><span
style='font-family:宋体'>或者</span><span lang=EN-US>gprof</span><span
style='font-family:宋体'>的性能分析选项，非常方便的拿到数据。缩短了改进和优化开发周期。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>3.&nbsp;</span><span style='font-family:
宋体'>引用计数的</span><span lang=EN-US>msgs</span><span style='font-family:宋体'>避免内存拷贝。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>4.&nbsp;</span><span style='font-family:
宋体'>使用</span><span lang=EN-US>writev</span><span style='font-family:宋体'>发送</span><span
lang=EN-US>chunked</span><span style='font-family:宋体'>包，避免消息到</span><span
lang=EN-US>chunked</span><span style='font-family:宋体'>包的内存拷贝。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>5.&nbsp;mw(merged-write)</span><span
style='font-family:宋体'>技术，即一次发送多个消息。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>6.&nbsp;</span><span style='font-family:
宋体'>减少</span><span lang=EN-US>timeout&nbsp;recv</span><span style='font-family:
宋体'>，每个连接都是一个</span><span lang=EN-US>st-thread</span><span style='font-family:
宋体'>在服务。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>7.&nbsp;fast&nbsp;buffer</span><span
style='font-family:宋体'>和</span><span lang=EN-US>cache</span><span
style='font-family:宋体'>。</span></p>

<p class=MsoNoSpacing><span lang=EN-US>8.&nbsp;vector</span><span
style='font-family:宋体'>还是</span><span lang=EN-US>list</span><span
style='font-family:宋体'>？</span><span lang=EN-US>vector</span><span
style='font-family:宋体'>！</span><span lang=EN-US>vector</span><span
style='font-family:宋体'>比</span><span lang=EN-US>list</span><span
style='font-family:宋体'>高</span><span lang=EN-US>10%</span><span
style='font-family:宋体'>性能。</span></p>

<h4><a name="_Toc462219558"><span style='font-family:宋体'>服务器日志</span></a></h4>

<p class=MsoNoSpacing><span style='font-family:宋体'>日志是定位故障的唯一途径，定位故障才能快速排错。可以这么说，对于直播，</span><span
lang=EN-US>10</span><span style='font-family:宋体'>分钟的排错，谁都会觉得长。然而，当前的视频云或</span><span
lang=EN-US>CDN</span><span style='font-family:宋体'>，谁又能做到</span><span
lang=EN-US>10</span><span style='font-family:宋体'>分钟呢？</span></p>

<p class=MsoNoSpacing><span style='font-family:宋体'>来看看日志吧。</span></p>

<p class=MsoNormal style='margin-top:12.0pt;margin-right:0cm;margin-bottom:
3.75pt;margin-left:0cm;line-height:15.75pt'><span lang=EN-US style='font-family:
"微软雅黑",sans-serif;color:black'>FMS</span><span style='font-family:"微软雅黑",sans-serif;
color:black'>的日志是这样的，恕我愚钝，你能看得出什么信息么？</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"微软雅黑",sans-serif;color:black'>2015-03-24 12:23:58
3409&nbsp;(s)2641173&nbsp;Accepted&nbsp;a&nbsp;connection&nbsp;from&nbsp;IP:192.168.1.141,&nbsp;referrer:http://www.ossrs.net/players/srs_player/release/srs_player.swf?_versi&gt;</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"微软雅黑",sans-serif;color:black'>702111234525315439&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3130&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3448&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;normal&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;livestream&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;rtmp://192.168.1.185:1935/live/livestream&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;rtmp://192.168.1.185:1935/live/livestream&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;flv&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;0&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;http://www.ossrs.net/players/srs_player.html?vhost=dev&amp;stream=livestream&amp;server=dev&amp;port=1935&nbsp;&nbsp;&nbsp;&nbsp;-1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-1.000000
&nbsp; &nbsp;</span><span lang=EN-US style='font-family:"微软雅黑",sans-serif;
color:black'>&nbsp; &nbsp; &nbsp;</span></p>

<p class=MsoNormal style='margin-top:3.75pt;margin-right:0cm;margin-bottom:
3.75pt;margin-left:0cm;line-height:15.75pt'><span lang=EN-US style='font-family:
"微软雅黑",sans-serif;color:black'>crtmpd</span><span style='font-family:"微软雅黑",sans-serif;
color:black'>的日志详细，但我又愚钝，若是上千人在线，你又能看出什么有用的东西么？</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"微软雅黑",sans-serif;color:black'>/home/winlin/tools/crtmpserver.20130514.794/sources/thelib/src/netio/epoll/iohandlermanager.cpp:120Handlers&nbsp;count&nbsp;changed:&nbsp;15-&gt;16&nbsp;IOHT_TCP_CARRIER</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"微软雅黑",sans-serif;color:black'>/home/winlin/tools/crtmpserver.20130514.794/sources/thelib/src/netio/epoll/tcpacceptor.cpp:185Client&nbsp;connected:&nbsp;192.168.1.141:54823&nbsp;-&gt;&nbsp;192.168.1.173:1935</span></p>

<p class=MsoNormal align=left style='margin-top:12.0pt;margin-right:0cm;
margin-bottom:12.0pt;margin-left:0cm;text-align:left;background:#EEEEEE;
vertical-align:baseline'><span lang=EN-US style='font-size:9.0pt;font-family:
"微软雅黑",sans-serif;color:black'>/home/winlin/tools/crtmpserver.20130514.794/sources/applications/appselector/src/rtmpap</span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

<h1><a name="_Toc26097995"></a><a name="_Toc462219560">常用的直播平台网站</a></h1>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="https://github.com/ossrs/srs"><span style='font-family:"Segoe UI",sans-serif;
color:#095EAB;background:white'>https://github.com/ossrs/srs</span></a></span><span
lang=EN>&nbsp;&nbsp;&nbsp; SRS</span><span style='font-family:宋体'>官网</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="https://github.com/arut/nginx-rtmp-module"><span lang=EN>https://github.com/arut/nginx-rtmp-module</span></a></span><span
lang=EN>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; nginx rtmp</span><span
style='font-family:宋体'>官网</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="https://www.qcloud.com/product/LVB.html"><span lang=EN>https://www.qcloud.com/product/LVB.html</span></a></span><span
lang=EN>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span
style='font-family:宋体'>腾讯云直播</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="https://www.aliyun.com/product/live?spm=5176.7960203.237031.164.Ve6N2d"><span
lang=EN>https://www.aliyun.com/product/live?spm=5176.7960203.237031.164.Ve6N2d</span></a></span><span
lang=EN> </span><span style='font-family:宋体'>阿里云直播</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="https://bce.baidu.com/product/lss.html"><span lang=EN>https://bce.baidu.com/product/lss.html</span></a></span><span
lang=EN>&nbsp;&nbsp; </span><span style='font-family:宋体'>百度云直播</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="http://www.lecloud.com/zh-cn/product/live.html"><span lang=EN>http://www.lecloud.com/zh-cn/product/live.html</span></a></span><span
lang=EN>&nbsp;&nbsp; </span><span style='font-family:宋体'>乐视云直播</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="https://www.upyun.com/products/video.html"><span lang=EN>https://www.upyun.com/products/video.html</span></a></span><span
lang=EN>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span style='font-family:宋体'>又拍云直播</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="http://www.qiniu.com/products/live"><span lang=EN>http://www.qiniu.com/products/live</span></a></span><span
lang=EN>&nbsp;&nbsp;&nbsp;&nbsp; </span><span style='font-family:宋体'>七牛云直播</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="http://xycdn.com/site/solution"><span lang=EN>http://xycdn.com/site/solution</span></a></span><span
lang=EN>&nbsp;&nbsp; </span><span style='font-family:宋体'>星域云</span><span
lang=EN>(</span><span style='font-family:宋体'>讯雷旗下的公司</span><span lang=EN>)</span></p>

<p class=MsoNormal><span lang=EN>&nbsp;&nbsp; </span><span lang=EN-US><a
href="http://www.easydarwin.org"><span lang=EN>http://www.easydarwin.org</span></a></span><span
lang=EN>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; RTSP</span><span style='font-family:
宋体'>开源平台</span></p>

<p class=MsoNormal><span lang=EN-US>&nbsp;</span></p>

</div>

</body>

</html>
