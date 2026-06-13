# 项目拷打（DeepResearch）

1. 你这个 DR 项目是要解决什么问题/
   
2. 显式状态管理很火，你是如何进行的？
    
2. 你的 benchmark 是什么？你认为你比 Gemini 的 DR 好在哪？
    
3. 利用 Agent 和传统 LLM 应用的区别是什么？
    
4. 为什么不用 ReAct？
    
5. Agent 系统如何快速定位错误？你是如何定位运行当中的错误？生成的计划、每一步执行有没有问题，你有没有看过？
    
6. 你如何对这个结果进行评测？
    
7. Planner 拆出来的多个 steps，执行时是不是串行的？有没有像多子任务 fan-out / fan-in 那样并行跑？
    
8. 你的多智能体是如何编排的？
    
9. 你是如何编排的，如此编排的优势？
    
10. 这个项目你收获最大的是什么？
    
11. 可靠性方面，如果继续往下做，你会怎么做？
    
12. 有了解过 Deep Agent、RAG Assistant 吗？
    
13. 你的 OCR 技术是怎么做的？
    
14. 表格处理用的什么库？
    
15. Trace 机制做了什么？
    
16. 你怎么测评？baseline 是什么？
    
17. 项目中如何保证大模型输出稳定？
    
18. 你的 State 中设置 message 和 observation 的意义是什么？保存什么？
    
19. 这个项目有没有做上下文工程?
    
20. 项目参考了哪些开源DeepResearch项目？ 自己做了哪些改进？
---
# AI Agent 八股拷打

1. 为什么传统 logging 在 Agent 面前失效？
2. RAG 文档分割的流程是什么？
3. 一个优秀的提示词应该包含什么？
4. LangGraph & LangChain  
	1. 特性
	2. 有哪些组件
	3. LangGraph 的协作方式有哪些
	4. LangGraph 和 Supervisor 的区别
5. MCP 和 Function calling 的区别