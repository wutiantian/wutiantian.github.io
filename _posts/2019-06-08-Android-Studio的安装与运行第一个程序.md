---
layout: post
title:  "Android-Studio的安装与运行第一个程序&翻墙"
date:   2019-06-08 19:16:25 +0800
---
作者：吴甜甜  
个人博客网站： wutiantian.github.io

---

#  Android-Studio的安装与运行第一个程序&翻墙



写于2019年6月，用最新的版本为AS3.4.1。其默认的Gradle为gradle-5.1.1-all.zip

![AS版本](/images/AS版本.png) 

个人建议 最好把这些最原始安装包都备份一遍 有时候导过来的项目的版本高于你Android studio 的话 它会强制让你升级的 然后会各种奇怪的报错 ，有时候解决不了弄烦了就删掉重装吧比较省事。

# 为什么写这篇文章？适合什么人看？

初学者，只需要运行“Hello World”就已经满足。What ! 我只是新建两个文件名而已，还没说要当伟大的程序员， 还没有敲一行代码，最后一行就是转不完的圈圈，控制台就显示报错！宝宝好委屈！运行的箭头灰色的，让人心如死灰呀。

想知道为什么？看下去吧。

再遇到此类情况就不会再难过，这就是时间带来的经验，累积的处理方式。

# 软件下载

网址

>www.androiddevtools.cn



这是个中文社区，官网有的都会在这个社区更新。可以不用连vpn直接下载

新建了Hello world项目，运行就卡在 Gradle:Executing tasks。

# 编译卡在Gradle环节解决办法

**此操作只一次，以后就不用重复！**

下载Gradle离线包地址（因为AS软件在线时间太长还不一定成功，需要翻墙，方法见附录一个标题）：

>http://services.gradle.org/distributions/ 



将解压后的gradle-xxx-all.zip文件放入gradle缓存目录的指定路径下。

>D:\android1\gradle\wrapper\dists\gradle-5.1.1-all\97z1ksx6lirer3kbvdnh7jtjg\gradle-5.1.1-all.zip



首先找到你的gradle缓存目录，在\wrapper\dists\gradle-xxx-all\xxxxxxxxxxxxxxxxx\目录下就放着各种版本的gradle。使用Android Studio导入你没有的gradle版本编译的项目时，界面一直加载build Gradle，这时强退Android Studio（正常关闭软件的叉号是没有用的！）。找到gradle缓存目录下的路径\wrapper\dists\，这是会自动新生成一个gradle-xxx-all\xxxxxxxxxxxxx路径，其中包含文件gradle-xxx-all.zip.lck和gradle-xxx-all.zip.part文件,拷贝下载解压后的gradle-xxx-all.zip到这个路径，并删除gradle-xxx-all.zip.lck和gradle-xxx-all.zip.part文件，运行Android Studio导入这个项目，系统自动读取识别。

将gradle-5.1.1-all.zip压缩包放到图片路径下，注意不要解压！（系统如果没发现该压缩包就自动去国外下载了）
软件系统发现该压缩包后会自动解压！


![gradle缓存目录](/images/gradle缓存目录.png) 
注意：这里自己解压的```gradle-5.1.1```文件夹不起作用


![gradle缓存目录安装包存放地址](/images/gradle缓存目录安装包存放地址.png) 


OK，问题解决了。

打开AS软件，开始 ```Build```菜单下重新编译

最底行还是会有圈圈，但不用怕，一分钟即可。

sync dependencies 需要时间还是编译运行必须的步骤，这步骤不可省略，时间不会太长，一个Helloworld等待一分钟以内。
在这里插入图片描述在这里插入图片描述



![GradleSync](/images/GradleSync.png) 


![HelloWorld运行成功](/images/HelloWorld运行成功.png) 

如果看到这画面，都是亮的，那你就是这台电脑里最靓的崽！运行成功！




# 附录-查看自己的项目要求的gradle版本

打开自己项目所在的文件夹，例如“HelloWorld”文件，找到gradle文件夹下的wrapper文件夹下

>D:\asworkspace\HelloWorld\gradle\wrapper


![查看自己项目要求的gradle版本](/images/查看自己项目要求的gradle版本.png) 


用文本文档打开```gradle-wrapper.properties```文件，查看版本



# 附录-如何免费稳定快速翻墙

蓝灯软件，**每个月有500M的免费试用高速流量**，速度到达当前电脑的最大物理带宽。

因为gradle依赖的仓库都在国外，而国内访问国外网络都情况大家也都懂得。





打开网址：

https://github.com/getlantern/download


![lantern下载](/images/lantern下载.png) 

![蓝灯打开页](/images/蓝灯打开页.png)



点击下载，浏览器会添加到自动下载列表，文件会在浏览器默认文件夹中，打开即可自动安装。

点击桌面蓝灯图标，立即会出现默认浏览器页面弹出。
此时不要点击页面上任何付费按钮，每月免费500M高速流量试用已经满足大部分学生学习使用。在这里插入图片描述

首次打开蓝灯网页和右下角图标可能要等3分钟（等它分配节点）才能由**灰色不可用**变为**彩色可用**。

第二次打开以后就能秒连接了！
