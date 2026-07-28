<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=2b329f45-0fae-5627-81ee-b20ac9c7d113 shared=true mirror=true source=_shared/多智能体开发与任务编排/cli-configuration-skill-directory.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/cli-configuration-skill-directory.md` 维护，请勿在此编辑。
> **CLI配置与技能目录** — 包括Antigravity CLI工具、GEMINI.md指令文件以及Gemini和跨运行时技能目录。
<!-- /kg:uuid=2b329f45-0fae-5627-81ee-b20ac9c7d113 -->

<!-- kg:uuid=00320313-3439-562b-b3b4-37c4b7dbdb58 tag=entity shared=false readonly-meta -->
## 任务管理工具集
- **归属**：多智能体开发与任务编排 / 任务跟踪与工件管理

**摘要**（可编辑）
用于创建和编辑任务工件的文件操作工具，包括write_to_file、replace_file_content、multi_replace_file_content和manage_task。

**详述**（可编辑）
任务管理工具集包含一组用于创建和编辑任务工件的文件操作工具。在 Antigravity CLI 中，write_to_file 工具可用于创建任务 artifact，通过设置 IsArtifact: true 和 ArtifactMetadata.ArtifactType: "task" 来保存一个 Markdown 检查清单。replace_file_content 工具用于替换文件内容，可修改已存在的任务 artifact，例如将单个步骤标记为完成。multi_replace_file_content 工具则支持在一次调用中替换文件的多个部分，适用于批量更新任务 artifact 中的多个检查项状态。此外，manage_task 工具虽然出现在工具集中，但它专门用于管理后台进程（提供 list、kill、status、send_input 等操作），并非待办事项清单工具，不可用于任务检查列表的管理。
<!-- /kg:uuid=00320313-3439-562b-b3b4-37c4b7dbdb58 -->

<!-- kg:uuid=ecb8907c-acc1-571f-9cbd-d034b5d3a1c2 shared=true mirror=true source=_shared/多智能体开发与任务编排/task-tracking-artifacts.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/task-tracking-artifacts.md` 维护，请勿在此编辑。
> **任务跟踪工件** — 用于记录任务状态的Markdown文件、计划文件或检查清单工件，包括TODO.md、Superpowers计划文件和任务artifact。
<!-- /kg:uuid=ecb8907c-acc1-571f-9cbd-d034b5d3a1c2 -->

<!-- kg:uuid=9fb5cc39-7d50-5bf8-849e-a1cd87e5386b tag=concept shared=false readonly-meta -->
## 任务跟踪方法
- **归属**：多智能体开发与任务编排 / 任务跟踪与工件管理

**摘要**（可编辑）
使用任务工件追踪多步骤任务的工作流，明确manage_task工具用于后台进程管理而非待办清单。

**详述**（可编辑）
任务跟踪方法的核心是利用任务 artifact 追踪多步骤任务的工作流，同时明确 manage_task 工具的正确用途。由于 Antigravity CLI 没有内置的待办事项工具（manage_task 仅用于管理后台进程，而非检查清单），在技能需要创建待办列表或跟踪任务时，应采用任务 artifact 方法：通过 write_to_file 工具创建一个 Markdown 检查清单文件，并以 artifact 形式保存（设置 IsArtifact: true, ArtifactType: "task"）。该 artifact 作为剩余任务的单一真实来源，开始多步骤任务时需列出所有计划步骤；每完成一个步骤，使用 replace_file_content 或 multi_replace_file_content 编辑文件将其标记为完成（如 - [x]）；如果计划发生变化，及时更新检查清单。在整个过程中，必须始终保持任务 artifact 为最新状态，当对话变长时，应在执行每一步之前重新阅读它，以确保对剩余任务有清晰了解。
<!-- /kg:uuid=9fb5cc39-7d50-5bf8-849e-a1cd87e5386b -->

<!-- kg:uuid=4dd791b7-4826-5e8b-b7d8-45b21cb3d4ae tag=entity shared=false readonly-meta -->
## 子代理类型
- **归属**：多智能体开发与任务编排 / 子代理调度与生命周期

**摘要**（可编辑）
内置子代理类型self（全功能）和research（只读），通过invoke_subagent调用。

**详述**（可编辑）
在Antigravity CLI中，通过invoke_subagent工具可调用两种内置子代理类型：self，具有完整能力，用于执行全功能工作任务；research，只读型子代理，用于研究、检索等只读操作。
<!-- /kg:uuid=4dd791b7-4826-5e8b-b7d8-45b21cb3d4ae -->

<!-- kg:uuid=3ff2eeb1-4f02-5e80-a2a2-3e532dae99c4 shared=true mirror=true source=_shared/多智能体开发与任务编排/sub-agent-scheduling-toolset.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/sub-agent-scheduling-toolset.md` 维护，请勿在此编辑。
> **子代理调度工具集** — 包含pi-subagents包、subagent工具和invoke_subagent工具，用于派生子代理。
<!-- /kg:uuid=3ff2eeb1-4f02-5e80-a2a2-3e532dae99c4 -->

<!-- kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc shared=true mirror=true source=_shared/多智能体开发与任务编排/skill-action-mapping-rules.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/skill-action-mapping-rules.md` 维护，请勿在此编辑。
> **技能动作映射规则** — 定义技能语言中的动作如何映射到CLI工具调用，包括通用映射规则和特定于调度子代理、Gemini CLI的映射。
<!-- /kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc -->

