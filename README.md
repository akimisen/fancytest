# part 1 
##### autotest是基于web的测试管理平台
##### 功能模块：
  1. 用户系统
  --已实现
  2. 项目管理
  （对接公司的项目管理平台，根据需求，集成部分常用功能）
  3. 环境管理
  （对接公司的运维平台，根据需求，集成部分常用功能）
  4. 用例管理 
  
    已实现：支持在web平台根据测试模板（http,web-ui,app-ui等）录入测试用例并提交到后台，实现测试数据的持久化。
    
    便于团队协作，历史问题的复现
 
    开发中：http接口实现在线调试、mock功能; ui测试任务提供任务监控功能; 支持用例批量导入

##### 技术栈：
`python` `flask` `sqlalchemy` `bootstrap`

web平台的实现代码在app\目录下

##### 快速部署：
```
git clone this_repo
cd project_dir
virtualenv venv
pip install -r requirements.txt
for mac/linux:  (仅在mac上做过测试...)
source venv/bin/activate   
sh build.sh     (本地调试模式)
```
##### 有问题请联系: 
  QQ:124394105

# part 2

##### 项目中有两个简单的测试脚本, 代码详见：
1. test-http.py  可以跑起来
2. test-webui.py 简单实现了基于关键字驱动+数据驱动的自动化测试（还跑不起来，需要稍作调试）

测试平台维护的数据能够和这样的测试脚本实现联动

----------------------------------------------
##### 备注：
1. 目前web前端部分因为采用的flask-bootstrap插件不方便做交互，仅实现了增+查，无法实现对数据进行筛选、排序等操作，正在用Vue进行重构，框架已经搭好。
2. 项目结构混乱，后续会优化
3. 各种优化工作预计还需要5~7天
