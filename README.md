RD_Checklist
============

知道创宇研发技能表

在线阅读：

* Sphinx版本：http://rd.readthedocs.org/
* FreeMind版本：http://blog.knownsec.com/Knownsec_RD_Checklist/v2.2.html

准备
----

* 使用Sphinx编辑，http://sphinx-doc.org/
* 安装：pip install Sphinx
* git clone https://github.com/knownsec/RD_Checklist.git

发布HTML格式
------------

* cd RD_Checklist
* make singlehtml
* cd _build/html
* python -m SimpleHTTPServer
* 浏览器查看

发布PDF格式
-----------

* make pdf
