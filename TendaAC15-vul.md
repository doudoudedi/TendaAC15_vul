---
title: TendaAC15_vul
date: 2022-03-31 17:31:30
tags:CVE
---

# TendaAC15_Vul

#### Vender

Tenda

Official website ：https://www.tendacn.com/

link:：https://www.tendacn.com/download/detail-3851.html

#### Vulnerability1

##### Detail

​	The stack overflow vulnerability lies in the /goform/setpptpservercfg interface of the web. The sent post data startip and endip are copied to the stack using the sanf function, resulting in stack overflow. Similarly, this vulnerability can be used together with CVE-2021-44971

​	![image-20220331155216047](/Users/doudou/Library/Application Support/typora-user-images/image-20220331155216047.png)

​	Therefore, adding a string of useless characters after straip and endip in the sent postData can cause the web end to crash

![image-20220331160446799](/Users/doudou/Library/Application Support/typora-user-images/image-20220331160446799.png)

#### Vulnerability2

##### Detail

​	There is command injection at the /goform/setsambacfg interface of Tenda ac15 device web, which can also cooperate with CVE-2021-44971 to cause unconditional arbitrary command execution

![image-20220331160952663](/Users/doudou/Library/Application Support/typora-user-images/image-20220331160952663.png)

​	Similarly, the packet that triggers this vulnerability is very simple

![image-20220331161115944](/Users/doudou/Library/Application Support/typora-user-images/image-20220331161115944.png)
