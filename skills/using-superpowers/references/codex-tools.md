<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=10054a24-9306-57b9-a0b2-d1b5f9e617cb tag=concept shared=false readonly-meta -->
## Git环境自适应流程
- **归属**：多智能体开发与任务编排 / Git环境检测与流程控制

**摘要**（可编辑）
检测Git环境状态（如链接工作树、分离头），并做出适应性调整，包括指引用户使用App完成分支操作。

**详述**（可编辑）
Git环境自适应流程首先通过只读Git命令检测当前环境状态：执行`GIT_DIR=$(cd "$(git rev-parse --git-dir)" 2>/dev/null && pwd -P)`获取.git目录路径，执行`GIT_COMMON=$(cd "$(git rev-parse --git-common-dir)" 2>/dev/null && pwd -P)`获取公共.git目录路径，并通过`BRANCH=$(git branch --show-current)`获取当前分支名。若`GIT_DIR`与`GIT_COMMON`不同，说明当前已处于链接工作树中，应跳过创建工作树的操作；若`BRANCH`为空，说明处于分离头（detached HEAD）状态，此时沙箱环境无法执行分支创建、推送或创建Pull Request等操作。在分离头状态或沙箱环境因其他限制无法进行分支/推送时，代理应完成当前工作（如暂存文件、运行测试等），并引导用户通过App原生控件完成后续操作。具体有两种衔接方式：一是“创建分支”，由代理建议分支名称，用户通过App UI完成提交、推送和PR创建；二是“移交到本地”，将工作转移到用户的本地检出副本。此过程中代理仍可运行测试、暂存变更，并输出建议的分支名、提交信息和PR描述供用户复制使用。
<!-- /kg:uuid=10054a24-9306-57b9-a0b2-d1b5f9e617cb -->

<!-- kg:uuid=b34c79f5-5c48-5049-8b58-961dfdb307b0 shared=true mirror=true source=_shared/多智能体开发与任务编排/sub-agent-scheduling-strategy-lifecycle.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/sub-agent-scheduling-strategy-lifecycle.md` 维护，请勿在此编辑。
> **子代理调度策略与生命周期** — 涵盖多代理启用配置、子代理生命周期管理、并行调度、提示模板填充等调度机制。
<!-- /kg:uuid=b34c79f5-5c48-5049-8b58-961dfdb307b0 -->

