[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fthokaka92%2Froot-tools.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fthokaka92%2Froot-tools?ref=badge_shield)

RootTools·Neo
=======================

* <font color=red>RootTools·Neo 正式发布啦~</font>

* RootTools 是一款专注于给 root 后的用户提供方便的软件。主要提供：
	* ```应用冻结``` 不删除系统内的应用，而是将其冻结，在需要时可以解冻，但是别乱来哦，冻错了会无法开机，只能双清；
	* ```组件管理``` 一个应用内往往包含大量的『四大组件』并且持续耗电，这个功能可以帮助禁用组件，但是最大程度上不影响应用的正常使用；
	* ```深度清理系统``` 运行久了，总会有各种各样的缓存，特别是 ART 缓存很难清理，留着会造成一些奇怪的问题，清理 ART 事不宜迟；
	* ```深度清理内存``` 一键杀掉各种疑难杂症的后台应用，尽可能的释放内存，让手机回到刚开机时的状态。
	
* 同时也针对目前海量用户的 MIUI 系统进行相应的优化：
	* ```去除系统广告``` 不知从何时起，MIUI 充斥着广告，这个功能将最大限度的帮助清理掉广告，以及各种带广告的闪屏页；
        * 针对广告的问题，在软件内开设了反馈的入口，当您发现了广告时，可以截图并通过该入口进行反馈；
        * 去广告同时也需要 root 权限，因为会向 hosts 写入数据，而 MIUI 要实现写 hosts 还必须解除 /system 分区的锁，解锁方法请自行搜索；
	* ```去除通知栏搜索和负一屏``` 反正对于不常用的东西就是没啥好感，能够去掉的话就去掉吧；
	* ```root 25 秒等待``` 又一个反人类设计，说好的为发烧而生呢，只能用一些黑科技来去掉这该死的 25 秒了，是谁说的时间就是金钱。
	
* 为了实现如去除广告等功能，必须借助 xposed 框架，以实现对目标方法的 Hook 和修改。因此要求用户的手机已安装 xposed 框架，请特别注意 MIUI 需要专用的 xposed，请自行搜索。

* 本软件会跟随 MIUI 版本更新而更新，尽可能让用户的手机保持在一个干净无广告的状态下，平均的发版本频率为每周一次。

- - -

* 本软件遵守 GPLv2 协议, 并坚持免费和开源, 保持更新。不接受代理、转卖等各种商业行为, 也不要求捐赠, 完全将软件的使用权利交给用户。
* 您甚至可以下载并修改这份源码, 在 GPLv2 允许的条件下自行发布版本。

- - -

* 编译软件

	* 系统必备 jdk8 和 gradle 4.4 以上
	
	```
	$ git clone https://github.com/rarnu/root-tools
	$ cd root-tools/RootTools2
	$ gradle clean build
	```

	* 如果您还需要自行编译 JNI 部分，可以自行下载 [CodeTyphon](http://www.pilotlogic.com/sitejoom/index.php/codetyphon/)，并编译其 Cross Elements 以适应 Android 跨平台编译（目前仅支持 Linux 环境，不需要额外安装 NDK）。源码中已提供编译脚本
	
	```
	$ fpccmd A64 cmd.lpr   ## 编译 arm64-v8a 的 so
	$ fpccmd AA cmd.lpr    ## 编译 armeabi-v7a 的 so
	$ fpccmd AI cmd.lpr    ## 编译 x86 的 so
	```
	
	* 此时即可以得到工作于 arm, mips, x86 三个平台的 libcmd.so
   
- - -

### 目前软件已不再更新，当前版本适配了 Android Q 以及 arm64-v8a。

## Good Luck!

## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fthokaka92%2Froot-tools.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fthokaka92%2Froot-tools?ref=badge_large)