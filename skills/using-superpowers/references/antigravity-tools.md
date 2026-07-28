<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=cf7f650a-851a-5303-b396-c27d2bacdd5f tag=entity shared=false readonly-meta -->
## Antigravity CLI
- **归属**：AI代理技能操作 / 工具映射与指令解析

**摘要**（可编辑）
技能动作解析为特定工具的命令行接口。

**详述**（可编辑）
Antigravity CLI (`agy`) is the command-line interface for the Antigravity system. Skills describe actions in natural language (e.g., 'dispatch a subagent', 'create a todo'), and these actions are mapped to the available CLI tools. The mapping table defines how skill requests translate to tools like `invoke_subagent` and `write_to_file`.
<!-- /kg:uuid=cf7f650a-851a-5303-b396-c27d2bacdd5f -->

<!-- kg:uuid=5cc0048f-0e21-5377-af20-d9dbd5b132f0 tag=concept shared=false readonly-meta -->
## manage_task工具用途与限制
- **归属**：AI代理技能操作 / 任务跟踪与流程控制

**摘要**（可编辑）
manage_task工具管理后台进程，不用于任务清单。

**详述**（可编辑）
manage_task 工具专为管理后台进程而设计，支持 list、kill、status 和 send_input 等操作。它明确不是待办列表或清单工具，不应用于任务跟踪。任务跟踪应通过任务工件概念处理。
<!-- /kg:uuid=5cc0048f-0e21-5377-af20-d9dbd5b132f0 -->

<!-- kg:uuid=ef104001-12b5-5cec-a1c6-47d0fae92b68 tag=entity shared=false readonly-meta -->
## write_to_file工具
- **归属**：AI代理技能操作 / 辅助工具与交互

**摘要**（可编辑）
写文件并可创建任务工件，通过设置IsArtifact: true和ArtifactType: 'task'实现。

**详述**（可编辑）
write_to_file 是一个通用文件写入工具。当设置 IsArtifact: true 并提供 ArtifactMetadata.ArtifactType: 'task' 时，它会创建一个任务工件——一个用于跟踪多步骤任务的标记检查清单。这些任务工件后续可以通过 replace_file_content 或 multi_replace_file_content 进行编辑。
<!-- /kg:uuid=ef104001-12b5-5cec-a1c6-47d0fae92b68 -->

<!-- kg:uuid=ba503059-44b1-50f0-a3aa-0b5ff754970b tag=concept shared=false readonly-meta -->
## 任务跟踪工件方法
- **归属**：AI代理技能操作 / 任务跟踪与流程控制

**摘要**（可编辑）
使用Markdown清单工件进行任务跟踪，替代专用待办工具的方法。

**详述**（可编辑）
当技能需要待办列表或任务跟踪时，Antigravity 使用任务工件——一个 Markdown 清单，通过 write_to_file 保存（设置 IsArtifact: true, ArtifactType: 'task'）。在多步骤任务开始时，该工件列出每个计划步骤；随着步骤完成，使用 replace_file_content 或 multi_replace_file_content 将其标记为已完成（- [x]）。如果计划发生变更，也会在工件中更新。该工件作为剩余工作的事实来源，若对话变长，应在执行每一步前重新阅读。
<!-- /kg:uuid=ba503059-44b1-50f0-a3aa-0b5ff754970b -->

<!-- kg:uuid=6af7c6be-2e73-5830-afdf-46dcd95e4404 shared=true mirror=true source=_shared/ai代理技能操作/6af7c6be-2e73-5830-afdf-46dcd95e4404.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理技能操作/6af7c6be-2e73-5830-afdf-46dcd95e4404.md` 维护，请勿在此编辑。
> **子代理调度工具** — 调度子代理的底层工具，如Codex的invoke_subagent和pi-subagents包，支持单个、链式、并行等调度模式。
<!-- /kg:uuid=6af7c6be-2e73-5830-afdf-46dcd95e4404 -->

