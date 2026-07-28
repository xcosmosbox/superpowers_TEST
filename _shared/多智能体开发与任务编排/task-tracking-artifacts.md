<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=ecb8907c-acc1-571f-9cbd-d034b5d3a1c2 tag=entity shared=true readonly-meta -->
## 任务跟踪工件
- **归属**：多智能体开发与任务编排 / 任务跟踪与工件管理

**摘要**（可编辑）
用于记录任务状态的Markdown文件、计划文件或检查清单工件，包括TODO.md、Superpowers计划文件和任务artifact。

**详述**（可编辑）
任务跟踪工件包括多种形式：在没有专用任务工具时，可以使用仓库本地的 TODO.md 文件、Superpowers 计划文件或 Markdown 检查清单来跟踪任务状态。旧版文档中引用的 TodoWrite 动作在工具映射中也应视为这类任务跟踪手段。在 Antigravity CLI 中，还有一种特殊的“任务 artifact”，它是一个 Markdown 格式的检查清单文件，通过 write_to_file 工具创建，并设置 IsArtifact: true 和 ArtifactType: "task"。该任务 artifact 作为多步骤任务的单一真实来源，初始时列出所有计划步骤，在步骤完成时通过工具编辑相关行将其标记为完成（例如 - [x]），并在计划变更时同步更新清单。在长时间对话前，应重新阅读任务 artifact 以了解待完成的任务。这些工件共同提供了灵活的任务跟踪方案。
<!-- /kg:uuid=ecb8907c-acc1-571f-9cbd-d034b5d3a1c2 -->

