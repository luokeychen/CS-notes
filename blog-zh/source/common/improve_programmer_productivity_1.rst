.. Author: Tower Joo<zhutao.iscas@gmail.com>
.. Time: 2009-11-09 21:23

========================================
如何提高程序员的生产率(一)
========================================


本博客所有内容采用 `Creative Commons Licenses <http://creativecommons.org/about/licenses/meet-the-licenses>`_  许可使用.
引用本内容时，请保留 `朱涛`_, `出处`_ ，并且 **非商业** .

点击 `订阅`_ 来订阅本博客.(推荐使用 `google reader`_, 如果你的浏览器不支持直接订阅,请直接在 `google reader`_ 中手动添加).

点击 `下载pdf阅读`_.


摘要
========================================

1周前看了某个园子里的同学(忘了名字了,不好意思)推荐的 `The Productive Programmer`_ , 于是在
上周便看了这个200多页的书, 如果哪位同学想只看下精要部分, 可参考 `slideshare`_.

本文在简单地谈谈这本书外,会主要介绍一些可以供程序员日常使用的能够切实提高生产率的方法.


.. contents::


引入
=========

不知道各位读者是否曾经见过在键盘上运指如飞的程序员, 不知道是否经历过当同事已经完成了任务,你还没有跟上他的脚步?

记得在研一的时候,去一家公司面试java程序员, 那个很胖的leader为我配j2ee环境时的神奇,我目瞪口呆地看着他完成了所有的
配置, 然后他冲我笑笑, 说"来,轮你了,开始写程序吧", 我这才从刚才那奇妙瞬间回过神来.

实习的事已经记不太清了,却从那刻起我开始知道, 一个人的生产率是可以提高的! 而带来的提高却是大大地节省时间,来提高
工作效率.

于是我开始留意和训练自己.


The Productive Programmer简单Review
========================================

上周前, 我看了某位同学写的一篇关于此书的书评, 单冲着这书名我是一定要看的.

上周便或细致或粗略地翻阅了一遍(不同的章节),简单地说下我的一些看法.

#. 书中尽量使用通用的计算机语言和工具,但是java确占了绝大部分(或许叫The Productive Java Programmer,会比较合适,
   当然作者是ThoughtWorks的职员,也难免)
#. 总体来说,是相当值得一读的书, 读后,至少你会知道, **原来有更好,更快的方式** 来解决这个问题
#. 慎重去选择工具和方法,所谓的 **过犹不及**

看了后,我不免也想总结和收集一些自己每天都在用的提高生产率的方法,于是便有了写本文的想法.

下面我会主要介绍,我在日常中用来提高效率的一些比较重要的方法.


命令行
===============

从开始使用Linux,我便喜欢上了命令行,从此后,无论是Linux(Ubuntu, Fedora, opensuse等), 或者Windows, 我都会尽量将工作
使用命令行来完成, 命令行有什么好处呢:

快速的操作
------------

我们通常大量的时间花在不同的目录的切换上,例如, 有下面的目录:


::

    .
    |-- A
    |   `-- AA
    |       `-- AAA
    `-- B
        `-- BA
                `-- BAA


A/AA/AAA目录下有个文件a.txt要复制到 B/BA/BAA目录下,如果完全使用鼠标,则需要(假设目前在AAA目录下):
复制a.txt(1次鼠标右键, 1次鼠标左键选择复制)
到B目录下(1+1+1+1)
复制到B目录(1+1)
回到A目录(1+1+1+1)

共需要12次鼠标操作.

那么如果我们使用命令行:


::

    Linux: ~$ cp a.txt ../../B/BA/BAA/ (回车即可)
    Win: C:/> copy a.txt ../../B/BA/BAA/ (回车即可)

所以命令行带来的好处的显而易见的, 如果算上时间的因素,大致在这个示例中会快6倍以上.

这只是个简单的例子, 你是否想过自己每天都在用鼠标做着同样的事情, **是提高效率的时候了**.


专注
----------
还是以上面的示例来说明, 想象下,你当前在处理的是项目的环境搭建工作, 你需要复制一个文件,
而复制只是一个过程,它是服务于 **环境搭建** 这个目的的,
如果你在别的辅助工作上花费了过多时间(上例中的复制操作), 要重新切换回自己的真正目标,
会产生额外的切换成本,甚至你可能都忘了你究竟是要做什么的(是否有过为了一个编程题查相关的语法,结果最后
居然去看美女,而忘了自己的编程题).

这里的切换成本是与花在辅助工作的时间成正比的,达到一定的程度,切换成本会致使程序员无法现切换回真正的目的上.自然就会
影响到这里所谓的专注.


鼠标
-----------

你喜欢使用鼠标吗? 答案肯定是 "YES", 但是 **通常来讲** 效率(当然指的是编程人员的操作)与鼠标的使用频度是成反比的,
鼠标使用的越多,效率越低.

在后续的部分会更加详细地说明, 参考快捷键部分.

推荐阅读 `完全用命令行工作-1 拔掉你的鼠标`_ 系列文章.


快捷键
=============

你在写程序时突然有了某个灵感,于是你想记录下来,你从开始菜单中找到程序,再找到附件,最后你打开了记事本, 
不知道你这样做了多久,才开始想为什么不把它做个快捷方式呢? 于是你把它放在在桌面的快捷方式, 不过每次你还得
显示桌面后才能打开, 你又把它加到了快速启动, 不过还得点击一下(或者二下)鼠标.

终于一天,你大悟找到了 `autohotkey`_ , 于是一个 CTRL_ALT_N 便搞定了, 欣喜之余,你加入了常用的快捷键,
如画图, 如dos等.

生活开始美好了,你解放了自己的鼠标!

所以,尝试着使用快捷键吧!

除了日常的一些桌面操作外,你还需要熟悉你最常用其它基于web的软件的快捷键,如gmail, google doc, google reader等.

用"c"命令来写邮件总比点下写邮件要快吧.

当你习惯了快捷键时,可能会出现下面一种情形, 那就是 **你设置了过多的快捷键**, 多到你开始记不住了, 分不清楚了,于是
你每次都得去查manual,你得确认你的快捷键. 所以如何保证一个合适大小的快捷键集是重要的.

我给几点建议:

#. 尽量使用统一的快捷键(无论是桌面或者web的应用, 如果不统一,你要去自定义,使其统一, 而不是记住新的)
#. 根据使用频率来决定哪些快捷键具有记忆的更高优先级,哪些有较低的优先级(如我大量使用的vim,我当然要记住更多的快捷键)
#. 适当的冗余来减少快捷键的集(如,在windows中,你可以使用 `autohotkey`_ 来指定打开某个程序,但是我通常会将最常用的
   使用 `autohotkey`_, 次常用的使用windows自身的开始快捷键, 点击WIN键,点击j再点击q,便打开了QQ, 注意:我在开始菜单中
   加入了一个jump目录,其中放有QQ的快捷方式)




后记
========================================
本文的后续篇会继续说明, 

#. 自动化
#. 编辑器
#. 其它的细节

这些内容在下篇中会进行说明.

另,欢迎大家留言来说明自己常用的一些提高生产率的方法.谢谢.

参考资料
========================================

#. `完全用命令行工作-1 拔掉你的鼠标`_
#. `The Productive Programmer`_

本文的rst源码
========================================

本文的源码链接在 `这里`_ .

点击 `下载pdf阅读`_.


.. _朱涛: http://sites.google.com/site/towerjoo
.. _出处: http://www.cnblogs.com/mindsbook
.. _订阅: http://feed.feedsky.com/MindsbookTowerJoo
.. _google reader: http://reader.google.com
.. _这里: http://groups.google.com/group/python-share/web/improve_programmer_productivity_1.rst
.. _The Productive Programmer: http://www.douban.com/subject/3073403/
.. _slideshare: http://www.slideshare.net/adorepump/the-productive-programer-mechanics-presentation
.. _autohotkey: http://www.autohotkey.com/
.. _完全用命令行工作-1 拔掉你的鼠标: http://blog.youxu.info/2008/09/04/unplug-your-mouse/
.. _下载pdf阅读: http://groups.google.com/group/python-share/web/%E5%A6%82%E4%BD%95%E6%8F%90%E9%AB%98%E7%A8%8B%E5%BA%8F%E5%91%98%E7%9A%84%E7%94%9F%E4%BA%A7%E7%8E%87%28%E4%B8%80%29.pdf
