<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=5c73e6dc-f6d5-572e-982c-174e020e9cf3 tag=concept shared=true readonly-meta -->
## 任务跟踪映射
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
将技能任务跟踪动作映射到 write_todos 工具。

**详述**（可编辑）
对于任务跟踪动作（如“创建一个待办事项”或“标记完成”），在 Pi 环境中等价的做法是使用已安装的待办/任务工具（如果可用）。如果没有安装此类工具，则可以在 Superpowers 计划文件、Markdown 中的清单或存储库本地的 TODO.md 中跟踪任务。较旧的 Superpowers 文档可能会提到“TodoWrite”，应将其视为与此处描述的任务跟踪操作相同。在 Gemini CLI 上，技能中创建或标记待办事项的请求通过 write_todos 工具处理，支持多种状态：pending（待处理）、in_progress（进行中）、completed（已完成）、cancelled（已取消）、blocked（被阻塞）。
<!-- /kg:uuid=5c73e6dc-f6d5-572e-982c-174e020e9cf3 -->

