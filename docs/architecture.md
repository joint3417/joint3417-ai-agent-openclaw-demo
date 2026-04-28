# 系统架构说明

## 总览
系统采用多 Agent 协作模式，每个 Agent 专注不同任务，通过 Orchestrator 调度，支持高并发任务处理。

## 模块说明
- **Agent Orchestrator**：任务调度、依赖管理、错误重试。
- **Analysis Agent**：扫描代码、识别技术债、生成优化方案。
- **Execution Agent**：执行重构任务、提交 PR、运行单元测试。
- **Report Agent**：汇总日志、生成报告、可视化展示。

## 技术栈
- OpenClaw: Agent 协作框架
- GPT-4o: 自然语言分析与代码生成
- Python / Node.js: 核心服务与 API
- Redis / PostgreSQL: 数据缓存与存储
