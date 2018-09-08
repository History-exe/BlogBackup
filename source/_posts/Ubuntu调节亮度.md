---
title: 使用软件调节Ubuntu的屏幕亮度
categories: Linux
tags:
- Linux
- Ubuntu调节亮度
---
由于对Linux系统感兴趣，前段时间给笔记本装上了双系统。主用Windows10，备用Ubuntu。

起初Ubuntu安装十分顺利，按照网上的教程下载镜像、用U盘制作安装盘、分区、进入BIOS调整启动顺序。一切正常。Ubuntu启动成功。可就是有一件事不太完美。不能调节屏幕亮度，屏幕十分亮瞎眼。

<!--more-->

具体表现就是按笔记本上的快捷键Fn和相关组合键调节亮度时，亮度条确实在动，但屏幕实际亮度没有变化。我之前试过使用命令行和修改设置文件的办法。但是都没有用。其中有一种方法使用之后，电脑提示我没有相关的brightness文件。

上网搜索解决办法。搜索关键字 `“Ubuntu 没有brightness文件 调节亮度”`，找到了这篇文章《[Ubuntu16.04/16.10下缺失brightness设置，解决屏幕亮度调节的问题](https://blog.csdn.net/HedWater/article/details/75465110)》。文章里的描述和我的情况很相似。按照文章里的操作安装了一个调节亮度的软件——**brightness-controler**。软件是图形界面的，很有好。

在这里我写上安装的一些指令。以作备份之用，想看更详细的描述请前往上面的文章查看。
“$”后面的是代码，每次执行一行。

``` bash
$ sudo add-apt-repository ppa:apandada1/brightness-controller
$ sudo apt-get update
$ sudo apt-get install brightness-controller
启动方式
$ brightness-controler       
安装完毕后可以在全部程序里看到图标，在图标上点击鼠标右键，有选项可将其附在菜单栏，方便随时调节。
```

这个方法并不会在每次开机时自动设置亮度，因此你要每次手动设置。还有就是我遇到过亮度自动失效的情况，比如通过浏览器点开一个视频，或者通过右上角的设置锁屏的时候，屏幕亮度都会回到最高。

文章索引<https://blog.csdn.net/HedWater/article/details/75465110>