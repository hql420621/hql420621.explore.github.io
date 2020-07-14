---
header:
  image: /assets/images/usedllinmfc.png
  teaser: /assets/images/usedllinmfc.png
title: Select static DLL in MFC  Configration in Properties
tags:
  - C/C++
  - DLL
---

#### overview

recently,i creat a dll in my project ,then i use it in my project,and in packed it finally,i run the project normally,but it doest work when i tranfer the project to another computer ,it bother me a lot ,fistly i sue the Depency tool to synasies it so that i can check out whether it miss some mandetory dll dependcy,but it doest miss anything.


#### The size of dll is wired

then i campare the last one dll i create to the before i found ,my dll size is so small,how could it be ? 
![dllmfc](/assets/images/dllmfc1.png)

#### locate the problem

i check out the project `propersit setting --->configration properity-->general-->use dll in MFC` i found i select ` use the share dll in mfc`,that is the problem it is ,when you select `use the share dll in mfc `,the excutable file doest contain the dll dependency,so it is small
![mfcdll2](/assets/images/mfcdll2.png)

### solution
right click the project -propersit setting --->configration properity-->general-->use dll in MFC,select `use mfc as static dll`
![dllmfc3](/assets/images/usedllinmfc.png)

problem solved!!!