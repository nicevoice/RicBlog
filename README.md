RicBlog
=======

##吐槽
比较奇葩的一个地方是为毛后台密码在程序里数据库就存一个session！
唔，需要的包如下

    web.py
    - MySQLDb (web.py需要)
    Jinja2
    markdown

写作方式就是markdown写作。RSS那里我不是很熟所以貌似写的很烂。
实际上写的都很烂....QAQ，大牛勿喷...
膜拜<a href="http://github.com/whtsky">whtsky</a>大神！
前端后端都是我自己来的..所以貌似整体都很烂..
啊，sad story

##Introduction
This is a lightweight blog system.   
It is written in Python.   
It is beautiful and elegant.   

    Version  : 0.1.1 - 2013/10/21
    Author   : Ricter (@RicterZ)
    Website  : http://www.ricter.info
    E-mail   : RicterZheng@gmail.com
    Frame: Jinja2, Web.py, Bootstrap, Markdown

RicBlog是一个轻量级博客系统。   
它是由Python编写的。   
它是美丽并且优雅的。   
为了最简洁，它尽量少用try...except   
为了最简洁，它把所有错误处理交给系统   

    DataBase : MySQL
    Python   : Python2
    Other: uwsgi(not necessary)
    Setting  :

###Template path

    eg.templates_path = 'templates'
    MySQL DataBase
    eg.MySQL_host       = 'www.ricter.info'
       MySQL_user       = 'root'
       MySQL_pass       = '123456'
       MySQL_DB         = 'myblog'
       MySQL_blog_table = 'blog'
       MySQL_user_table = 'user'

###Blog Title

    eg.default_title = ' | RicterZ's Blog | Welcome!'
    PS:#这里出现错误的时候就是奇葩中文编码的错误，把decode改成gbk试试

###Blog Manager

    eg.blog_bacground_user = 'admin'
       blog_bacground_pass = 'admin'

###MySQL DataBase Structure

    - blog
    -------------
    id         int ,   A_I
    title      text, gb2312_chinese_ci
    time       text, gb2312_chinese_ci
    content    text, gb2312_chinese_ci
    lookcount  int


    - session
    -------------
    session    text, gb2312_chinese_ci

