<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 tag=entity shared=true readonly-meta -->
## 子代理调度工具
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
用于调度子代理执行任务的工具，涵盖多种实现和变体

**详述**（可编辑）
子代理调度工具是用于将子代理任务派发到不同运行时环境执行的核心工具，具有多种平台变体。在 Antigravity CLI 中，该工具为 invoke_subagent，接受内置 TypeName 参数，例如 'self' 表示全能力工作子代理，'research' 表示只读研究子代理。在 Gemini CLI 中，对应工具为 invoke_agent，使用 agent_name: 'generalist' 调度通用子代理，并支持通过 @generalist 聊天语法快捷调用，可在同一响应中多次调用以实现并行执行。在 Pi 平台上，若安装了可选的 pi-subagents 包，则提供 subagent 工具，支持单代理任务、链式工作流、并行执行、异步操作、分叉上下文处理以及恢复/状态监控等高级功能。这些工具在各自平台上实现了技能中“dispatch a subagent”动作的具体解析与执行。
<!-- /kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 -->

