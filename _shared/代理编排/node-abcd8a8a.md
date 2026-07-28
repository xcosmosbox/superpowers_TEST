<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=17698f72-ad9e-5c21-bec0-6375ff13b189 tag=entity shared=true readonly-meta -->
## 子代理工具
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
可选的子代理工具及CLI，来源于pi-subagents包，支持多种执行工作流。

**详述**（可编辑）
子代理工具（Subagent Tool）由可选的 pi-subagents 包提供。它支持多种执行工作流，包括单代理、链式、并行、异步、分叉上下文以及恢复/状态工作流。在 Antigravity CLI 中，invoke_subagent 是调遣子代理的内置工具，对应技能中的“dispatch a subagent”动作，通过 TypeName 参数指定子代理类型（如 'self' 表示全能力工作，'research' 表示只读）。如果环境中没有可用的子代理工具，不应捏造调用，而应在当前会话中顺序执行任务或说明可选子代理能力未安装。
<!-- /kg:uuid=17698f72-ad9e-5c21-bec0-6375ff13b189 -->

