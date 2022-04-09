## 海鸥云ERP--开源ERP管理系统
### 项目介绍
#### 开源ERP管理系统，该前后端分离，api使用restful协议，方便二次开发，后端使用Python，Django，DRF等技术，前端代码使用AntD进行构建，包含采购管理，销售管理，库存管理等业务管理流程。
* Gitee地址: [Gitee](https://gitee.com/haioucloud/erp)
* Github地址: [Github](https://github.com/lianzhanshu/oms)
* Demo地址: [Demo](http://114.218.158.78:12222/) &nbsp;&nbsp;公司编号: admin  测试帐号：admin  密码：admin

### 使用前须知
* 软件开放源码(发行协议:GPL-3.0)，用户可免费使用，但禁止任何单位或个人修改软件后再次发行的行为。商业使用需得到我司商业授权。
* 我们欢迎对开源技术感兴趣的朋友一起加入到我们项目中来完善系统功能并为客户提供服务。欢迎扫描下方二维码添加技术交流群，添加时请备注来意

   ![微信群](https://gitee.com/haioucloud/erp/raw/master/raw/%E5%BE%AE%E4%BF%A1%E7%BE%A4.png)
* 功能定制或代理授权咨询：Tel:18761717855或扫描下方二维码联系

   ![微信](https://gitee.com/haioucloud/erp/raw/master/raw/%E5%BE%AE%E4%BF%A1.png)

### 项目背景
#### 目前市面上没有一款采用流行的前后端技术易用开源的ERP系统。有不少朋友也跟我们反应实施了ERP系统但是仍然会面临许多问题，尤其二开的费用高昂。于是我们总结了这些年ERP系统开发的经验，设计了这款开源的海鸥云ERP系统，支持高自由度的开发，来支持企业的自定义需求。我们的代码将持续更新，并且保持与[Demo](http://114.218.158.78:12222/)地址的同步。

### 开发环境
* Python版本为V3.9+
* Django版本为V3.2+
* Django-rest-framework版本为V3.12+
* Vue版本为2.6+
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
3. 迁移数据库
    * python manage.py makemigrations
    * python manage.py migrate
4. 创建用户
    * python manage.py runscript create_user

### 本地运行

1. 启动后端服务
    python manage.py runserver
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

### 业务流程
![业务流程](https://gitee.com/haioucloud/erp/raw/master/raw/ERP%20Workflow.png)

### 管理模块
![管理模块](https://gitee.com/haioucloud/erp/raw/master/raw/ERP%E6%A8%A1%E5%9D%97.png)

### 界面截图
首页
![首页](https://gitee.com/haioucloud/erp/raw/master/raw/%E9%A6%96%E9%A1%B5.png)
报表
![报表](https://gitee.com/haioucloud/erp/raw/master/raw/%E6%8A%A5%E8%A1%A8.png)
产品
![产品](https://gitee.com/haioucloud/erp/raw/master/raw/%E4%BA%A7%E5%93%81.png)
采购
![采购](https://gitee.com/haioucloud/erp/raw/master/raw/%E9%87%87%E8%B4%AD.png)
销售
![销售](https://gitee.com/haioucloud/erp/raw/master/raw/%E9%94%80%E5%94%AE.png)
生产
![生产](https://gitee.com/haioucloud/erp/raw/master/raw/%E7%94%9F%E4%BA%A7.png)
库存
![库存](https://gitee.com/haioucloud/erp/raw/master/raw/%E5%BA%93%E5%AD%98.png)
财务
![财务](https://gitee.com/haioucloud/erp/raw/master/raw/%E8%B4%A2%E5%8A%A1.png)
设置
![设置](https://gitee.com/haioucloud/erp/raw/master/raw/%E8%AE%BE%E7%BD%AE.png)