<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=05888306-652d-5de9-bf77-e4d687f7904b tag=concept shared=false readonly-meta -->
## Codex App完成流程
- **归属**：平台集成 / Git与Codex流程

**摘要**（可编辑）
沙箱环境下代理提交代码并引导用户使用应用完成操作的流程。

**详述**（可编辑）
当代理检测到当前处于一个由 Codex App 外部管理的工作树中，并且处于分离头状态（从而导致无法在沙箱内进行分支、推送等操作）时，将触发 Codex App 完成流程。首先，代理将所有本地改动提交（commit），然后通知用户通过 Codex App 的原生界面控件来完成后续操作。用户面临两种选择：选择 “Create branch” 可通过 App UI 为当前提交命名一个新分支、将其推送到远程仓库并创建 Pull Request，完全在 App 内完成；或者选择 “Hand off to local” 将当前工作状态转移到用户的本地检出环境中，由用户在本地继续操作。在此期间，代理仍然可以在沙箱内运行测试、暂存文件，并输出建议的分支名称、提交消息和 Pull Request 描述，供用户在后续步骤中复制使用。
<!-- /kg:uuid=05888306-652d-5de9-bf77-e4d687f7904b -->

<!-- kg:uuid=7f3b4523-0599-5b70-8ee6-60d2ecd2eda3 tag=concept shared=false readonly-meta -->
## Git环境检测
- **归属**：平台集成 / Git与Codex流程

**摘要**（可编辑）
通过只读 git 命令检测工作目录状态的方法。

**详述**（可编辑）
通过执行一系列只读 git 命令来检测当前工作目录的状态，为后续操作提供决策依据。具体步骤：首先通过 GIT_DIR=$(cd "$(git rev-parse --git-dir)" 2>/dev/null && pwd -P) 获取当前仓库的 .git 目录的绝对路径，同样 GIT_COMMON=$(cd "$(git rev-parse --git-common-dir)" 2>/dev/null && pwd -P) 获取共享的 .git 目录（通常在主工作树中）。若 GIT_DIR 与 GIT_COMMON 不相等，则表明当前已处于一个由 git worktree 创建的链接工作树中，此时应跳过创建工作树的步骤。然后通过 BRANCH=$(git branch --show-current) 获取当前分支名；若 BRANCH 为空，则说明处于分离头状态，在此状态下无法进行分支、推送或创建 PR 等操作。这些检测信号被 using-git-worktrees 流程的 Step 0 和 finishing-a-development-branch 流程的 Step 1 所利用，以决定后续是否创建新的工作树或如何处理分支操作。
<!-- /kg:uuid=7f3b4523-0599-5b70-8ee6-60d2ecd2eda3 -->

<!-- kg:uuid=2a439f3e-3392-5b2d-9fc4-23d9ca1cc7a5 tag=concept shared=false readonly-meta -->
## 多代理配置
- **归属**：子代理管理 / 代理类型

**摘要**（可编辑）
在配置文件中启用多代理支持的特性标志。

**详述**（可编辑）
多代理配置是通过特性标志启用多代理支持的设置。具体方式为：在 ~/.codex/config.toml 文件的 [features] 段中将 multi_agent 设置为 true。启用此配置后，才能使用 spawn_agent、wait_agent、close_agent 等多代理管理工具，并作为执行 dispatching-parallel-agents、subagent-driven-development 等高级技能的前提条件。
<!-- /kg:uuid=2a439f3e-3392-5b2d-9fc4-23d9ca1cc7a5 -->

<!-- kg:uuid=f6a8f8c3-119b-5a9b-89ad-fabcefd66afa tag=entity shared=false readonly-meta -->
## 子代理关闭工具
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
关闭子代理的工具。

**详述**（可编辑）
`close_agent` 用于显式关闭一个子代理，释放资源。在子代理驱动开发（subagent-driven-development）技能中，审查子代理在其审查返回后应立即关闭，因为它的工作已完成；而实现子代理则需要保持打开状态，直到修复循环完成、审查通过后才关闭。
<!-- /kg:uuid=f6a8f8c3-119b-5a9b-89ad-fabcefd66afa -->

<!-- kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c shared=true mirror=true source=_shared/子代理管理/sub-agent-dispatch-tool.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/子代理管理/sub-agent-dispatch-tool.md` 维护，请勿在此编辑。
> **子代理分派工具** — 在不同平台中用于创建和分派子代理的工具集合。
<!-- /kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c -->

<!-- kg:uuid=9869663a-fc81-553f-bb68-11a30327108a tag=entity shared=false readonly-meta -->
## 子代理等待工具
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
等待子代理完成任务的工具。

**详述**（可编辑）
在 Codex 的多代理环境中，`wait_agent` 用于等待之前生成（通过 `spawn_agent`）的子代理完成其分配的任务，以便协调和收集结果。它与 `spawn_agent` 和 `close_agent` 一起构成子代理生命周期的核心接口。
<!-- /kg:uuid=9869663a-fc81-553f-bb68-11a30327108a -->

<!-- kg:uuid=817bef50-27e5-5fc5-b3ab-cf442c80e59f tag=concept shared=false readonly-meta -->
## 子代理调度使用准则
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
在子代理驱动开发中关闭审查代理、保持实现代理及修复循环的指导。

**详述**（可编辑）
在使用子代理驱动开发（subagent-driven-development）时，审查子代理返回审查结果后应立即调用 `close_agent` 关闭；每个实现子代理需要保持打开状态直到其任务的审查通过，因为修复循环会继续使用该实现子代理进行迭代。如果工具不支持向已生成的代理发送另一条消息，则需要将每次修复轮次作为一个全新的实现子代理启动，并附带任务摘要、报告文件和发现；原来的实现子代理随即关闭。
<!-- /kg:uuid=817bef50-27e5-5fc5-b3ab-cf442c80e59f -->

<!-- kg:uuid=e3988be1-41ac-5960-a2bc-b1c860076bb3 shared=true mirror=true source=_shared/子代理管理/predefined-sub-agent-types.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/子代理管理/predefined-sub-agent-types.md` 维护，请勿在此编辑。
> **预定义子代理类型** — 平台内置或特定用途的子代理类型定义。
<!-- /kg:uuid=e3988be1-41ac-5960-a2bc-b1c860076bb3 -->

