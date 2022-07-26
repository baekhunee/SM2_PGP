# 实验名称
SM2_PGP

# 实验简介
基于对称加密算法SM4与非对称加密算法SM2实现简易PGP

# 实验完成人
权周雨 

学号：202000460021 

git账户名称：baekhunee

# PGP简介
PGP（Pretty Good Privacy），是一个基于RSA公钥和对称加密相结合的邮件加密软件。该系统能为电子邮件和文件存储应用过程提供认证业务和保密业务。

PGP是个混合加密算法，它由一个对称加密算法（IDEA）、一个非对称加密算法（RSA）、与单向散列算法（MD5）以及一个随机数产生器（从用户击键频率产生伪随机数序列的种子）组成的。

# 实验过程
本次实验旨在实现一个简易PGP，调用gmssl库中封装好的SM2/SM4加解密函数。

加密时使用对称加密算法SM4加密消息，非对称加密算法SM2加密会话密钥；

解密时先使用SM2解密求得会话密钥，再通过SM4和会话密钥求解原消息。

## 加密过程
![image](https://user-images.githubusercontent.com/105578152/180976048-bc82649d-e801-4a28-a5c2-3a340b11e63f.png)

## 解密过程
![image](https://user-images.githubusercontent.com/105578152/180976114-0d3a1d28-5c1b-4034-ad68-6da4d6779308.png)

# 部分代码说明
