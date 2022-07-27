#####注：现在还没有发布！
#OurOs,YourOs
##前言
OurOs是一个基于win32开发的操作系统，软盘启动。虽然大小不过1.44MB，但是功能强大。能够上网，玩游戏，看视频，写文章，画图，还能够自制程序（虽说要在电脑上再次编译罢了）。

不过嘛，有一点可能会让用着老电脑的Windows用户崩溃。就是这款操作系统是用DeepinLinux开发的（两点：一、本来Linux就是面向开发者的，开发工具也很多。二、之所以用deepin，主要是国产出身，而且操作界面也类似于Windows<就是命令不大一样了（>_<）>），而且似乎无法在Windows上跑（毕竟Windows的nasm是不支持生成elf的）。

所以，各位Windows用户，三条路：“要么直接装linux，要么就用虚机装，要么就别开发了。”（笑）

不过，如果电脑硬盘空间很大的话（其实作者的电脑只有一个250G
左右的硬盘，但还是装上了。(>_<)），也可以考虑装双系统，毕竟deepin装双系统很简单了：划一个分区，然后加个根分区和交换分区就好了。也不用装其他的第三方软件，就搞定了。当然，用这样的方法在装点别的也没问题。

还是推荐用着老电脑的Windows用户装双系统，或者用虚拟机装乌本图操作系统，不要用虚拟机装deepin，不然你会卡崩溃的...(苦笑)。

当然，实装deepin也有很大的好处：我的电脑是2013年的，Intel i7 pro，8G内存，推荐装windows7（苦笑），装上win11后...（二次苦笑）。但是，当我装上deepin后，电脑直接起飞！！！（笑）

####话说，我们是不是跑题了？？？

##开发环境配置
以下是本次开发需要另行安装的工具：

- nasm
- qemu
- qemu-kvm
- gcc

可选下载工具：

- vim

当然，如果懒得输命令，在同目录里有一个config.sh，你可以把他拷贝到任意文件夹里，让后运行它，他就会帮你配置环境。中途要输密码的那是要安装软件，直接输就行了。

还有一点要注意的是，它会自动安装vim，vim是linux下最强编辑器。由于是靠命令行启动，所以很少人会用，在进入vim编辑界面或编辑完成时，要输入“:wq”才能保存并退出，注意，一定要输入“:wq”才行！

###vim的基本用法
- “vim 文件名”可以启动vim，如果是旧文件就会打开，新文件就会创建
- 按i可以进行编辑
- 按esc可以退出
- 退出后，先输入“:w”保存，在输入“:q”退出，也可以直接“:wq”保存并退出

##特色
PandaOs系统开发用了整整一年时间，虽然大小还没有1.44MB，但是功能很丰富，完全可以把自己家的老电脑换系统了（笑）。功能如下：

- [x] 拥有启动图形界面
- [X] 拥有操作图形界面
- [X] 能够对文本、图像进行处理
- [X] 能够播放mp4和mp3的音频文件
- [X] 拥有图形化文件系统
- [X] 拥有网络支持
- [X] 自带游戏“超级马里奥”
- [X] 大小不过1.44MB

系统方面主要就是这些功能，其他的相信你们也能够体会到。但是...

###重点不是系统本身！！！
OurOs与其他系统最大的差别是，对GCC里的几乎所有标准函数都进行了重写(一般是P_GCC标准函数名)，因此对开发者极其友好（也是让作者再用C语言写程序时省心了[>_<]），大家可以随心所欲的用标准函数写自己的应用。

当然了，如果你愿意把你写的程序发在评论区，那就谢谢你了（不过嘛，大家不要误解，没有奖金的！（笑））！！！(>_<)

##缺陷
我感觉这个操作系统几乎没有缺陷（笑），不过，只有三点，那就是：
- [ ] 启动动画只是一张图片
- [ ] 网卡只支持NVIDIA网卡
- [ ] 马里奥只有一关，不爽！
  
除此之外，若有其他的bug，大家就想想《30天自制操作系统》作者的那句话吧：

`
看上去弊端很多的开源方式，其实也有好的一面。如果用户跟你抱 怨“请加上一个○○的功能吧”、“××功能没什么用啊，去掉吧”、“bug太多 了，帮帮忙”之类的话，你可以说： “这个是开源软件，请自己修改好了（笑）。
`
##后记

###部分代码问题

大家其实仔细阅读一下源代码，就能够发现IPL和asmhead.asm，完全与其他代码风格不一样，不要意思那是我ctrl+c ctrl+v来的，实在抱歉。

因为作者其实是个学生党，才刚上初中，所以学汇编就学的很难，干脆就复制粘贴来了，（<>_<>）也参考了部分程序的写法，很抱歉

###deepinLinux真的有那么神？？？

deepin作为一个国产操作系统，在用户体验、生态问题都得到了很好的解决。

deepin的自带商店里有很多常见应用：wps，微信，QQ等。而且还有很多wine和apk软件，并且都是经过适配的。deepin又基于debian开发，debian其本身的软件生态也很好，所以生态并没有那么差。

deepin的用户体验也很好：1、deepin为了满足国人习惯，特意设计了Windows和Mac-OS风格，也符合国人习惯。2、deepin超耐看！其本身的特效模式就够好看的，更别说加入幻梦壁纸和KDE系统设置了！

###感谢
在此感谢以下作者与书籍：
- 《30天自制操作系统》
- 《orange's 一个操作系统的实现》
- ghosind在gitee的https://gitee.com/ghosind/HariboteOS
