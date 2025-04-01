# demo_for_job  
Demo for job hunting  
## llm demo
全部使用langchain/langgraph实现。实现了一个框架。
### v0.1  
![click video](https://www.bilibili.com/video/BV14ARMYLEsV/?vd_source=8bbf3cb1652e5970bfa9fea339b83ac6)  
**介绍**  
1. 调用的千问大模型api。   
2. 参考coze的调用流方式，实现的代码。通过请求某个工作流，然后在工作流内部请求详细任务。

**功能介绍**  
1. 调用函数
  1.1 查询天气。  
  1.2 通过用户输入爬去arixv的论文，论文信息保存到xlsx中，有重复的不做写入。  
  1.3 分析xlsx工作表，把迟到/早退人员上报给人事部；缺少的零件以及价格，包给采购部和财务处，（涉及到多表查询），  
  1.4 根据用户的输入，对检测模型结果作分析。  
  1.5 模拟触发检测土壤湿度功能，根据时间，季节，天气，作物品种所处生长周期（外部知识库）所需灌水量，土地面积等，分析结果，给出最佳灌溉方式。
2. chat  增加了长记忆功能
  2.1 角色为农业专家，外部数据库有10种作物（使用了rag技术），每种作物知识包括：生长周期内需要化肥介绍，灌水量介绍，（辽宁地区）适合种植时间。
  2.2 根据用户的输入，查询表格，写入xlsx，分析表格功能。  
### v0.2
![click_video](https://www.bilibili.com/video/BV1WXQGY2EbC/?vd_source=8bbf3cb1652e5970bfa9fea339b83ac6)   
**介绍**   
对v0.1优化。  

**功能介绍**    
参考了manus的一些思路，作了感知处理，去掉先启动工作流，再去执行任务的功能。 
### v0.3
开发中
**介绍**   
优化长记忆，优化rag。

**功能介绍**    
1. rag部分接入flashrag，在改flashrag，让其支持langchain接口。
2. 把记忆做成rag检索的模式。

### v0.3.1
![click_video](https://www.bilibili.com/video/BV1Z3ZFYmEFj/?vd_source=8bbf3cb1652e5970bfa9fea339b83ac6)

**介绍**   
为了应对面试，花了一天时间写的demo。主要工作为rag优化。还有优化地方。

**功能介绍**    
1. rag优化
2. 33篇文章，长的有81页，短的有1页。
3. 有噪声数据，文章有很多方面，有使用手册，农业知识，客服聊天记录，工作表格，项目计划书，项目手册。
4. 根据用户需要查询的内容，返回结果。
5. 调用的本地embedding、chat和rand模型，chat为7b的小模型，解析有时候不准。
