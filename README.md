# win10Stuff
some win10 log



1.

GLK
Windows 10 企业版 LTSC 2019：M7XTQ-FN8P6-TTKYV-9D4CC-J462D

slmgr /ipk xxxxx-xxxxx-xxxxx-xxxxx
slmgr /skms kms.03k.org


slmgr /ato

slmgr /dlv


其实这个东西已经不新鲜了，不过很多人来问，我就简单写写，（明天还要早起出去玩

首先别问win10政府版在哪里下载，我不是，我没有

不过你嫌麻烦的话可以到这里下载镜像：

Windows10政府版64位镜像ISO



然后我告诉你怎么得到传说中的windows10政府版本。

首先你的win10要是专业版或者企业版（LTSB不行），然后打开你的设置：



点击更改产品密钥

输入下面这个key：

YYVX9-NTFWV-6MDM3-9PT4T-4M68B



然后就会弹出升级提示：



嗯，当然是点击开始了



耐心等待然后会自动重启。



重启之后显示升级成功。

重启之后，就变成未激活了，不要慌，继续。

这个时候就用管理员打开命令行，输入：

 slmgr /ipk YYVX9-NTFWV-6MDM3-9PT4T-4M68B

slmgr /skms kms.03k.org

slmg /ato

 

slmgr /skms 127.0.0.1

然后无意外就可以激活成功了：



 



可以看到，政府版是企业版G，G大概是Gov的意思（瞎蒙

然后我们再看一下传说中的400年：

管理员打开命令行输入下面命令：

slmgr /dlv



系统产品名称是Windows EnterpriseG edition。

看圈圈的那个数字。150000/365=410.958904 。传说中的400年不过期说的就是这个意思。某种意义上的用KMS永久激活。

而我们说KMS有效期就半年说的是这个意思：



就是180天内都不连kms服务器就会掉激活。

所以激活了之后可以把激活服务器地址设置成本地，这样就不会联网了，反正400年过期不是

slmgr /skms 127.0.0.1

关于400年激活的测试，参见这篇文章：

测试下400年的KMS激活


2.office 
cd "C:\Program Files (x86)\Microsoft Office\Office16"

1
cscript ospp.vbs /sethst:kms.03k.org
cscript ospp.vbs /act
