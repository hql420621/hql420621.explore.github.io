---
header:
  image: /assets/images/dll.jpg
  teaser: /assets/images/dll.jpg
title: could not Load the dll 
tags:
  - DLL
  - C/C++
---
recently,i run into a very annoy bug when i run code below

`hdl=loadlibrary("dirlog-c.dll")`,the fllowing function `getlasterror()` return `126`,that is explained in msdn

```c++
ERROR_MOD_NOT_FOUND
　　126 (0x7E)
　　The specified module could not be found.
```
`the specified moudle could not be found`,but,i surly confirm that i have set the correct path.i found a tool named `depend.exe` on website,which include in VS by default,you can just <a href=https://www.dependencywalker.com>download</a> if you can not find it,it is very simpy and tiny tool.

click the `depend.exe` and run it.

open the `dirlog-cl.dll`.or you can just drag it into the `depend.exe ` ,it will be take a few time that the software to analyse the dll

we can see there is somthing wrong with the `pcre.dll` on which my `dirlog-cl.dll` depends. i miss it ,the `pcre.dll`can not found 
![dependn](/assets/images/dependn.jpg)

 so, i download the `pcre.dll` and put it under the debug folder. and use the `depend.exe` to check the `dirlog-cl.dll` again,it shows as below
 
 ![dependy](/assets/images/dependy.png)

it make sense!! i load the `dirlog-cl.dll`,but it miss the `pcre.dll`,that is why the specified module could not be found.


**<span style="color:red">NOTE</span>**:there are many reason when you get the `126`code return,like the wrong path,or you actually use the `loadlibrayW()` not `loadlibrayA()`,they are difference when you pass the parameter,and so on
