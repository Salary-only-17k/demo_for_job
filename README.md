# demo_for_job  
Demo for job hunting  
## llm demo
全部使用langchain/langgraph实现
### v0.1  
![click video](https://www.bilibili.com/video/BV14ARMYLEsV/?vd_source=8bbf3cb1652e5970bfa9fea339b83ac6)  
**介绍**  
1. 调用的千问大模型api。   
2. 参考coze的调用流方式，实现的代码。通过请求某个工作流，然后在工作流内部请求详细任务。

**功能介绍**  
1. 调用函数
  1.1 查询天气
  1.2 通过用户输入爬去arixv的论文，论文信息保存到xlsx中，有重复的不做写入
  1.3 分析xlsx工作表，把迟到/早退人员上报给人事部；缺少的零件以及价格，包给采购部和财务处，（涉及到多表查询），
  1.4 根据用户的输入，对检测模型结果作分析。
  1.5 模拟触发检测土壤湿度功能，根据时间，季节，作物品种所处生长周期（外部知识库）所需灌水量，土地面积等，分析结果，给出最佳灌溉方式。
