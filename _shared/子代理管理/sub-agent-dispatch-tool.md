<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c tag=entity shared=true readonly-meta -->
## 子代理分派工具
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
在不同平台中用于创建和分派子代理的工具集合。

**详述**（可编辑）
子代理分派工具是在不同平台中用于创建和分派子代理的工具集合。在 Pi 平台上，subagent 工具来自可选的 pi-subagents 包，支持单一代理、链式调用、并行执行、异步处理、分叉上下文以及恢复/状态跟踪等多种工作流模式，用于实现技能动作“Dispatch a subagent”的映射。在 Antigravity CLI (`agy`) 中，该动作解析为 `invoke_subagent` 工具调用，通过内置 `TypeName` 参数指定子代理类型：`self` 用于全能力工作负载，`research` 用于只读操作。在 Codex 中，启用 `multi_agent = true` 后，`spawn_agent` 可用，用于派生出新的子代理来并行或独立处理任务，在 dispatching-parallel-agents 和 subagent-driven-development 等技能中使用。在 Gemini CLI 中，则是通过 `invoke_agent` 工具调用，接受 `agent_name` 和 `prompt` 参数，通用目的子代理分派使用 `agent_name: "generalist"`，并支持聊天快捷语法 `@generalist <prompt>`，且可并行分派多个 `invoke_agent` 调用。
<!-- /kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c -->

