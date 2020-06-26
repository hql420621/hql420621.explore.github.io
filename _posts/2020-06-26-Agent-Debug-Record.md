---
header:
  image: /assets/images/perl.png
  teaser: /assets/images/perl.png
title: how to solve Can't locate Sys/Syslog.pm in @INC
tags:
  - Perl
  - linux
---

#### how to solve Can't locate Sys/Syslog.pm in @INC
when i write the code `use Sys::syslog` in perl script,and excute the `my.pl` command in linux ,i run into `can't locate Sys/syslog.pm in @INC` i think i just miss this file ,so i put the `syslog.pm` in `/usr/lib64/perl5/Sys/`path,but it still doesnt work and give me another error `Can't locate loadable object for module Sys::Syslog in @INC`,than i search it in google,and find this reason
![perl_locate_object](/assets/images/perl_locate_object.jpg)
i guss this is the reason that i cant be secuss,so i just delect the syslog.pm an type this command below
`yum install -y perl-Sys-Syslog`,it works !
