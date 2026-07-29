<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=da4ba5de-4657-5293-963b-ee7b0155fd19 tag=concept shared=false readonly-meta -->
## Codex应用完成工作流
- **归属**：AI代理增强与技能集成 / 技能映射与环境配置

**摘要**（可编辑）
沙箱环境下引导用户通过原生控件完成推送等工作流

**详述**（可编辑）
当沙箱阻止分支/推送操作（例如在外部管理的工作树中处于分离头状态）时，代理提交所有工作并通知用户使用应用的原生控件：选项包括“Create branch”（命名分支，然后通过应用 UI 提交/推送/PR）或“Hand off to local”（将工作转移到用户的本地检出）。代理仍然可以运行测试、暂存文件，并输出建议的分支名称、提交消息和 PR 描述供用户复制使用。
<!-- /kg:uuid=da4ba5de-4657-5293-963b-ee7b0155fd19 -->

<!-- kg:uuid=13221553-c891-5317-8b3c-b245114bafec tag=entity shared=false readonly-meta -->
## multi_agent配置
- **归属**：AI代理增强与技能集成 / 技能映射与环境配置

**摘要**（可编辑）
启用多代理支持的配置项

**详述**（可编辑）
在 Codex 配置文件 (~/.codex/config.toml) 中添加 [features] multi_agent = true 以启用多代理支持。启用后，spawn_agent、wait_agent 和 close_agent 等工具可用于 dispatching-parallel-agents 和 subagent-driven-development 等技能。
<!-- /kg:uuid=13221553-c891-5317-8b3c-b245114bafec -->

<!-- kg:uuid=dc70fe9e-464e-50f5-9ca5-ab0f9e6a61db tag=concept shared=false readonly-meta -->
## 子代理调度规则
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
管理子代理审查与实现生命周期的一般规则

**详述**（可编辑）
在使用 subagent-driven-development 方法时，审查子代理在完成审查并返回结果后应立即关闭。实现子代理则应保持打开状态，直到其对应任务的审查获得通过；若审查未通过，修复循环将恢复该实现子代理以继续修改。如果运行环境限制导致无法向已生成的代理发送后续消息（即无法恢复现有代理），则应将每个修复轮次作为一个全新的实现子代理进行调度，并提供简要说明、报告文件以及发现的问题，以维持开发流程。
<!-- /kg:uuid=dc70fe9e-464e-50f5-9ca5-ab0f9e6a61db -->

<!-- kg:uuid=1fa7625c-0020-50e0-b311-9881959749b0 tag=concept shared=false readonly-meta -->
## 技能环境检测方法
- **归属**：AI代理增强与技能集成 / 技能映射与环境配置

**摘要**（可编辑）
使用git命令检测分支状态以决策工作流

**详述**（可编辑）
创建 worktree 或完成分支的技能应在操作前使用只读 git 命令检测环境：运行 GIT_DIR=$(cd "$(git rev-parse --git-dir)" 2>/dev/null && pwd -P) 和 GIT_COMMON=$(cd "$(git rev-parse --git-common-dir)" 2>/dev/null && pwd -P) 以及 BRANCH=$(git branch --show-current)。判断逻辑：如果 GIT_DIR != GIT_COMMON，则已处于链接工作树中（应跳过创建）；如果 BRANCH 为空，则处于分离头状态（无法从沙箱分支/推送/PR）。具体使用方式参见 using-git-worktrees 的 Step 0 和 finishing-a-development-branch 的 Step 1。
<!-- /kg:uuid=1fa7625c-0020-50e0-b311-9881959749b0 -->

