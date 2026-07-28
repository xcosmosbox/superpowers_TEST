<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=4bc9b020-f88e-5fd8-902e-38c5fb637a28 tag=concept shared=true readonly-meta -->
## 子代理分派映射
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
将技能动作“Dispatch a subagent”映射到 invoke_agent 工具。

**详述**（可编辑）
当技能请求“Dispatch a subagent”（例如使用通用子代理模板）时，在 Pi 环境中等效于使用已安装的子代理工具（如 pi-subagents 提供的工具）。如果没有子代理工具，不应捏造 Task 调用，而应在当前会话中顺序执行所需工作或说明可选子代理能力未安装。在 Gemini CLI 中，此动作通过 invoke_agent 工具实现，调用时指定 agent_name 为 "generalist" 并传入提示词，同时也支持通过 chat 语法 @generalist 快捷完成。这种映射确保了技能在不同平台上的可移植性。
<!-- /kg:uuid=4bc9b020-f88e-5fd8-902e-38c5fb637a28 -->

