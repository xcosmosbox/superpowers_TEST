<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=44081383-217a-5148-b092-1a1ff3e222ed tag=entity shared=false readonly-meta -->
## manage_task工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
管理后台进程（列表、终止、状态查询等）

**详述**（可编辑）
在 Antigravity CLI 中，`manage_task` 是一个进程管理工具，用于管理后台进程，支持的操作包括 list（列表）、kill（终止）、status（状态）和 send_input（发送输入）。该工具专为进程控制设计，不应被误用于任务跟踪场景，如创建待办事项或标记完成等。
<!-- /kg:uuid=44081383-217a-5148-b092-1a1ff3e222ed -->

<!-- kg:uuid=d68cbb4c-e24d-5f68-952c-95d0e579e112 tag=concept shared=false readonly-meta -->
## 任务工件
- **归属**：AI代理增强与技能集成 / 任务追踪与组织

**摘要**（可编辑）
以Markdown清单形式存在的任务跟踪核心工件

**详述**（可编辑）
在 Antigravity 中，由于没有专用的待办事项工具，任务跟踪通过维护任务工件（task artifact）来实现。该工件是一个使用 write_to_file 保存的 Markdown 清单，创建时需设置 IsArtifact: true 且 ArtifactMetadata.ArtifactType 为 "task"，后续可通过 replace_file_content 或 multi_replace_file_content 进行编辑。在执行多步骤任务前，应先创建一份列出所有步骤的计划工件；每完成一步，编辑工件将其标记为完成（- [x]）。若计划发生变更，需实时更新清单，使其始终作为当前剩余工作的唯一真实来源。当对话变得较长时，应在执行每一步前重新读取该工件，以保持状态同步。
<!-- /kg:uuid=d68cbb4c-e24d-5f68-952c-95d0e579e112 -->

<!-- kg:uuid=3935e6c5-9a0f-5c14-aebe-17da8c12f0cb shared=true mirror=true source=_shared/ai代理增强与技能集成/action-mapping-rule.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理增强与技能集成/action-mapping-rule.md` 维护，请勿在此编辑。
> **动作映射规则** — 定义技能动作如何映射到具体工具调用的规则
<!-- /kg:uuid=3935e6c5-9a0f-5c14-aebe-17da8c12f0cb -->

<!-- kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 shared=true mirror=true source=_shared/ai代理增强与技能集成/sub-agent-scheduling-tool.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理增强与技能集成/sub-agent-scheduling-tool.md` 维护，请勿在此编辑。
> **子代理调度工具** — 用于调度子代理执行任务的工具，涵盖多种实现和变体
<!-- /kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 -->

