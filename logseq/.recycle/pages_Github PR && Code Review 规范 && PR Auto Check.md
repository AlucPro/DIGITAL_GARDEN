### 规范：
* PR 标题 [必须填写JIRA issue号](https://cf.qiniu.io/pages/viewpage.action?pageId=3670256) ，稍微复杂的PR必须有设计稿 
* Code Review必须至少两位成员review过并LGTM才可以被merge。
* PR过于庞大，队友有权拒绝review。
* 对于那些不负责任的reviewer，譬如连续多次没有指出明显有问题的地方，那将被剥夺code review的资格一段时间。
* PR必须严格完成PR Template中的内容[各产品线可选]
* Code Review质量会被考虑到绩效[各负责人根据情况]
* gitlab deploy库必须经过 模块负责人review 确认配置变更无误
- ### 注意
  * *⚠ PR 规范* 必须填写JIRA issue号
  * LGTM = Look Good To Me!
  * LGTM要小心给出，只有你真的觉得代码没问题才可以
  * [WIP] = Work In Process. 看到这个标志表示任务进行中，不需要merge
### 进阶：
* GO语言代码覆盖率PR Travis Auto Coverage Check [需修改.travis.yml]
	* 实现原理与使用姿势： [Go 单元测试覆盖率](https://cf.qiniu.io/pages/viewpage.action?pageId=11666446) 
	* 各产品线覆盖率比对： [https://aone.qiniu.io/reports/coverage](https://aone.qiniu.io/reports/coverage) 
* 七牛GO语言静态检查[自动]
	* 实现原理：  [Go 语言静态检查](https://cf.qiniu.io/pages/viewpage.action?pageId=12487944) 
	* 各产品线检查结果： [https://aone.qiniu.io/reports/goreports](https://aone.qiniu.io/reports/goreports) 
* PR Check Template:建议各组都加上，增强code review的规范性
	* 代码库的根目录新建.github/PULL_REQUEST_TEMPLATE 文件
	* 规范参考： [如何定义github code review模版](https://cf.qiniu.io/pages/viewpage.action?pageId=12488627) 
	* 效果图： [pr效果图.png](https://cf.qiniu.io/download/attachments/1736931/pr%E6%95%88%E6%9E%9C%E5%9B%BE.png?version=1&modificationDate=1479380093000&api=v2)  [review过程图.png](https://cf.qiniu.io/download/attachments/1736931/review%E8%BF%87%E7%A8%8B%E5%9B%BE.png?version=1&modificationDate=1479380103000&api=v2) 
* JIRA issue状态的自动流转，建议各组都配置，以提高工作效率
	* 配置方法见： [jira/github/jenkins集成方案](https://cf.qiniu.io/pages/viewpage.action?pageId=16759731) 
	* 效果可参考项目： [ASLAN](https://jira.qiniu.io/secure/RapidBoard.jspa?rapidView=234&projectKey=ASLAN) 
* gitlab与JIRA 集成
	* 在gitlab的pr里填写JIRA issue号，即可完成gitlab pr 与 JIRA issue的关联
	* 目前适用：deploy／deploy-test库
- ### 规范的库：
  ![09BD9191-4081-4D78-9CDF-04204589D463.png](../assets/09BD9191-4081-4D78-9CDF-04204589D463_1651108928746_0.png) 
  
  
  ￼