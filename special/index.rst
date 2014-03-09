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

HTTP抓包与调试
~~~~~~~~~~~~~~

* Firefox插件

  + Firebug/Firecookie

    - 抓包与各种调试

  + Tamper Data

    - 拦截修改

  + Live HTTP Headers

    - 重放功能

  + HackBar

    - 编码解码/POST提交

  + Modify Headers

  + 修改头部

* Fiddler

  + 浏览器代理神器
  + 拦截请求或响应
  + 抓包
  + 重放
  + 模拟请求
  + 编码解码
  + 第三方扩展

    - Watcher

      1. Web前端安全的自动审计工具

* Wireshark

  + 各种强大的过滤器语法

* tcpdump

  + 命令行的类Wireshark抓包神器

* Python

  + urllib2

    - 打开请求响应调试

      1. 编辑urllib2的do_open里的h.set_debuglevel
      2. 改为h.set_debuglevel(1)，这时可以清晰看到请求响应数据，包括HTTPS

什么是跳转
~~~~~~~~~~

服务端跳转
""""""""""

* 302

  + <?php header("Location: 3.php"); ?>

* 301

  + <?php header("HTTP/1.1 301 Moved Permanently"); header("Location: 2.php"); ?>

* u = urllib2.urlopen(url)后，u.url能得到服务端跳转后的地址

  + urllib2自己的特性
  + 所谓的会跟进去

客户端跳转
""""""""""

* <meta http-equiv="refresh" content="0; url=http://www.evilcos.me" />

  + htmlparse解析就行了

* location.href = "http://evilcos.me";

  + 正则（弱），JS引擎（王道）

Python编码规范
~~~~~~~~~~~~~~

编码规范
""""""""

* :download:`PythonCodingRule.pdf </download/PythonCodingRule.pdf>`

入门书
""""""

Python核心编程2

* 第4章 Python对象

  + 完整熟练

* 6.8 Unicode

  + 完整熟练

* 8.11 迭代器和iter()函数

  + 完整熟练

* 第9章 文件的输入和输出

  + 完整熟练

* 第10章 错误和异常

  + 完整熟练

* 第11章 函数和函数式编程

  + 完整熟练

* 第12章 模块

  + 完整熟练

* 第14章 执行环境

  + 完整熟练

* 第15章 正则表达式

  + 完整熟练

* 第18章 多线程编程

  + 完整熟练

* 20.2 使用Python进行Web应用：创建一个简单的Web客户端

  + 完整熟练

Office能力
~~~~~~~~~~

* Word文档编写，看去要专业，尤其对外的
* Excel里面大量的统计、图表功能，需要善于使用
* PPT演讲、培训等必备，如何做好PPT？Google一下...
* 进一步

  + yEd
  + Visio
  + Freemind

    - 本技能表就是这个制作

  + Sphinx

    - 本技能表reStructuredText版本就是这个制作

熟练Vim
~~~~~~~

* 实战至少3回合：http://coolshell.cn/articles/5426.html

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
* :download:`regex/regularexpressions.pptx </download/regex/regularexpressions.pptx>`
* :download:`regex/正则表达式引擎浅析.txt </download/regex/about_regx_engine.txt>`

研发能力
~~~~~~~~

瀑布模型
""""""""

* 需求 -> 需求分析 -> 设计 -> 开发 -> 测试 -> 上线 -> 运维/运营

需求分析能力
""""""""""""

* 给你一个需求，如何给出一个优美的执行思路
* 这个能力非常非常非常的关键

调试能力
""""""""

* 只要定位出，就没有解决不了的Bugs
* 肉眼看到的都是假象

  + 一定要专业的工具与经验配合

* Bugs在哪出现，最终就在哪进行真实模拟调试
* 缩小范围

  + 构建自己的测试样例

    - 排除网络复杂未知情况

  + 关联模块一个个排除
  + Python单步调试

    - import pdb;pdb.set_trace()
    - 在需要单步调试的地方加上面这句，运行程序后中断在此，然后h查看指令进行一步步细细调试

  + 粗暴调试：print

敏捷思想
""""""""

* 快速迭代
* 任务拆细
* v1原则：定义好v1的目标，快速完成v1为优先
* 习惯Wiki记录，利于沉淀与分享

翻墙
~~~~

* http://code.google.com/p/goagent/
* SSH隧道

  + http://www.ibm.com/developerworks/cn/linux/l-cn-sshforward/index.html
  + 本地转发

    - ssh -L <local port>:<remote host>:<remote port> <SSH hostname>

  + 远程转发

    - 反弹
    - ssh -R <local port>:<remote host>:<remote port> <SSH hostname>

  + 动态转发

    - ssh -D <local port> <SSH Server>

Web安全
-------

Web服务组件
~~~~~~~~~~~

8+1：一图胜千言哎:)

.. image:: /download/web_component.png

* 钟馗之眼

  + 网络空间搜索引擎
  + 大数据，懂的人懂，不懂的人不懂
  + http://www.zoomeye.org

* 组件具有影响面，越底层的组件影响面可能越大

安全维度
~~~~~~~~

* 漏洞
* 风险
* 事件

Web安全标准
~~~~~~~~~~~

* OWASP
* WASC
* 我们内部Wiki

实战环境
~~~~~~~~

XSS
"""

* ks-xsslab_open（内部虚拟机）

  + 可以搞通

    - XSS
    - CSRF
    - ClickJacking

* http://xss-quiz.int21h.jp/

  + 答案：:download:`xss/xss_quiz.txt </download/xss/xss_quiz.txt>`

SQL
"""

* https://github.com/Audi-1/sqli-labs

  + SQLI-LABS is a platform to learn SQLI

500多个WSL靶场
""""""""""""""

渗透虚拟机/BT5/Kali
"""""""""""""""""""

* 海量各类型黑客工具

书
~~

* 黑客攻防技术宝典（Web实战篇）
* 白帽子讲Web安全
* Web前端黑客技术揭秘

  + 余弦和xisigr自己出品

* SQL注入攻击与防御

Papers
~~~~~~

* http://www.exploit-db.com/papers/
* blackhat/defcon/国内各安全沙龙等Papers需要持续跟进

研发清单
--------

编码环境
~~~~~~~~

* pip
* Vagrant
* tmux/screen
* Vim
* zsh + oh-my-zsh
* Python2.7
* >Django1.4

  + http://djangobook.py3k.cn/2.0/

* web.py
* node.js
* Ubuntu/Gentoo/CentOS
* IPython
* 版本控制

  + Git/SVN
  + GitLab

* Nginx + uWSGI

Python
~~~~~~

* 官方手册

  + 至少过一遍，这都没过一遍，视野会局限
  + 行之说：「我没看过Python的书，却熟读官方手册……」

Linux
~~~~~

* 书

  + :download:`Bash新手指南.pdf </download/linux/bash_freshman.pdf>`
  + :download:`高级Bash脚本编程.pdf </download/linux/advanced_bash.pdf>`

* :download:`bash快捷操作.txt </download/linux/bash_shortcut.txt>`
* :download:`screen最佳实践.pdf </download/linux/screen.pdf>`
* :download:`crontab格式详解.pdf </download/linux/crontab.pdf>`

前端
~~~~

书
""

* JavaScript DOM编程艺术

了解DOM
"""""""

* 这同样是搞好前端安全的必要基础

库
""

* jQuery

  * 优秀的插件应该体验一遍，并做些尝试
  * 官方文档得过一遍

* ECharts

  + 来自百度

* Google API
* ZoomEye Map组件

  + ZoomEye团队自己基于开源的打造

* AngularJS

  + Google出品的颠覆性前端框架

* Bootstrap

  + 应该使用一遍

爬虫进阶
~~~~~~~~

* 代理池

  + 爬虫「稳定」需要

* 网络请求

  + wget/curl
  + urllib2/httplib2/requests
  + scrapy

* 验证码破解

  + pytesser

调度
~~~~

* crontab是最原生的定时调度
* 基于Redis实现的分布式调度
* 基于RPyC实现的分布式调度
* Celery/Gearman等调度框架

并发
~~~~

* 线程池

  + 进程内优美的并发方案

* 协程

  + 进程内另一种优美的并发方案

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
* Hadoop体系
* Redis
* SQLite
* bsddb

DevOps
~~~~~~

* SSH证书
* Fabric
* SaltStack
* Puppet
* pssh/dsh

调试
~~~~

* pdb
* logging
* Sentry
* strace/ltrace
* lsof
* 性能

  + Python内

    - timeit
    - cProfile
    - Python性能分析指南：http://www.oschina.net/translate/python-performance-analysis

  + Python外

    - top/htop/free/iostat/vmstat/ifconfig/iftop...

算法
~~~~

* 分词
* 贝叶斯

  * :download:`algorithm/贝叶斯.txt </download/algorithm/bayes.txt>`

* 神经元
* 遗传算法
* 聚类/分类
* ...

持续集成
~~~~~~~~

* 自测试

  + nose

* Jenkins

协作
~~~~

* 类似Trello的在线协同平台
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

    - 大数据，先考虑run it（运行之），然后才能知道规律在哪
    - “run it优先”能快速打通整体，洞察问题
    - “run it优先”能摆脱细节（繁枝末节）的束缚
    - “run it优先”能快速迭代出伟大的V1

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

牛人1,2,3
---------

* 1研究：研究东西，有足够洞察力，研究水准不错
* 2研发：hack idea自己有魄力实现，不懂研发的黑客如同不会游泳的海盗
* 3工程：研发出来的需要实战、需要工程化，否则只是玩具，而不能成为真的武器
