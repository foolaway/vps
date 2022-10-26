



#### 购买的vps

[Shopping Cart - Virtual Machine Solutions LLC (virmach.com)](https://billing.virmach.com/cart.php?a=confproduct&i=0)



![image-20221026185550172](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026185550172.png)



![image-20221026185559607](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026185559607.png)



!(C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026185606506.png)



#### 测试网速、选择一个网上最块的、适合自己节点（我的是芝加哥）

![image-20221026185633578](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026185633578.png)

![image-20221026190129995](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190129995.png)

![image-20221026190050624](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190050624.png)











#### 选择系统

![image-20221026190022525](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190022525.png)



![](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190102050.png





#### 购买

![image-20221026190314631](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190314631.png)



![image-20221026190307761](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190307761.png)



### ！！！！！！使用支付宝支付

#### 没注册的按步骤注册、信息可以乱写、但邮箱必须正确

购买成功后，邮件会收到



![image-20221026190630294](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190630294.png)



##### 使用远程连接工具进行连接vps。例如xshell











连接上后，上传压缩包里的脚本

```

#rz    shadowsocks-all.sh
#sh shadowsocks-all.sh


1.出现 SSR 安装的引导界面，输入数字2，按回车键进行 SSR 安装，如下图所示：
2.然后会提示设置SSR密码，输入自定义密码后按回车，建议不要使用默认密码。
3.接下来选择SSR要使用的服务器端口，尽量选择一个比较大的数字，避免端口冲突，建议选择 8099，经验证 8080、8090 端口是被封了的，千万不要用这个（如果后面遇到可以登录 VPS，但是 ssr 上不了网，可能就是端口封了，修改一下 ssr 端口就可以了）， 然后回车，如下图所示
4.然后选择加密方式，如果选择chacha20的话，就输入对应序号12，按回车继续。 
5.接下来选择协议，建议选择自auth_aes128_md5开始以下的几种，输入对应序号按回车。
6.然后选择混淆方式，如下图所示，选择好后按回车。
7.以上参数选择完成后，按任意键开始安装。  

```

![image-20221025213312453](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025213312453.png)

![image-20221025213454743](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025213454743.png ![image-20221026190821354](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026190821354.png)



```
安装完成后，会有如下图安装成功的提示。
```

![](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025213648232.png



![image-20221025213916125](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025213916125.png)









#### windows客户端解压ShadowsocksR-win-4.9.2.zip文件（防火墙啥的自己看着办）

![

](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025213742405.png)

启动任意一个，电脑右下角出现，右键点击

![image-20221025213819651](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025213819651.png)



![image-20221025214310881](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025214310881.png

!(C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025214336020.png)



![image-20221025214422939](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221025214422939.png)





#### 去谷歌尝试科学上网















虽然 SSR 搭建好了，但是速度还不是很快，要搭建 BBR 才快，下面我们就说说怎么搭建 BBR。

BBR 是 Google 的一款 SSR 加速产品，使用下面的命令就可以实现 BBR 加速，只有 Hostwinds 等少数 KVM VPS 才支持 BBR 加速，这也是我们推荐选择 Hostwinds 的原因。

在 xShell 连接端输入，如下命令，然后回车：

> yum -y install wget wget –no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh chmod +x bbr.sh ./bbr.sh

![img](https://user-images.githubusercontent.com/52620310/62406006-18317000-b5d7-11e9-8146-b9b05d4240d7.jpg)

然后按任意键进行部署

![img](https://user-images.githubusercontent.com/52620310/62406007-1c5d8d80-b5d7-11e9-822f-fd9ed195a88b.jpg)

然后需要等待命令执行，大约5分钟，如下图所示：

![img](https://user-images.githubusercontent.com/52620310/62406009-22536e80-b5d7-11e9-826b-e1f1b0774db9.jpg)

会在下面的图片过程中等待一会儿

![img](https://user-images.githubusercontent.com/52620310/62406011-267f8c00-b5d7-11e9-8ac1-67599ff1facb.jpg)

最后完成后需要重启，根据提示输入：y，重启服务器即可生效

![img](https://user-images.githubusercontent.com/52620310/62406015-2bdcd680-b5d7-11e9-9aec-fdf762a5f191.jpg)

如果错过了重启步骤，直接输入重启命令命令：

> reboot

![img](https://user-images.githubusercontent.com/52620310/62406018-31d2b780-b5d7-11e9-819b-baa65e585c47.jpg)

然后耐心等待，待服务器重启后即可自动开启 SSR 加速。(这里注意如果是 centos 7 系统重启后可能防火墙阻止了 SSR，需要关闭防火墙，如果是 centos 6 就不会有这个问题，所以我们建议使用的是 Hostwinds 的 centos 6 操作系统。)













#### 若ip被墙，则进入官网免费换一个ip（仅一次）

![image-20221026184905637](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026184905637.png)

![image-20221026184919700](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026184919700.png)

![image-20221026184931706](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026184931706.png)



跟着步骤直接发送操作



！！等（忘记需要多久）

加成功后会出现

![image-20221026185052986](C:\Users\至\AppData\Roaming\Typora\typora-user-images\image-20221026185052986.png)

使用此ip可继续科学上网



