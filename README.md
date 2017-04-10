RD_Checklist
============

知道创宇研发技能表

在线阅读：

* Sphinx版本：http://rd.readthedocs.io/
* FreeMind版本：http://blog.knownsec.com/Knownsec_RD_Checklist/

准备
----

* 使用Sphinx编辑，http://sphinx-doc.org/
* 安装：pip install Sphinx
* git clone https://github.com/knownsec/RD_Checklist.git

发布 HTML 格式
--------------

* cd RD_Checklist
* make singlehtml
* cd `_build/singlehtml`
* python -m SimpleHTTPServer
* 浏览器查看

发布 PDF 格式
-------------

* make pdf
