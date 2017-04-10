专业技能
========

..
  Show Source? 别看了，加入我们吧 ;-)
  http://blog.knownsec.com/2012/02/knownsec-recruitment/

原则
----

* 至少完整看完与练习好一本书
* 至少过一遍官方文档

基础必备
--------

HTTP 抓包与调试
~~~~~~~~~~~~~~~

Firefox 插件
""""""""""""

* Firebug/Firecookie

  + 抓包与各种调试

* Tamper Data

  + 拦截修改

* Live HTTP Headers

  + 重放功能

* HackBar

  + 编码解码/POST 提交

* Modify Headers

* 修改头部

Fiddler
"""""""

* 浏览器代理神器
* 拦截请求或响应
* 抓包
* 重放
* 模拟请求
* 编码解码
* 第三方扩展

  + Watcher

    - Web 前端安全的自动审计工具

Wireshark
"""""""""

* 各种强大的过滤器语法

tcpdump
"""""""

* 命令行的类 Wireshark 抓包神器

Python
""""""

* urllib2

  + 打开请求响应调试

    - 编辑 urllib2 的 do_open 里的 h.set_debuglevel
    - 改为 h.set_debuglevel(1)，这时可以清晰看到请求响应数据，包括 HTTPS

什么是跳转
~~~~~~~~~~

服务端跳转
""""""""""

* 302

  + <?php header("Location: 3.php"); ?>

* 301

  + <?php header("HTTP/1.1 301 Moved Permanently"); header("Location: 2.php"); ?>

* u = urllib2.urlopen(url) 后，u.url 能得到服务端跳转后的地址

  + urllib2 自己的特性
  + 所谓的会跟进去

客户端跳转
""""""""""

* <meta http-equiv="refresh" content="0; url=http://www.evilcos.me" />

  + htmlparse 解析就行了

* location.href = "http:/" + "/evilcos.me";

  + 正则解析（弱）
  + JavaScript 引擎解析（强）

Office 能力
~~~~~~~~~~~

* Word 文档编写，看去要专业，尤其对外的
* Excel 里面大量的统计、图表功能，需要善于使用
* PPT 演讲、培训等必备，如何做好 PPT？百度一下...
* 进一步

  + yEd
  + Visio
  + Freemind

    - 本技能表就是这个制作

上手 Linux
~~~~~~~~~~

* 《鸟哥的 Linux 私房菜》

熟练 Vim
~~~~~~~~

* 实战至少 3 回合：http://coolshell.cn/articles/5426.html

上手 Python
~~~~~~~~~~~

* https://www.python.org/dev/peps/pep-0008/
* http://learnpythonthehardway.org/book/

《Python 核心编程 2》
"""""""""""""""""""""

* 第 4 章 Python 对象

  + 完整熟练

* 6.8 Unicode

  + 完整熟练

* 8.11 迭代器和 iter() 函数

  + 完整熟练

* 第 9 章 文件的输入和输出

  + 完整熟练

* 第 10 章 错误和异常

  + 完整熟练

* 第 11 章 函数和函数式编程

  + 完整熟练

* 第12章 模块

  + 完整熟练

* 第14章 执行环境

  + 完整熟练

* 第15章 正则表达式

  + 完整熟练

* 第18章 多线程编程

  + 完整熟练

* 20.2 使用 Python 进行 Web 应用：创建一个简单的 Web 客户端

  + 完整熟练

算法
~~~~

* 快排
* 二分

正则表达式
~~~~~~~~~~

* 调试工具

  + Kodos
  + RegexBuddy

    - 支持多种语言
    - 支持调试优化

  * http://www.regexper.com/

    + 正则图解

* 正则表达式30分钟入门教程：http://deerchao.net/tutorials/regex/regex.htm
* http://wiki.ubuntu.org.cn/Python正则表达式操作指南
* 《精通正则表达式》

研发能力
~~~~~~~~

瀑布模型
""""""""

* 需求 -> 需求分析 -> 设计 -> 开发 -> 测试 -> 上线 -> 运维/运营

需求分析能力
""""""""""""

* 给你一个需求，如何给出一个优美的执行思路——方法论
* 这个能力非常非常非常的关键

调试能力
""""""""

* 只要定位出，就没有解决不了的 Bugs
* 肉眼看到的都是假象

  + 一定要专业的工具与经验配合

* Bugs 在哪出现，最终就在哪进行真实模拟调试
* 缩小范围

  + 构建自己的测试样例

    - 排除网络复杂未知情况

  + 关联模块一个个排除
  + Python 单步调试

    - import pdb; pdb.set_trace()
    - 在需要单步调试的地方加上面这句，运行程序后中断在此，然后h查看指令进行一步步细细调试

  + 粗暴调试：print

敏捷思想
""""""""

* 快速迭代
* 任务拆细
* v1原则：定义好 v1 的目标，快速完成 v1 为优先
* 习惯 WiKi 记录，利于沉淀与分享

翻墙
~~~~

* 优雅解决方案
  + shadowsocks + 一台海外 VPS + Chrome(SwitchyOmega)/Firefox(AutoProxy)
  + 详情了解：http://mp.weixin.qq.com/s?__biz=MzA3NTEzMTUwNA==&mid=210457700&idx=1&sn=322d1e4c13d3f33ade848e3889c410bf#rd

* SSH 隧道

  + http://www.ibm.com/developerworks/cn/linux/l-cn-sshforward/index.html
  + 本地转发

    - ssh -L <local port>:<remote host>:<remote port> <SSH hostname>

  + 远程转发

    - 反弹
    - ssh -R <local port>:<remote host>:<remote port> <SSH hostname>

  + 动态转发

    - ssh -D <local port> <SSH Server>

Web 安全
--------

零基础如何学习 Web 安全
~~~~~~~~~~~~~~~~~~~~~~~

* http://www.zhihu.com/question/21606800/answer/22268855

Web 服务组件
~~~~~~~~~~~~

8+1：一图胜千言哎:)

.. image:: /download/web_component.png

* 钟馗之眼

  + 网络空间搜索引擎
  + http://www.zoomeye.org
  + 大量样例：http://www.zoomeye.org/search/dork

* 组件具有影响面，越底层的组件影响面可能越大

安全维度
~~~~~~~~

* 漏洞
* 风险
* 事件

Web 安全标准
~~~~~~~~~~~~

* OWASP
* WASC

实战环境
~~~~~~~~

XSS
"""

* ks-xsslab_open

  + 可以上手

    - XSS
    - CSRF
    - ClickJacking

* http://xss-quiz.int21h.jp/

  + 答案：:download:`xss/xss_quiz.txt </download/xss/xss_quiz.txt>`

* http://prompt.ml/0

  + 答案：https://github.com/cure53/XSSChallengeWiki/wiki/prompt.ml

* http://escape.alf.nu/

  + 答案：http://blog.nsfocus.net/alert1-to-win-write-up/

SQL
"""

* https://github.com/Audi-1/sqli-labs

  + SQLI-LABS is a platform to learn SQLI

i春秋
"""""

* http://www.ichunqiu.com/

Sebug + ZoomEye
"""""""""""""""

* http://sebug.net
* http://zoomeye.org
* 你懂得...

工具
~~~~

我的渗透利器
""""""""""""

Firefox
'''''''

* Firebug

  + 调试 JavaScript，HTTP 请求响应观察，Cookie，DOM 树观察等

* Tamper Data

  + 拦截修改

* Live Http Header

  + 重放功能

* Hackbar

  + 编码解码/POST 提交

* Modify Headers

  + 修改头部

* GreaseMonkey

  + Original Cookie Injector for Greasemonkey

* NoScript

  + 进行一些 JavaScript 的阻断

* AutoProxy

  + 翻墙必备

Chrome
''''''

* F12

  + 打开开发者工具，功能 == Firebug + 本地存储观察等

* SwichySharp

  + 翻墙必备

* CookieHacker

  + http://evilcos.me/?p=366

Web 2.0 Hacking
'''''''''''''''

* XSS'OR

  + 常用其中加解密与代码生成
  + http://evilcos.me/lab/xssor/
  + 源码：https://github.com/evilcos/xssor

* XSSEE 3.0 Beta

  + Monyer开发的，加解密最好用神器
  + http://evilcos.me/lab/xssee/

* Online JavaScript beautifier

  + JavaScript美化工具，分析JavaScript常用
  + http://jsbeautifier.org/

* BeEF

  + The Browser Exploitation Framework
  + http://beefproject.com/

HTTP 代理
'''''''''

* Fiddler

  + 非常经典好用的 Web 调试代理工具

* Burp Suite

  + 神器，不仅 HTTP 代理，还有爬虫、漏洞扫描、渗透、爆破等功能

* mitmproxy

  + Python 写的，基于这个框架写神器实在太方便了

漏洞扫描
''''''''

* AWVS

  + 不仅漏扫方便，自带的一些小工具也好用

* Nmap

  + 绝对不仅仅是端口扫描！几百个脚本

* Python 自写脚本/工具

漏洞利用
''''''''

* sqlmap

  + SQL 注入利用最牛神器，没有之一

* Metasploit

  + 最经典的渗透框架

* Hydra

  + 爆破必备

抓包工具
''''''''

* Wireshark

  + 抓包必备

* tcpdump

  + Linux 下命令行抓包，结果可以给 Wireshark 分析

Sebug + ZoomEye
'''''''''''''''

* 类似这类平台都是我们需要的
* Sebug 类似的

  + https://www.exploit-db.com/

* ZoomEye 类似的

  + https://www.shodan.io/

Kali Linux
""""""""""

* 除了上面介绍的一些工具，其他海量各类型黑客工具，自己去摸索

书
~~

* 《黑客攻防技术宝典（Web 实战篇）》
* 《白帽子讲 Web 安全》
* 《Web 前端黑客技术揭秘》

  + 余弦和 xisigr 自己出品

* 《Web之困》
* 《SQL 注入攻击与防御》

Papers
~~~~~~

* http://www.exploit-db.com/papers/
* BlackHat/Defcon/XCon/KCon/国内各安全沙龙等相关 Papers 需要持续跟进

嵌入式安全
----------

路由器安全
~~~~~~~~~~

基础
""""

* 嵌入式 Linux 系统方面知识
* 开发系统互联参考模型——第三层网络层
* MIPS/ARM 汇编知识
* VxWorks 系统方面知识
* JTAG 调试接口规范
* 嵌入式系统交叉环境开发
* 路由器芯片方案提供商

  + 博通
  + Atheros
  + TrendChip
  + ACROSPEED
  + IC+
  + 瑞昱
  + ...

站点
""""

* https://www.openwrt.org/

  + OpenWrt is described as a Linux distribution for embedded devices

* http://routerpwn.com

  + 全球主流路由器相关漏洞大集合

* http://see.sl088.com/wiki/Uboot_%E7%BC%96%E8%AF%91

  + Uboot_编译

* http://www.devttys0.com/

  + Embedded Device Hacking

工具
""""

* Binwalk
* IDA Pro
* gdb/gdbserver
* qemu-system
* qemu-user-static
* Smiasm
* Metasm
* JTAG 硬件调试器

书
""

* 《揭秘家用路由器 0day 漏洞挖掘技术》
* 《Hacking the XBOX: An Introduction to Reverse Engineering》
* 《Hacking the Cable Modem: What Cable Companies Don't Want You to Know》
* 《MIPS 体系结构透视 》
* 《计算机组成与设计：硬件、软件接口》

摄像头安全
~~~~~~~~~~

* http://www.openipcam.com/
* https://media.blackhat.com/us-13/US-13-Heffner-Exploiting-Network-Surveillance-Cameras-Like-A-Hollywood-Hacker-Slides.pdf

工控安全
~~~~~~~~

基础
""""

* 工业生产环境的基本结构，如：SCADA、PCS
* 工业生产环境的信息安全风险点（可参考 DHS 出版物）

  + Improving Industrial Control Systems Cybersecurity with Defense-In-Depth Strategies

* 工控网络组态、逻辑开发、应用组态的基本技术方法
* 抓包、看 RFC 分析几个常规工业以太网协议，如：Profinet、Modbus
* 买两款 PLC 玩玩，会真实感受到工业环境的信息安全问题（一定记得买以太网模块，不贵二手几百块）

站点
""""

事件跟踪分析
''''''''''''

* http://plcscan.org/blog/
* http://scadastrangelove.blogspot.kr
* http://www.phdays.com/
* http://www.scadasl.org
* https://scadahacker.com
* Duqu

  + https://scadahacker.com/resources/duqu.html

* Stuxnet

  + https://scadahacker.com/resources/stuxnet.html

* Havex

  + https://scadahacker.com/resources/havex.html

标准协会/测试工具
'''''''''''''''''

* DHS CET 套件

  + http://ics-cert.us-cert.gov/Assessments

* NERC ES-ISAC

  + http://www.esisac.com/SitePages/Home.aspx

* ICS-ISAC

  + http://ics-isac.org

* NTSB 美国国家工控测试床

  + http://energy.gov/oe/downloads/common-cyber-security-vulnerabilitiesobserved-control-system-assessments-inl-nstb

* NIST SP 800-82

  + http://csrc.nist.gov/publications/nistpubs/800-82/SP800-82-final.pdf

* ISA-99 控制系统安全协会

  + http://isa99.isa.org/ISA99%20Wiki/Home.aspx

* NERC CIP 标准

  + http://www.nerc.com/pa/Stand/Pages/ReliabilityStandards.aspx

工具
""""

仿真类
''''''

* 电力仿真软件 testhaness
* Modbus 仿真软件 ModScan
* 电力 104 协议仿真软件 PMA

测试类
''''''

* Wurldtech Achilles
* Codenomicon Defensics
* Spirent
* BPS

源代码
''''''

* 发现

  + https://code.google.com/p/plcscan/
  + https://code.google.com/p/modscan/
  + https://github.com/arnaudsoullie/scan7
  + https://github.com/atimorin
  + https://github.com/digitalbond/Redpoint

* 操纵

  + https://www.scadaforce.com/modbus
  + https://github.com/bashwork/pymodbus
  + https://rubygems.org/gems/modbus-cli
  + http://libnodave.sourceforge.net
  + https://code.google.com/p/dnp3

* 异常监测

  + http://blog.snort.org/2012/01/snort-292-scada-preprocessors.html
  + http://www.digitalbond.com/tools/quickdraw/

* Fuzz

  + https://github.com/jseidl/peach-pit/blob/master/modbus/modbus.xml

其它
""""

* ZoomEye工控专题： http://ics.zoomeye.org/
* Shodan工控专题：https://www.shodan.io/report/l7VjfVKc
* https://github.com/evilcos/papers/blob/master/网络空间工控设备的发现与入侵.ppt

zoomeye.org
~~~~~~~~~~~

* 全球可以找到无数真实路由器/摄像头/工控设备等
* 如：http://www.zoomeye.org/search?q=app:%22MikroTik%20RouterOS%22&from=dork

研发清单
--------

编码环境
~~~~~~~~

* pip
* Vagrant
* tmux/screen
* Vim
* Markdown
* zsh + oh-my-zsh
* Python2.7
* >Django1.4

  + http://djangobook.py3k.cn/2.0/
  + http://django-debug-toolbar.readthedocs.org/en/latest/

* 其它框架

  + web.py
  + Flask
  + Tornado

* Node.js
* Ubuntu/Gentoo/CentOS
* IPython
* 版本控制

  + 废弃 SVN，全面拥抱 Git
  + GitLab

* Nginx + uWSGI

Python
~~~~~~

* 官方手册

  + 至少过一遍，这都没过一遍，视野会局限
  + 行之说：「我没看过 Python 的书，却熟读官方手册……」

Linux/UNIX
~~~~~~~~~~

* 书

  + 《鸟哥的 Linux 私房菜》
  + 《Linux Shell 脚本攻略》
  + 《UNIX 编程艺术》
  + 《Software Design 中文版 01》、《Software Design 中文版 02》、《Software Design 中文版 03》

* 让你的电脑默认操作系统就是Linux...

前端
~~~~

书
""

* 《JavaScript DOM 编程艺术》

了解 DOM
""""""""

* 这同样是搞好前端安全的必要基础

库
""

* jQuery

  * 优秀的插件应该体验一遍，并做些尝试
  * 官方文档得过一遍

* D3.js
* ECharts

  + 来自百度

* Google API
* ZoomEye Map 组件

  + ZoomEye 团队自己基于开源的打造

* AngularJS

  + Google 出品的颠覆性前端框架

* Bootstrap

  + 应该使用一遍

爬虫进阶
~~~~~~~~

* 代理池

  + 爬虫「稳定」需要

* 网络请求

  + wget/curl
  + urllib2/httplib2/requests
  + Scrapy

* 验证码破解

  + pytesser

调度
~~~~

* crontab 是最原生的定时调度
* 基于 Redis 实现的分布式调度
* 基于 RPyC 实现的分布式调度
* Celery/Gearman 等调度框架

并发
~~~~

* 线程池

  + 进程内优美的并发方案

* 协程

  + 进程内另一种优美的并发方案
  + gevent

* 多进程

  + os.fork
  + multiprocessing

数据结构
~~~~~~~~

* JSON
* cPickle
* protobuf

数据库
~~~~~~

* MySQL
* MongoDB
* Cassandra
* Hadoop 体系
* Redis
* SQLite
* bsddb
* ElasticSearch

大数据处理
~~~~~~~~~~

* Hive
* Spark
* ELK

  + ElasticSearch
  + Logstash
  + Kibana

DevOps
~~~~~~

* SSH 证书
* Fabric
* SaltStack
* Puppet
* pssh/dsh
* 运维进阶

  + 运维工程师必须掌握的基础技能有哪些？
  + http://www.zhihu.com/question/23665108/answer/25299881

调试
~~~~

* pdb
* logging
* Sentry
* strace/ltrace
* lsof
* 性能

  + Python 内

    - timeit
    - cProfile
    - Python性能分析指南：http://www.oschina.net/translate/python-performance-analysis

  + Python 外

    - top/htop/free/iostat/vmstat/ifconfig/iftop...

算法
~~~~

* 分词
* 贝叶斯
* 神经元
* 遗传算法
* 聚类/分类
* ...

持续集成
~~~~~~~~

* 自测试

  + nose

* Jenkins

安全
~~~~

* 我的分享

  + 程序员与黑客：http://www.infoq.com/cn/presentations/programmers-and-hackers

协作
~~~~

* 类似 Trello 的在线协同平台
* Slack
* 微信
* 立会

设计思想
--------

* 人人都是架构师：具备架构思想是一件多酷的事
* 实战出真知
* 如何设计

  + :download:`任务架构设计变迁.pptx </download/arch_design_evolution.pptx>`
  + 松耦合、紧内聚
  + 单元与单元属性
  + 生产者与消费者
  + 结构

    - 队列
    - LRU

  + 分布式

    - 存储
    - 计算

  + 资源考虑

    - CPU
    - 内存
    - 带宽

  + 粗暴美学/暴力美学

    - 大数据，先考虑 run it，然后才能知道规律在哪
    - “run it 优先”能快速打通整体，洞察问题
    - “run it 优先”能摆脱细节（繁枝末节）的束缚
    - “run it 优先”能快速迭代出伟大的 V1

  + 一个字总结

    - 美

优质资源
--------

* 知乎周刊：http://zhuanlan.zhihu.com/Weekly
* 码农周刊：http://weekly.manong.io/
* Pycoder's Weekly：http://pycoders.com/archive/
* Hacker News：https://news.ycombinator.com/
* Startup News：http://news.dbanotes.net/
* 极客头条：http://geek.csdn.net/
* InfoQ：http://www.infoq.com/cn
* Stack Overflow：http://stackoverflow.com/
* GitHub：https://github.com/
* FreeBuf：http://www.freebuf.com/
* WooYun：http://drops.wooyun.org/

牛人 1, 2, 3
------------

* 1 研究：研究东西，有足够洞察力，研究水准不错
* 2 研发：Hack Idea 自己有魄力实现，不懂研发的黑客如同不会游泳的海盗
* 3 工程：研发出来的需要实战、需要工程化，否则只是玩具，而不能成为真的武器
