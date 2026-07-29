<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=7c69f017-552a-5625-a62b-71131f53050f tag=concept shared=false readonly-meta -->
## Codex应用完成工作流
- **归属**：对话式AI代理基础设施 / 技能与工作流

**摘要**（可编辑）
沙箱环境下引导用户通过原生控件完成推送等工作流。

**详述**（可编辑）
当沙箱环境阻止分支或推送操作（例如在外部管理的工作树中处于分离头状态）时，代理会提交所有工作并通知用户使用应用的原生控件。用户可以选择“Create branch”（命名分支，然后通过应用 UI 完成提交、推送和 PR 操作）或“Hand off to local”（将工作转移到用户的本地检出）。在此过程中，代理仍然可以运行测试、暂存文件，并输出建议的分支名称、提交消息和 PR 描述，供用户复制使用。
<!-- /kg:uuid=7c69f017-552a-5625-a62b-71131f53050f -->

<!-- kg:uuid=90d2f502-878c-5b88-b781-b822c7e899c6 tag=entity shared=false readonly-meta -->
## multi_agent配置
- **归属**：对话式AI代理基础设施 / 子代理调度

**摘要**（可编辑）
启用多代理支持的配置项。

**详述**（可编辑）
在 Codex 配置文件 (~/.codex/config.toml) 中，通过设置 [features] 下的 multi_agent = true 来启用多代理支持。启用后，spawn_agent、wait_agent、close_agent 等工具可用于 dispatching-parallel-agents 和 subagent-driven-development 等技能。
<!-- /kg:uuid=90d2f502-878c-5b88-b781-b822c7e899c6 -->

<!-- kg:uuid=dc70fe9e-464e-50f5-9ca5-ab0f9e6a61db tag=concept shared=false readonly-meta -->
## 子代理调度规则
- **归属**：对话式AI代理基础设施 / 子代理调度

**摘要**（可编辑）
管理子代理审查与实现生命周期的一般规则。

**详述**（可编辑）
子代理调度规则管理子代理审查与实现生命周期。在使用 subagent-driven-development 方法时，审查子代理在完成审查并返回结果后应立即关闭。实现子代理则应保持打开状态，直到其对应任务的审查获得通过；若审查未通过，修复循环将恢复该实现子代理以继续修改。如果运行环境限制导致无法向已生成的代理发送后续消息（即无法恢复现有代理），则应将每个修复轮次作为一个全新的实现子代理进行调度，并提供简要说明、报告文件以及发现的问题，以维持开发流程。
<!-- /kg:uuid=dc70fe9e-464e-50f5-9ca5-ab0f9e6a61db -->

<!-- kg:uuid=1fa7625c-0020-50e0-b311-9881959749b0 tag=concept shared=false readonly-meta -->
## 技能环境检测方法
- **归属**：对话式AI代理基础设施 / 技能与工作流

**摘要**（可编辑）
使用git命令检测分支状态以决策工作流。

**详述**（可编辑）
在创建 worktree 或完成分支等操作前，技能应使用只读 git 命令检测当前环境。具体命令包括：运行 GIT_DIR=$(cd "$(git rev-parse --git-dir)" 2>/dev/null && pwd -P)、GIT_COMMON=$(cd "$(git rev-parse --git-common-dir)" 2>/dev/null && pwd -P) 以及 BRANCH=$(git branch --show-current)。根据结果判断：如果 GIT_DIR 与 GIT_COMMON 不同，则已处于链接工作树中，此时应跳过创建操作；如果 BRANCH 为空，则处于分离头状态，无法从沙箱中执行分支、推送或 PR 操作。该方法的详细使用可参考 using-git-worktrees 的 Step 0 和 finishing-a-development-branch 的 Step 1。
<!-- /kg:uuid=1fa7625c-0020-50e0-b311-9881959749b0 -->

