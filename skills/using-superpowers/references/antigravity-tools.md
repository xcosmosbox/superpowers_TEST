<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=434e2cf0-7663-5ee2-a03d-9ae25a5151d8 tag=entity shared=false readonly-meta -->
## Manage Task CLI工具
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
管理后台进程的 CLI 工具，提供列表、终止、状态查询与发送输入等操作。

**详述**（可编辑）
manage_task 是 Antigravity CLI 中用于管理后台进程的工具，支持 list（列出进程）、kill（终止）、status（查看状态）和 send_input（发送输入）操作。它不是任务清单工具，不应用于任务跟踪。
<!-- /kg:uuid=434e2cf0-7663-5ee2-a03d-9ae25a5151d8 -->

<!-- kg:uuid=fe101a58-4dc4-599d-9e5a-ab40e3c20ce0 tag=concept shared=false readonly-meta -->
## 任务跟踪工件
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
以 Markdown 清单形式保存的任务跟踪约定，用于多步骤任务的管理与更新。

**详述**（可编辑）
任务跟踪工件（task artifact）是 Antigravity 中替代 todo 工具的任务跟踪机制。当 skills 要求创建待办列表或跟踪任务时，通过 write_to_file（设置 IsArtifact: true，ArtifactType: "task"）保存一个 Markdown 清单文件，并可使用 replace_file_content 或 multi_replace_file_content 随时编辑。在多步骤任务开始时，创建列出所有计划步骤的工件；每完成一步，编辑标记为完成（- [x]）；若计划变更，更新清单内容。工件应保持最新，作为剩余步骤的权威来源，在对话变长后需重新阅读以掌握进度。
<!-- /kg:uuid=fe101a58-4dc4-599d-9e5a-ab40e3c20ce0 -->

<!-- kg:uuid=17698f72-ad9e-5c21-bec0-6375ff13b189 shared=true mirror=true source=_shared/代理编排/node-abcd8a8a.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/代理编排/node-abcd8a8a.md` 维护，请勿在此编辑。
> **子代理工具** — 可选的子代理工具及CLI，来源于pi-subagents包，支持多种执行工作流。
<!-- /kg:uuid=17698f72-ad9e-5c21-bec0-6375ff13b189 -->

