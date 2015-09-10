#User Agent

##[概述][5]
User Agent也简称UA。它是一个特殊字符串头，是一种向访问网站提供你所使用的浏览器类型及版本、操作系统及版本、浏览器内核、等信息的标识。通过这个标识，用户所访问的网站可以显示不同的排版从而为用户提供更好的体验或者进行信息统计；例如用手机访问谷歌和电脑访问是不一样的，这些是谷歌根据访问者的UA来判断的。UA可以进行伪装。

userAgent字串说明:

1. 浏览器标识(大部分为 Mozilla/)
出于兼容及推广等目的，很多浏览器的标识相同，因此浏览器标识并不能说明浏览器的真实版本，真实版本信息在 UA 字串尾部可以找到。

2. 操作系统标识
Linux i686
Linux x86_64
PPC Mac OS X
Intel Mac OS X
Windows NT 6.1(windows7)
Windows NT 6.0(vista)
Windows NT 5.1(xp)
Windows NT 10.0(windows10)

3. 加密等级标识
* N: 表示无安全加密
* I: 表示弱安全加密
* U: 表示强安全加密

4. 浏览器语言
在首选项 > 常规 > 语言中指定的语言

5. 渲染引擎
显示浏览器使用的主流渲染引擎有：Gecko、WebKit、KHTML、Presto、Trident、Tasman等，格式为：渲染引擎/版本信息

6. 版本信息
显示浏览器的真实版本信息，格式为：浏览器/版本信息
注：
*在广告定向设定中，浏览器定向和操作系统定向均是针对User-Agent中的信息进行定向。*



###PC端user-agent


###移动端user-agent
[一些手机端的user-agent](http://www.cnblogs.com/relax/p/3487714.html)
[ios的user-agent大全](http://www.enterpriseios.com/wiki/UserAgent)


##历史
###[user-agent字符串史][1]

* Mozilla/	由Netscape最开始有,是其产品名，IE为被当时的浏览器嗅探识别伪装也加上了Mozilla/
* Gecko  firefox的渲染引擎，苹果自主研发了webkit，是KHTML渲染引擎的一个分支，为溶入主流不被踢出局伪装加上(like Gecko)
凡是基于 WebKit 的浏览器都将自己伪装成了 Mozilla 5.0，与基于 Gecko 浏览器完全一样。但 Safari 的版本是浏览器的构建版本号(build number)。Safari 1.25 在 user-agent 字串中号为 125.1(如上所示)。
* Opera 浏览器默认 user-agent 字串是现代浏览器中最合理的－－正确的标识了它自己及其版本。
Opera/Version (OS-or-CPU; Encryption) [Language]

###[各大浏览器诞生年表][3]

1993年1月23日：Mosaic
1994年12月：Netscape 			(Gecko)
1994年：Opera
1995年8月16日：Internet Explorer
1996年10月14日：Kongqueror (KHTML)
2003年1月7日：Safari				(webkit基于KHTML)
2008年9月2日：Chrome				(webkit)

* 新的chrome的渲染引擎是基于webkit的blink
* 新版firefox以及Opera也使用了blink

##总结
user-agent 字串史可以说明曾对 user-agent 嗅探说不的原因：IE 想要将自己识别为 Netscape 4，Konqueror 和 WebKit 想要识别为 Firefox，Chrome 想要识别为 Safari。这样使得除 Opera 外所有浏览器的 user-agent 嗅探区别很小，想要从一堆茫茫浏览器海洋中找出有用的标识太少了。关于嗅探要记住：一款浏览器与其它浏览器是兼容的，这样造成了不能完全准确的断定是哪款 浏览器。

##工具
* [user-agent浏览器切换插件(user-agent-switcher)](https://chrome.google.com/webstore/detail/djflhoibgkdhkhhcedjiklpkjnoahfmg)
* [浏览器user-agent列表(xml格式)](http://techpatterns.com/forums/about304.html)
* [user-agent分析](http://www.useragentstring.com/index.php)

###[手动修改浏览器user-agent](http://www.iefans.net/user-agent-weizhuang-liulanqi-caozuoxitong/)



[1]:[http://www.blogdaren.com/post-2194.html]
[2]:[https://en.wikipedia.org/wiki/User_agent]
[3]:[http://nonfu.me/p/8262]
[5]:[http://blog.csdn.net/q809204304/article/details/17714175]
