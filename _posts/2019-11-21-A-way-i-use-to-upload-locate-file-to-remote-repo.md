---
header:
  image: /assets/images/myblog.jpg
  teaser: /assets/images/myblog.jpg
title: A way i use to uplode locate file to remote repo
tags:
  - website
---

#### Overview

&nbsp;&nbsp;you can write a article directly in github,but waht if there are many picture you need in your artical,it is fussy to add image into your artical,you have to uplode a picture to a folder,then use its refrence.you have to commit it again and again.there a method i use which make you get a screenshot picture,Let us jump in....

#### Tool 

<li> VS code+Markdown</li>
<li>Vmwarware workstation,Ubuntu</li>
<li>GIt</li>


#### STEP 1
use `git --versin` see if you have install the git
use `git clone **your own reposority URL**`
jump into your clone folder in local
use `git init`
use `git remote add origin "your repository URL"`


open the vamvare -> `option`->`share folder` like following:
![vm](/assets/images/vm.jpg)

#### STEP 2
creat a article `yourposrt.md` in the shared folder

#### STEP 3

move the shared folder to your reposority derectory 

#### SETP 4

use 

`git add "your post"`

`git commit -m "something"`

`git push origin master`

then put your username and user password
