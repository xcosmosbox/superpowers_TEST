<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=f6a8f8c3-119b-5a9b-89ad-fabcefd66afa tag=entity shared=false readonly-meta -->
## Close Agent 工具
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Codex 中用于关闭不再需要的代理的工具。

**详述**（可编辑）
close_agent 是 Codex 工具，在多代理支持启用后可用。它允许当前代理终止并释放已生成的子代理占用的资源，通常在子代理任务完成或不再需要时调用，以优化系统资源使用。
<!-- /kg:uuid=f6a8f8c3-119b-5a9b-89ad-fabcefd66afa -->

<!-- kg:uuid=05888306-652d-5de9-bf77-e4d687f7904b tag=concept shared=false readonly-meta -->
## Codex App 完成流程
- **归属**：开发工作流 / 代码管理

**摘要**（可编辑）
当沙箱环境阻止分支或推送时，代理提交所有工作并通知用户使用 Codex App 的原生控件来完成后续操作。

**详述**（可编辑）
当沙箱环境因外部管理的工作树处于分离头状态而无法执行分支或推送操作时，代理应遵循 Codex App 的完成流程：首先提交所有工作变更，然后通知并引导用户使用 Codex App 的原生控件来完成后续操作。用户有两种选择：一是使用 “Create branch” 控件输入分支名称，随后在 App 界面中完成提交、推送和 Pull Request 创建；二是使用 “Hand off to local” 控件将工作成果转移至本地检出环境。在此过程中，代理仍可辅助运行测试、暂存文件，并向用户提供建议的分支名、提交信息和 PR 描述，以便用户复制使用。
<!-- /kg:uuid=05888306-652d-5de9-bf77-e4d687f7904b -->

<!-- kg:uuid=5a439118-465b-5d1a-b34f-e66d6a22cb37 tag=entity shared=false readonly-meta -->
## Codex 配置文件
- **归属**：配置与上下文 / 环境配置

**摘要**（可编辑）
Codex 的主配置文件，路径为 ~/.codex/config.toml，包含功能开关等设置。

**详述**（可编辑）
Codex 的主配置文件位于用户主目录下的 `~/.codex/config.toml`。在该文件的 `[features]` 部分可以配置功能开关，例如启用多代理支持等高级功能。
<!-- /kg:uuid=5a439118-465b-5d1a-b34f-e66d6a22cb37 -->

<!-- kg:uuid=1ca7cd48-a087-5f92-81cf-7718673e7d39 tag=entity shared=false readonly-meta -->
## Create Branch 原生控件
- **归属**：开发工作流 / 代码管理

**摘要**（可编辑）
Codex App 中用于创建分支并继续操作的用户界面控件。

**详述**（可编辑）
Create Branch 是 Codex App 中的一个原生控件，当沙箱环境因分离头状态等原因无法直接创建分支时，用户可通过该控件输入期望的分支名称，随后在 Codex App 的用户界面中完成剩余的提交、推送以及 Pull Request 创建操作。
<!-- /kg:uuid=1ca7cd48-a087-5f92-81cf-7718673e7d39 -->

<!-- kg:uuid=a30e558d-950e-5dc8-b593-6e1147aa5efd tag=entity shared=false readonly-meta -->
## Hand Off to Local 原生控件
- **归属**：开发工作流 / 代码管理

**摘要**（可编辑）
Codex App 中用于将当前工作转移到本地环境的控件。

**详述**（可编辑）
Hand Off to Local 是 Codex App 提供的一个原生控件，用于将沙箱中已完成的工作成果直接转移至本地检出的工作环境，使用户能够在本地继续后续的开发工作。
<!-- /kg:uuid=a30e558d-950e-5dc8-b593-6e1147aa5efd -->

<!-- kg:uuid=d17f55e7-353b-5fbc-a402-3cb1eb27f4ef tag=entity shared=false readonly-meta -->
## Spawn Agent 工具
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Codex 中用于动态生成新代理的工具。

**详述**（可编辑）
spawn_agent 是 Codex 内置工具，当多代理支持启用后可用。它允许当前代理动态生成新的子代理，这些子代理可以并行或独立执行任务，是实现并行代理分派和子代理驱动开发的基础工具之一。
<!-- /kg:uuid=d17f55e7-353b-5fbc-a402-3cb1eb27f4ef -->

<!-- kg:uuid=9869663a-fc81-553f-bb68-11a30327108a tag=entity shared=false readonly-meta -->
## Wait Agent 工具
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Codex 中用于等待指定代理完成的工具。

**详述**（可编辑）
wait_agent 是 Codex 工具，在多代理支持启用后可用。它允许当前代理等待某个已生成的子代理完成其任务，常用于同步并行流程，确保父代理在子代理工作结束后再继续执行。
<!-- /kg:uuid=9869663a-fc81-553f-bb68-11a30327108a -->

<!-- kg:uuid=b3504714-0737-5fb4-8153-cc7bbcd49437 tag=concept shared=false readonly-meta -->
## 多代理支持配置
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
在 Codex 配置中启用 multi_agent 特性，以支持子代理的生成、等待与关闭。

**详述**（可编辑）
通过在 Codex 配置文件 ~/.codex/config.toml 的 [features] 部分设置 multi_agent = true，可以启用多代理支持。启用后，代理将获得 spawn_agent、wait_agent 和 close_agent 三个工具，从而能够执行 dispatching-parallel-agents 和 subagent-driven-development 等高级技能，实现子代理的生成、等待与关闭。
<!-- /kg:uuid=b3504714-0737-5fb4-8153-cc7bbcd49437 -->

<!-- kg:uuid=a27f7d07-fe20-5635-9805-ec3d3e7e66b6 tag=concept shared=false readonly-meta -->
## 子代理调度最佳实践
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
使用子代理驱动开发时的最佳实践，如及时关闭 reviewer、修复循环等。

**详述**（可编辑）
在使用 subagent-driven-development 技能时，应遵循以下调度最佳实践：一旦 reviewer 子代理返回审查结果，应立即关闭它们以释放资源。每个 implementer 子代理应保持打开状态，直到其任务的审查通过——后续的修复循环将直接恢复该 implementer 继续工作，而不是创建新代理。如果运行环境无法向已生成的代理发送另一条消息，则应为每个修复轮次分派一个新的 implementer，并携带简报、报告文件和审查发现，以衔接上下文。
<!-- /kg:uuid=a27f7d07-fe20-5635-9805-ec3d3e7e66b6 -->

<!-- kg:uuid=e9ca63ab-6caa-5c5d-909b-06db1aae37a9 tag=concept shared=false readonly-meta -->
## 环境检测方法
- **归属**：开发工作流 / 代码管理

**摘要**（可编辑）
在执行工作树创建或分支完成操作前，通过只读 git 命令检测当前状态。

**详述**（可编辑）
在进行工作树创建或分支完成操作之前，应执行一系列只读 Git 命令以检测当前环境状态。具体包括：通过 GIT_DIR=$(cd "$(git rev-parse --git-dir)" 2>/dev/null && pwd -P) 获取 .git 目录的绝对路径；通过 GIT_COMMON=$(cd "$(git rev-parse --git-common-dir)" 2>/dev/null && pwd -P) 获取通用目录路径；通过 BRANCH=$(git branch --show-current) 获取当前分支名。若 GIT_DIR 与 GIT_COMMON 不相等，说明当前已处于链接工作树中，应跳过工作树创建步骤；若 BRANCH 为空，则表示处于分离头状态，此时无法从沙箱进行分支、推送或发起 PR。该检测方法应用于 using-git-worktrees 技能的 Step 0 和 finishing-a-development-branch 技能的 Step 1。
<!-- /kg:uuid=e9ca63ab-6caa-5c5d-909b-06db1aae37a9 -->

