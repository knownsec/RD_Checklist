专业技能
========

..
  Show Source? 别看了，加入我们吧 ;-)
  http://blog.knownsec.com/2012/02/knownsec-recruitment/

**基础必备**
------------

人品第一
^^^^^^^^

HTTP抓包与调试
^^^^^^^^^^^^^^

* Firefox插件

  * Firebug/Firecookie

    * 抓包与各种调试
  * Tamper Data

    * 拦截修改
  * Live HTTP Headers

    * 重放功能
  * HackBar

    * 编码解码/POST提交
  * Modify Headers

   * 修改头部
* Fiddler

  * 浏览器代理神器
  * 拦截请求或响应
  * 抓包
  * 重放
  * 模拟请求
  * 编码解码
  * 第三方扩展

    * Watcher

      * Web前端安全的自动审计工具
* Wireshark

  * 各种强大的过滤器语法
* tcpdump

  * 命令行的类Wireshark抓包神器
* Python

  * urllib2

    * 打开请求响应调试

      * 编辑urllib2的do_open里的h.set_debuglevel
      * 改为h.set_debuglevel(1)，这时可以清晰看到请求响应数据，包括HTTPS

什么是跳转
^^^^^^^^^^

* 服务端跳转

  * 302

    * <?php header("Location: 3.php"); ?>
  * 301

    * <?php header("HTTP/1.1 301 Moved Permanently"); header("Location: 2.php"); ?>
  * u = urllib2.urlopen(url)后，u.url能得到服务端跳转后的地址

    * urllib2自己的特性
    * 所谓的会跟进去
* 客户端跳转

  * <meta http-equiv="refresh" content="0; url=http://www.evilcos.me" />

    * htmlparse解析就行了
  * location.href = "http://evilcos.me";

    * 正则（弱），JS引擎（王道）

Python编码规范
^^^^^^^^^^^^^^

<PythonCodingRule.pdf>

Office能力
^^^^^^^^^^

* Word文档编写，看去要专业，尤其对外的
* Excel里面大量的统计、图表功能，需要善于使用
* PPT演讲、培训等必备，如何做好PPT？百度一下...
* **进一步**

  * yEd
  * Visio
  * Freemind

熟练VIM
^^^^^^^

* 实战至少3回合：http://coolshell.cn/articles/5426.html

算法
^^^^

* 快排
* 二分

正则表达式
^^^^^^^^^^

* 调试工具

  * **Kodos**
  * **RegexBuddy**

    * 支持多种语言
    * 支持调试优化
  * **http://www.regexper.com/**

    * 正则图解
* http://wiki.ubuntu.org.cn/Python正则表达式操作指南
* <regex/regularexpressions.pptx>
* regex/正则表达式引擎浅析.txt <regex/about_regx_engine.txt>

研发能力
^^^^^^^^

* 瀑布模型

  * 需求 -> 需求分析 -> 设计 -> 开发 -> 测试 -> 上线 -> 运维/运营
* **需求分析能力**

  * 给你一个需求，如何给出一个优美的执行思路
  * 这个能力非常非常非常的关键
* 调试能力

  * 只要定位出，就没有解决不了的Bugs
  * 肉眼看到的都是假象

    * 一定要专业的工具与经验配合
  * Bugs在哪出现，最终就在哪进行真实模拟调试
  * 缩小范围

    * 构建自己的测试样例

      * 排除网络复杂未知情况
    * 关联模块一个个排除
    * Python单步调试

      * import pdb;pdb.set_trace()
      * 在需要单步调试的地方加上面这句，运行程序后中断在此，然后h查看指令进行一步步细细调试
    * 粗暴调试：print
* 敏捷思想

  * 快速迭代
  * 任务拆细
  * 定义好V1的目标，快速完成V1为优先
  * 习惯Wiki记录，利于沉淀与分享

翻墙
^^^^

* http://code.google.com/p/goagent/
* SSH隧道

  * http://www.ibm.com/developerworks/cn/linux/l-cn-sshforward/index.html
  * 本地转发

    * ssh -L <local port>:<remote host>:<remote port> <SSH hostname>
  * 远程转发

    * 反弹
    * ssh -R <local port>:<remote host>:<remote port> <SSH hostname>
  * 动态转发

    * ssh -D <local port> <SSH Server>

kscomm
^^^^^^

* 知道创宇的公共模块，精华
* threadpool
* spider
* charsetck
* redirectck
* ...

**原则**
--------

* 至少完整看完与练习好一本书
* 至少过一遍官方文档

Python
------

* 书

  * Python核心编程2

    * 第4章 Python对象

      * 完整熟练
    * 6.8 Unicode

      * 完整熟练
    * 8.11 迭代器和iter()函数

      * 完整熟练
    * 第9章 文件的输入和输出

      * 完整熟练
    * 第10章 错误和异常

      * 完整熟练
    * 第11章 函数和函数式编程

      * 完整熟练
    * 第12章 模块

      * 完整熟练
    * 第14章 执行环境

      * 完整熟练
    * 第15章 正则表达式

      * **完整熟练**
    * 第18章 多线程编程

      * 完整熟练
    * 20.2 使用Python进行Web应用：创建一个简单的Web客户端

      * 完整熟练
  * 可爱的Python

    * 抽空品味下鸡汤是个不错的选择
* 官方手册

  * 至少过一遍，这都没过一遍，视野会局限

Linux
-----

.. TODO 资源文件

* 书

  * Bash新手指南.pdf <linux/bash_freshman.pdf>
  * 高级Bash脚本编程.pdf <linux/advanced_bash.pdf>
* bash快捷操作.txt <linux/bash_shortcut.txt>
* screen最佳实践.pdf <linux/screen.pdf>
* crontab格式详解.pdf <linux/crontab.pdf>

前端
----

* 书

  * JavaScript DOM编程艺术
* 了解DOM

  * 这同样是搞好前端安全的必要基础
* 库

  * jQuery

    * 优秀的插件应该体验一遍，并做些尝试
    * 官方文档得过一遍
  * Bootstrap

    * 应该使用一遍
  * Django

    * http://djangobook.py3k.cn/2.0/

Web安全
-------

.. TODO 资源文件

WebApp分层
^^^^^^^^^^

* 第三方内容

  * 如：CNZZ, Google Ad, Mashup等
* 前端框架

  * 插件体系
  * 如：jQuery, Bootstrap等
* 应用本身

  * 插件体系
  * 如：Discuz!, WordPress, Trac等
* 开发框架

  * 插件体系
  * 如：ThinkPHP, Django, Rails等
* 支撑层

  * CGI语言
  * Web容器
  * 操作系统
* Web应用安全结构.pptx <webapp_sec_structure.pptx>

安全维度
^^^^^^^^

* 漏洞
* 风险
* 事件

Web安全标准
^^^^^^^^^^^

* OWASP
* WASC
* 我们内部Wiki

实战环境
^^^^^^^^

* XSS

  * ks-xsslab_open（内部虚拟机）

    * 可以搞通

      * XSS
      * CSRF
      * ClickJacking
  * http://xss-quiz.int21h.jp/

    * 答案：xss/xss_quiz.txt <xss/xss_quiz.txt>
* SQL

  * https://github.com/Audi-1/sqli-labs

    * SQLI-LABS is a platform to learn SQLI
* 100多个WSL靶场

  * 渗透虚拟机/BT5/Kali

    * 海量各类型黑客工具

书
^^^^

* 黑客攻防技术宝典（Web实战篇）
* 白帽子讲Web安全
* Web前端黑客技术揭秘
* SQL注入攻击与防御

Papers
^^^^^^

* http://www.exploit-db.com/papers/
* blackhat/defcon/国内各安全沙龙等Papers需要持续跟进

设计思想
--------

.. TODO 资源文件

* 人人都是架构师——我还是一贯的想法 ;-)
* 实战出真知
* 如何设计

  * 任务架构设计变迁.pptx <arch_design_evolution.pptx>
  * 松耦合、紧内聚
  * 单元与单元属性
  * 生产者与消费者
  * 结构

    * 队列
    * LRU
  * 分布式

    * 存储
    * 计算
  * 资源考虑

    * CPU
    * 内存
    * 带宽
  * 粗暴美学/暴力美学

    * 大数据，先考虑run it（运行之），然后才能知道规律在哪
    * “run it优先”能快速打通整体，洞察问题
    * “run it优先”能摆脱细节（繁枝末节）的束缚
    * “run it优先”能快速迭代出伟大的V1
  * 一个字总结

    * 美
* 核心存储与计算

  * MySQL
  * MongoDB
  * Cassandra
  * Hadoop体系
  * Redis
  * Memcached
  * RabbitMQ
  * Celery
  * Gearman

算法
----

.. TODO 资源文件

* 分词
* 贝叶斯

  * algorithm/贝叶斯.txt <algorithm/bayes.txt>
* 神经元
* 遗传算法
* ...
