<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc tag=concept shared=true readonly-meta -->
## 技能动作映射规则
- **归属**：多智能体开发与任务编排 / 技能动作映射与执行

**摘要**（可编辑）
定义技能语言中的动作如何映射到CLI工具调用，包括通用映射规则和特定于调度子代理、Gemini CLI的映射。

**详述**（可编辑）
技能语言中的抽象动作指令（如“派遣子代理”、“创建待办事项”、“读取文件”等）在运行时会被解析为特定CLI环境下的具体工具调用。在Gemini CLI中，常用动作到工具的映射包括：读取文件 -> read_file，批量读取文件 -> read_many_files，创建新文件 -> write_file，编辑文件 -> replace，运行shell命令 -> run_shell_command，搜索文件内容 -> grep_search，按文件名查找 -> glob，列出目录内容 -> list_directory，获取URL -> web_fetch，网页搜索 -> google_web_search，调用技能 -> activate_skill，派遣子代理 -> invoke_agent（agent_name固定为"generalist"），并行派遣可在同一响应中发起多个invoke_agent调用，任务追踪则通过write_todos工具管理，支持待办(pending)、进行中(in_progress)、已完成(completed)、已取消(cancelled)、已阻塞(blocked)等状态。在Antigravity CLI中，派遣子代理映射为invoke_subagent工具；任务追踪通过任务artifact（如write_to_file等）实现，不使用manage_task。在Pi环境中，若已安装子代理工具（如pi-subagents），则“派遣子代理”动作可使用该工具；否则不应虚构Task调用，而应在当前会话中顺序执行或提示子代理能力未安装。总体上，动作映射遵循结构化、可扩展的规则，确保跨不同CLI工具的技能动作语义一致。
<!-- /kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc -->

