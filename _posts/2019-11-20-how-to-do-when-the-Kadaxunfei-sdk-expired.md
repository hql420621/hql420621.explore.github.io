---
title: how to do when the Kadaxunfei SDK expired
header:
  image: /assets/images/speach_recognize.jpg
  teaser: /assets/images/speach_recognize.jpg
tags:
  - SDK
---
### Overview

so far, you can only use the Kadaxunfei SDK only for one month. so what if the SDK expired after on  month, you have to download it again,and build your project form the scrath,it is ok if the project is small,but it will annoy you a lot and take your more time to rebuild it when the project is big.Finally,i find the solution that can make you quickly to rebuild it rather than from the biginning.Let us jump in..

`take my project for example`

***SETP 1***

reapply the application in <a href="https://www.xfyun.cn/">offical site</a>.

![application](/assets/images/application.jpg)

and download the <a href="https://www.xfyun.cn/sdk/dispatcher">offine-command-SDK</a>.

![offline_sdk](/assets/images/offine_sdk.jpg)

***STEP 2***

open the SDK and unzip it. replace the old `msc` folder in `bin` by the new `msc` folder in new SDK.(keep the different file and replace the common file)
![msc](/assets/images/msc.jpg)

***STEP 3***

modify the path `ASR_RES_PATH=" the new msc path"`

***STEP 4***

modify the `APPID` to new.

ALL SET!

***FYI:*** i am use the SDK in unity project ,so i just creat the dll and call it in unity(C#).during  the period of creting  DLL. keep in mind add `DLLDIR_EX` in  `item property sheet -->C/C++`




