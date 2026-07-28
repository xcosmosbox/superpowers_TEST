<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=00bd1faf-9ce8-5480-90d8-c4c9e5834e9a tag=entity shared=false readonly-meta -->
## TODO.md文件
- **归属**：任务管理 / 任务跟踪

**摘要**（可编辑）
用于任务跟踪的仓库本地 Markdown 文件。

**详述**（可编辑）
在 Pi 环境中没有安装 todo/task 扩展时，可以使用仓库本地的 TODO.md 文件进行任务跟踪。这是 Superpowers 任务跟踪替代方案之一，文件内容采用 Markdown 格式，用于记录待办事项及其完成状态，作为轻量级的本地任务清单。
<!-- /kg:uuid=00bd1faf-9ce8-5480-90d8-c4c9e5834e9a -->

<!-- kg:uuid=155c9b89-7374-53b1-bd69-ef81738a1d16 tag=concept shared=false readonly-meta -->
## 任务跟踪替代方案
- **归属**：任务管理 / 任务跟踪

**摘要**（可编辑）
在无专用工具时使用计划文件或检查清单进行任务管理的方法。

**详述**（可编辑）
Pi 核心没有内置的任务列表工具。如果安装了 todo/task 扩展，应优先使用其提供的工具；否则，可以选择 Superpowers 计划文件、Markdown 格式的检查清单或仓库本地的 TODO.md 文件作为任务跟踪的替代手段。旧的 Superpowers 文档中提到的 TodoWrite 功能也对应此处的任务跟踪动作。这些替代方案均以文件为基础，提供轻量级的任务管理能力。
<!-- /kg:uuid=155c9b89-7374-53b1-bd69-ef81738a1d16 -->

<!-- kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c shared=true mirror=true source=_shared/子代理管理/sub-agent-dispatch-tool.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/子代理管理/sub-agent-dispatch-tool.md` 维护，请勿在此编辑。
> **子代理分派工具** — 在不同平台中用于创建和分派子代理的工具集合。
<!-- /kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c -->

<!-- kg:uuid=07a196ef-a6fa-5c3a-9f7d-87bd8acb5cdd tag=concept shared=false readonly-meta -->
## 子代理可用性处理策略
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
当没有子代理工具时应顺序执行而不是虚构调用的策略。

**详述**（可编辑）
Pi 核心不提供标准子代理工具，pi-subagents 包是可选的。若环境中无任何子代理工具，则不能凭空编造 Task 调用；应改为在当前会话中按顺序执行任务，或向用户说明子代理能力未安装，以避免执行错误。这一策略确保了在缺少子代理支持时的优雅降级。
<!-- /kg:uuid=07a196ef-a6fa-5c3a-9f7d-87bd8acb5cdd -->

<!-- kg:uuid=6d047b95-bb2b-5c89-8fac-6e21ed0aeae2 tag=entity shared=false readonly-meta -->
## 子代理支持包
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
Pi 的可选伙伴包，提供 subagent 工具。

**详述**（可编辑）
pi-subagents 包是 Pi 核心的一个强可选伙伴包，为 Pi 提供 subagent 工具。该工具支持单一代理、链式、并行、异步、分叉上下文以及恢复/状态等工作流。当没有安装子代理工具时，不应虚构 Task 调用，而应在当前会话中顺序执行或说明该可选能力未安装。
<!-- /kg:uuid=6d047b95-bb2b-5c89-8fac-6e21ed0aeae2 -->

<!-- kg:uuid=9ba0cbd8-bbed-5712-a021-88535fd398a1 shared=true mirror=true source=_shared/技能系统/skill-action-mapping-rules.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/技能系统/skill-action-mapping-rules.md` 维护，请勿在此编辑。
> **技能动作映射规则** — 定义技能描述的动作如何解析为具体平台工具调用的规则。
<!-- /kg:uuid=9ba0cbd8-bbed-5712-a021-88535fd398a1 -->

