<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=3ff2eeb1-4f02-5e80-a2a2-3e532dae99c4 tag=entity shared=true readonly-meta -->
## 子代理调度工具集
- **归属**：多智能体开发与任务编排 / 子代理调度与生命周期

**摘要**（可编辑）
包含pi-subagents包、subagent工具和invoke_subagent工具，用于派生子代理。

**详述**（可编辑）
Pi核心没有标准子代理工具。pi-subagents包提供subagent工具，支持单代理、链式、并行、异步、分支上下文和恢复/状态等工作流。若未安装该包，不应虚构任务调用，而应对当前会话顺序执行或说明可选能力未安装。在Antigravity CLI中，invoke_subagent工具通过指定TypeName参数（如self或research）派生子代理执行任务。这些工具共同构成子代理调度工具集。
<!-- /kg:uuid=3ff2eeb1-4f02-5e80-a2a2-3e532dae99c4 -->

