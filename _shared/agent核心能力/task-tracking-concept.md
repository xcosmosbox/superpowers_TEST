<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=98c0729d-8a5a-5d7d-bbed-f6e3f8a8ceac tag=concept shared=true readonly-meta -->
## 任务追踪概念
- **归属**：Agent核心能力 / 任务管理

**摘要**（可编辑）
包含任务工件和任务追踪器工具集在内的任务跟踪核心概念。

**详述**（可编辑）
任务追踪的核心概念包括任务工件（task artifact）和任务追踪器工具集。在 Antigravity 中，任务工件的实现是通过 write_to_file 保存的 Markdown 清单，创建时需设置 IsArtifact: true 且 ArtifactMetadata.ArtifactType 为 "task"，后续可通过 replace_file_content 或 multi_replace_file_content 进行编辑。在多步骤任务前，应先创建计划工件列出所有步骤，每完成一步编辑工件标记为完成（- [x]）；若计划变更需实时更新，使其作为当前剩余工作的唯一真实来源；对话较长时，应在执行每一步前重新读取该工件以保持状态同步。Gemini CLI 则提供了一套丰富的任务追踪器工具集，包括 tracker_create_task（创建任务）、tracker_update_task（更新任务）、tracker_get_task（获取任务详情）、tracker_list_tasks（列出所有任务）、tracker_add_dependency（添加任务依赖）和 tracker_visualize（可视化任务关系），支持完整的任务生命周期管理，能够创建和更新任务状态，建立依赖关系，并以可视化方式展示任务进展和结构，用于高效组织与追踪复杂任务。
<!-- /kg:uuid=98c0729d-8a5a-5d7d-bbed-f6e3f8a8ceac -->

