<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=de2730e4-7183-512e-ad1c-a26a0b22f1a8 tag=concept shared=false readonly-meta -->
## Codex应用完成流程
- **归属**：AI代理技能操作 / 环境配置与初始化

**摘要**（可编辑）
当沙箱阻塞分支/推送操作时，代理提交所有工作并指导用户使用应用原生控件完成。

**详述**（可编辑）
当沙箱环境阻止分支或推送操作时（例如在外部管理的worktree中出现分离HEAD的情况），代理会提交所有工作并通知用户使用Codex应用的原生控件来完成后续步骤。具体提供两种选项：一是“创建分支”——由代理提供分支名称，然后用户在应用UI中完成提交、推送及创建PR；二是“移交到本地”——将工作成果转移至用户的本地检出中。在此期间，代理仍可运行测试、暂存文件，并输出建议的分支名称、提交消息和PR描述，供用户复制使用。
<!-- /kg:uuid=de2730e4-7183-512e-ad1c-a26a0b22f1a8 -->

<!-- kg:uuid=2c4c2ace-2d35-50b2-8101-3dbd48c2df48 tag=entity shared=false readonly-meta -->
## Codex配置文件
- **归属**：AI代理技能操作 / 环境配置与初始化

**摘要**（可编辑）
Codex的配置文件，位于~/.codex/config.toml，用于启用特性标志。

**详述**（可编辑）
Codex的配置文件位于~/.codex/config.toml。通过在配置文件中添加[features]部分并设置multi_agent = true，可以启用多代理支持，从而使spawn_agent、wait_agent和close_agent工具在诸如dispatching-parallel-agents和subagent-driven-development等技能中可用。
<!-- /kg:uuid=2c4c2ace-2d35-50b2-8101-3dbd48c2df48 -->

<!-- kg:uuid=93ff1ebb-7b7b-591d-ad07-c26fb29726b2 tag=concept shared=false readonly-meta -->
## Git环境检测
- **归属**：AI代理技能操作 / 环境配置与初始化

**摘要**（可编辑）
技能创建worktrees或完成分支前，使用只读命令检测Git环境的流程。

**详述**（可编辑）
那些需要创建worktrees或完成分支的技能，在进行之前应使用只读的git命令来检测当前环境。具体流程为：运行GIT_DIR=$(cd "$(git rev-parse --git-dir)" 2>/dev/null && pwd -P)、GIT_COMMON=$(cd "$(git rev-parse --git-common-dir)" 2>/dev/null && pwd -P)和BRANCH=$(git branch --show-current)。如果GIT_DIR不等于GIT_COMMON，说明仓库已经处于一个链接的worktree中（此时应跳过创建）；如果BRANCH为空，则表示HEAD处于分离状态（此时无法从沙箱进行分支、推送或创建PR）。这一检测流程被用在using-git-worktrees技能的步骤0和finishing-a-development-branch技能的步骤1中。
<!-- /kg:uuid=93ff1ebb-7b7b-591d-ad07-c26fb29726b2 -->

<!-- kg:uuid=e9c1f125-7819-5c81-b1f3-123c9bef89e8 shared=true mirror=true source=_shared/ai代理技能操作/e9c1f125-7819-5c81-b1f3-123c9bef89e8.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理技能操作/e9c1f125-7819-5c81-b1f3-123c9bef89e8.md` 维护，请勿在此编辑。
> **子代理支持** — 启用多代理/子代理支持功能，在Codex中通过配置multi_agent=true，在Gemini CLI中通过invoke_agent工具调度。
<!-- /kg:uuid=e9c1f125-7819-5c81-b1f3-123c9bef89e8 -->

