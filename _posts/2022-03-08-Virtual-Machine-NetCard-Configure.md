---
header:
  image: /assets/images/image-20220308180127225.png
  teaser: /assets/images/image-20220308180127225.png
title: VMware Network configure
tags:
  - Tool
---

#### overview

when we build a virtual machine with vmware in local host,i wanna do two thing firstly ,the one thing is that i can connect it with ssh tool ,such as  MobaXtem ,another thing is that i can connect to outside network.without futher ado,let's break it down.

+ Connect with ssh tool 

  if we want connet the local host with ssh tool ,we simply configure the netcard into **HOST ONLY MOdE**

  + step 1

    right click the icon in the picture below

  ![image-20220308180127225](images/image-20220308180127225.png)

  + step 2

      select the network adpter and choose host only mode

  ![image-20220308180446977](images/image-20220308180446977.png)
      

  + step 3

    configure the network file in `/etc/sysconfig/network-scripts/`,and set static ip

+ connet outside network

  if we want our local host connect network ,like ping baidu.com ,we can configure the network into **bridge pattern**
    + step 1
  
  right click the icon in the picture below
    ![image-20220308180127225](images/image-20220308180127225.png)
  
    + step 2
  
  add another network adpter![image-20220308182810687](images/image-20220308182810687.png)

  ![image-20220308183946519](images/image-20220308183946519.png)

+ step 3

  ![image-20220308184420276](images/image-20220308184420276.png)
  + step 4

configure the network file in `/etc/sysconfig/network-scripts/`,and set dynamic ip


