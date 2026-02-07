The File Hierarchy Structure (FHS) defines the directory structure and directory contents in Unix-like OS. 

All files and directories appear under the root directory /, even if they are stored on different physical or virtual devices. Some of these only exist on a particular system if certain subsystems, such as the X Window System, are installed.

Here is a general layout of core files:

![[root-files-example.png]]

<div style="position: relative; width: 720px;">
<img src="images/root-files-example.png" usemap="#linuxmap" style="width:100%;">

<map name="linuxmap">

  <area shape="rect" coords="205,35,350,80" href="bin" alt="/bin">
  <area shape="rect" coords="205,90,350,135" href="boot" alt="/boot">
  <area shape="rect" coords="205,145,350,190" href="dev" alt="/dev">
  <area shape="rect" coords="205,200,350,245" href="etc" alt="/etc">
  <area shape="rect" coords="205,255,350,300" href="home" alt="/home">
  <area shape="rect" coords="205,310,350,355" href="lib" alt="/lib">
  <area shape="rect" coords="205,365,350,410" href="media" alt="/media">
  <area shape="rect" coords="205,420,350,465" href="mnt" alt="/mnt">
  <area shape="rect" coords="205,475,350,520" href="opt" alt="/opt">
  <area shape="rect" coords="205,530,350,575" href="sbin" alt="/sbin">
  <area shape="rect" coords="205,585,350,630" href="srv" alt="/srv">
  <area shape="rect" coords="205,640,350,685" href="tmp" alt="/tmp">
  <area shape="rect" coords="205,695,350,740" href="usr" alt="/usr">
  <area shape="rect" coords="205,750,350,795" href="proc" alt="/proc">

</map>
</div>


#FHS
