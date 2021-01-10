# Part 1 
## autotest-基于web的测试管理平台
## 功能模块：
 *   用户系统 <br>
  --已实现：注册登录、菜单权限管理
 *   项目管理
  （对接项目管理平台，根据需求集成常用功能)
 *   环境管理
  （对接运维平台，根据需求集成常用功能)
 *   用例管理  <br>
  --已实现：支持在web平台录入测试用例并提交到后台，实现测试数据的持久化。**便于团队协作、复现历史问题** <br>
  --开发中：http接口支持调试、mock; ui测试任务支持监控; 支持用例批量导入 <br>

## 技术栈：
`python3.7` `flask` `sqlalchemy` `bootstrap`

## 项目结构：
(app/路径下) <br>
* models.py 定义数据库的ORM模型，通过表名把数据库对象映射为一个python类，用这个类实现常用的增删查改 <br>
* views/\*.py 定义视图函数，每个函数处理一个路由。按照菜单分类：user-用户登录及权限管理, case-用例管理 <br>
* templates/\*.html 存放用于前端展示的模板。base.html定义基本布局，其他页面继承base，以base的<main>节点为根节点，渲染页面的个性化组件 <br>

## demo截图展示：
https://pan.baidu.com/s/1hDtngYp2woC3TziMfFdbyg 提取码: fhgt

## 快速部署：
```
git clone git@github.com:akimisen/autotest.git
cd autotest
virtualenv venv
source venv/bin/activate (windows: venv/scripts/activate.bat) 
pip install -r requirements.txt
*  for mac/linux:
  sh build.sh    
*  for windows cmd:
  set FLASK_APP=demo
  flask run
```
访问localhost:5000/login

### 有问题请联系: 
  qq: 124394105(@qq.com) <br>
  vx: akimisen <br>

# Part 2

### 项目包含两个简单的测试脚本：

1. test-http.py  （http接口测试，脚本可以直接运行）
2. test-webui.py 简单实现了基于关键字驱动+数据驱动的自动化测试（还需要稍作调试，大致的逻辑已经梳理好，详见代码注释）<br>

测试平台维护的数据能够和这样的测试脚本实现联动

### 备注：

1. 目前web前端部分采用的技术(只支持jquery)不方便做交互，正在用Vue进行重构。
2. 项目结构较乱，后续会优化
