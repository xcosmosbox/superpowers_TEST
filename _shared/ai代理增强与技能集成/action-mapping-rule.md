<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=3935e6c5-9a0f-5c14-aebe-17da8c12f0cb tag=concept shared=true readonly-meta -->
## 动作映射规则
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
定义技能动作如何映射到具体工具调用的规则

**详述**（可编辑）
动作映射规则定义了技能中描述性动作（如“dispatch a subagent”、“create a todo”）如何映射到具体平台上的工具调用。在 Antigravity CLI 上，“dispatch a subagent”映射为 invoke_subagent 工具（通过 TypeName 指定子代理类型），任务跟踪动作则映射为基于文件操作的工件维护流程，使用 write_to_file、replace_file_content 等工具，而非专用的 manage_task 工具。在 Pi 平台上，若安装了可选的 pi-subagents 包，则“dispatch a subagent”映射到其提供的 subagent 工具；对于“create a todo”等任务跟踪动作，优先使用已安装的待办事项或任务工具，若无此类工具，则回退到 Superpowers 计划文件、Markdown 清单或仓库本地 TODO.md 文件进行任务管理。这些规则确保了技能与底层工具的解耦以及跨平台行为一致性。
<!-- /kg:uuid=3935e6c5-9a0f-5c14-aebe-17da8c12f0cb -->

