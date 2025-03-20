## 语言/Language

- [中文](#中文)
- [English](#english)

## 中文
## 盒木ERP社区版--开源ERP进销存管理系统
### 协议
#### 本项目采用GPL-3.0协议，您可以免费使用本项目，商业用途请联系我们。

### 项目介绍
#### 该系统前后端分离，api使用restful协议，方便二次开发，后端使用Python，Django，DRF等技术，前端代码使用AntD进行构建，包含采购管理，销售管理，库存管理等业务管理流程。移动端使用Uniapp，包含产品标签打印，出入库扫码等功能。

* Github地址: [Github](https://github.com/lsjt5858/HimoolERP)

### 项目背景
#### 目前市面上没有一款采用流行的前后端技术易用开源的ERP系统。有不少朋友也跟我们反应实施了ERP系统但是仍然会面临许多问题，尤其二开的费用高昂。于是我们总结了这些年ERP系统开发的经验，设计了这款开源的盒木ERP系统，支持高自由度的开发，来支持企业的自定义需求。

### 硬件要求及开发环境
* 移动端打印功能需指定型号PDA，请联系作者购买
* Python版本为V3.9+
* Django版本为V3.2+
* Django-rest-framework版本为V3.12+
* Vue版本为2.6+
* PDA端使用Uniapp
* 数据库为MySQL
* 前端组件为AntD
* 其他Python包可参考requirements.txt文件

### 搭建运行环境

* pip install -r requirements.txt
* cd frontend  #进入frontend文件夹
* npm install -g @vue/cli  #安装vue脚手架
* npm install  #安装依赖包

### 配置 MySQL

1. 数据库字符集设置为 utf8mb4
2. 创建 erp-db 数据库(先设置字符集, 再创建数据库)
    CREATE DATABASE erp_db;
3. 创建配置文件
    * python tools/create_configs.py
4. 迁移数据库
    * python manage.py makemigrations
    * python manage.py migrate
5. 创建用户
    * python manage.py runscript create_user

### 本地运行

1. 启动后端服务
    python3 manage.py runserver
2. 启动前端服务
    npm run serve
3. 浏览器访问前端地址

### 服务器运行

1. 配置 uwsgi
    pip install uwsgi
2. 运行 uwsgi
    uwsgi --ini [项目路径]/configs/uwsgi.ini
3. 配置 nginx(配置文件在 /configs/nginx)
4. 构建前端文件
    进入 frontend 目录, npm run build
