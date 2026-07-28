<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=e81a356f-a7cf-5687-b523-d0a41e49bf45 tag=concept shared=false readonly-meta -->
## 任务工件概念
- **归属**：任务管理 / 任务跟踪

**摘要**（可编辑）
用于任务跟踪的 Markdown 清单工件。

**详述**（可编辑）
在 Antigravity 中，当技能要求创建待办列表或跟踪任务时，由于没有专门的待办事项工具，需要维护一个任务工件（task artifact）。该工件是一个 Markdown 格式的清单，通过 write_to_file 工具创建，并设置 IsArtifact: true 以及 ArtifactMetadata.ArtifactType: "task"。在任务执行过程中，可以使用 replace_file_content 或 multi_replace_file_content 工具编辑工件内容来标记任务的完成状态。任务工件作为剩余工作的唯一真实来源，必须保持最新状态，并且在对话长度增加时，应该在每一步开始前重新阅读，以确保不遗漏任何事项。
<!-- /kg:uuid=e81a356f-a7cf-5687-b523-d0a41e49bf45 -->

<!-- kg:uuid=d90ff4b9-aefa-57aa-a7c2-b22f3cdd5a95 tag=concept shared=false readonly-meta -->
## 任务跟踪实践
- **归属**：任务管理 / 任务跟踪

**摘要**（可编辑）
多步任务中创建、更新并依赖任务工件清单的流程方法。

**详述**（可编辑）
在多步任务开始时，应首先创建任务工件并列出所有计划步骤。每完成一步，立即编辑工件将该步骤标记为已完成（例如使用 - [x]）。如果计划发生变化，及时更新清单以反映新计划。需要始终保持任务工件的时效性，将其作为剩余工作的唯一真实来源。当对话变长时，在执行每一步之前重新阅读任务工件，确保所有待办事项都被跟踪和完成。
<!-- /kg:uuid=d90ff4b9-aefa-57aa-a7c2-b22f3cdd5a95 -->

<!-- kg:uuid=434e2cf0-7663-5ee2-a03d-9ae25a5151d8 tag=entity shared=false readonly-meta -->
## 后台进程管理工具
- **归属**：任务管理 / 进程管理

**摘要**（可编辑）
管理后台进程的工具，支持查看、终止、状态检查等操作。

**详述**（可编辑）
后台进程管理工具，具体指 Antigravity CLI 中的 `manage_task` 工具。该工具用于管理后台进程，提供 `list`（列出进程）、`kill`（终止进程）、`status`（查看状态）和 `send_input`（发送输入）等操作。注意，该工具并非用于待办事项或清单管理，因此当技能要求创建待办列表时不应使用它。
<!-- /kg:uuid=434e2cf0-7663-5ee2-a03d-9ae25a5151d8 -->

<!-- kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c shared=true mirror=true source=_shared/子代理管理/sub-agent-dispatch-tool.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/子代理管理/sub-agent-dispatch-tool.md` 维护，请勿在此编辑。
> **子代理分派工具** — 在不同平台中用于创建和分派子代理的工具集合。
<!-- /kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c -->

