# wku_drf_web

WKU Learning Resource Sharing Platform

本项目使用Django Rest Framework + SQLite + Vue.js + Element UI 组件库

### 参考文档

Django 官方文档

https://www.djangoproject.com/

Django Rest Framework 文档

https://www.django-rest-framework.org/

Vue3.js 文档

https://cn.vuejs.org/

Element UI 框架 文档

https://element-plus.org/zh-CN/

### 如何使用本项目

本项目在虚拟环境下开发，虚拟环境已上传至 venv/ 目录下

如何进入虚拟环境

假设将项目clone至本地 D:\GitHub\ 目录下

在CMD中输入

cd D:\GitHub\wku_drf_web\

进入项目目录，输入  
venv\Scripts\activate

进入虚拟环境

如何运行服务器

进入Django项目根目录

cd D:\GitHub\wku_drf_web\wku_textbook

输入运行服务器

python manage.py runserver

![]([.\python%20manage.py%20runserver.png](https://github.com/UnknownCloud1024/wku_drf_web/blob/main/python%20manage.py%20runserver.png))

### 已完成的部分

#### Django APP 模块

1. Article 文章相关功能（增删改查）

2. Comment 评论相关功能 （增删改查）

3. Textbook 教科书，教学大纲，学习资料的上传管理，以及下载

4. User_info 用户管理功能（使用 Django Rest Framework 自带的用户管理功能，详情见 Django Rest Framework 文档）

注：

APP目录结构

admin.py - 在这里注册Model

model.py 模型文件

permission.py 权限文件

serializers.py 序列化器

view.py 视图文件

test.py 测试文件

**当对模型有改动时，输入以下指令，完成对数据库的迁移**

python manage.py makemigrations  
python manage.py migrate

#### Django 后台管理界面

如何进入后台管理

启动服务器后，在浏览器中输入

http://127.0.0.1:8000/admin/

进入后台登录界面

用户名：Cloud

密码：HatsuneMiku39

即可登入后台管理界面

![](.\back%20ui.png)

#### API

运行服务器后，输入

http://127.0.0.1:8000/api/

进入后台接口界面

![](.\api.png)

具体例子，如api需要修改请修改对应的序列化器和视图文件

![](.\api%20example.png)

### 未完成的部分

### 前台界面

./wku_textbook/frontend 为前端资源目录

已安装Vue3.js 和 Element UI 组件库，如果希望更换其他前端框架，可直接将本目录删除

### 飞跃手册分享功能

目前解决方案有两种

1. 完成项目中 APP guide 模块，实现飞跃手册的线上上传分享，简而言之，就是提供一个表单功能，供用户填写自己的申请心得。具体表单内容可参考往年飞跃手册以及一亩三分地网站的分享。（比如，申请者的三维，科研 / 项目背景，申请策略，四年计划安排，语言考试心得等等）

2. 简单的方法，将其与 APP textbook 模块合并，即仅提供飞跃手册（pdf版）的上传和下载，此方法无需 APP guide 模块，可直接删除
