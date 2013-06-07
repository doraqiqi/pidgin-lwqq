pidgin-lwqq
===========

简  介
-----
为linux的pidgin提供qq协议,基于webqq服务.
是在[lwqq](https://github.com/mathslinux/lwqq)基础上开发而来.
lwqq库是一个非常严谨有效的webqq协议的库.  
lwqq 即是 linux webqq 之意

效  果
------

![gnome3](http://i.imgur.com/8kuEPHI.png)

想实现上面的效果? 猛击:[gnome3集成聊天](https://github.com/xiehuc/pidgin-lwqq/wiki/gnome3-support)

快速安装
--------

### 从源代码编译

    cmake ..
    make
    sudo make install

第一次使用? 猛击:[简易使用教程](https://github.com/xiehuc/pidgin-lwqq/wiki/simple-user-guide)

### 编译选项

- VERBOSE[=0]
> 设置输出等级 .0表示没有输出,3表示最大输出.

- SSL=[On]
> 开启SSL的支持

功能列表
--------

### pidgin

* 支持发送接受 好友|群|讨论组 消息
* 支持发送接受图片
* 支持发送接受表情(在设置中使用webqq表情主题)
* 支持发送接受 输入提示|窗口摇动
* 支持设置 好友|群|讨论组 备注
* 完整支持讨论组
* 支持头像
* 支持更改好友分组
* 支持确认添加好友请求
* 支持群的临时会话
* 支持访问QQ空间
* 支持更改在线状态|群名片
* 支持多账户登录
* 支持发送接受离线文件
* 支持文本样式
* 支持群消息屏蔽
* 支持接受文件传输
* 支持本地QQ号缓存机制
* 支持添加好友|群
* 支持下载漫游记录

### empathy not support ###

由于telepathy-haze无法顺利的创建本地缓存，造成
性能低下，所以不推荐使用empathy配合lwqq。


已知问题
--------

* pidgin使用明文保存密码
    请配合使用[pidgin-gnome-keyring](https://code.google.com/p/pidgin-gnome-keyring/)并开启插件

* 当libcurl版本低于7.22.0时可能造成图片发送失败

*telepathy-haze 本身不支持群组聊天和图片显示.比较纠结.*

**注意:**
telepathy-haze 比较坑爹.居然不保存好友列表.!!
它只在/tmp/haze-XXXXXX 存放下文件.
所以速度非常受影响.
不知道为什么要这样设计.


