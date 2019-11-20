---
title: recover backup from banwagong
image："/assets/images/banwagong.png"
tags:
  - website
  - vps
---
<p>
<h2> overview</h2>
i've ever built my own blog by Wordpress and VPS folowing the the tutorial <a href="https://www.seoimo.com/wordpress-vps/">how to build a website with wordpress and vps</a>.but it was easilly to being attacked by hacker.enventually my host suspended,it only recover until next year. the situation like following: </p>

![vps erro](/assets/images/vps.jpg)

lucky,the biggest strenth of the bangwagong is that it has the snapshot,it can help you to recover it when it is necessary,so i am gonna to restore it ,but i was forbbien to that,and gimme the hint:the host has been suspended. i cant wait to repair my blog ,so i just abandon the preview blog built by worldpress and VPS and turn my head  to the Jekyll and github-page method. but how about i want use the picture,the post i written before,i've ever try to download the backup and unzip it ,and it turns out 
the file with the suffix of .disk.like the folowing:
![vps_disk](/assets/images/vps_disk.jpg)

the above file with the suffix of .dsk can not be opened in windows,it really bother me ,finnlly ,i find the tutorial: <a href="https://www.hostloc.com/thread-392553-1-1.html">get reletive file from banwagong</a>.let us kick off.
***NOTE: the .disk file can only  be opened in linux system***

<li>STEP 1:</li>

download the .tar.gz snapshot file from vps. and use the `scp` command to copy the .tar.gz  from the pc to linux[it depends what OS you use,u can ignore this process if you download derectly in linux].and use `tar` command to uncompress the file,and get the `vm-1234xxx.disk` file

<li>STEP2</li>

check out which dev is free by the `losetup -f`
