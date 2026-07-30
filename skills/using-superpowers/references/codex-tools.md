<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=7c69f017-552a-5625-a62b-71131f53050f tag=concept shared=false readonly-meta -->
## Codex应用完成工作流
- **归属**：AI代理能力扩展 / 知识持久化与配置

**摘要**（可编辑）
沙箱环境下引导用户通过原生控件完成推送等工作流。

**详述**（可编辑）
Codex 应用完成工作流是指在沙箱环境（例如处于分离头状态或外部管理工作树）阻止分支或推送操作时，代理会将所有工作提交并通知用户通过应用的原生控件完成后续流程。用户有两个选择：一是“创建分支”，即创建一个新分支（用户命名），然后借助应用 UI 提交、推送并创建 PR；二是“转移到本地”，将当前工作转移到本地检出以便本地处理。在整个过程中，代理仍然能够运行测试、暂存文件，并输出建议的分支名称、提交消息和 PR 描述，供用户复制使用。
<!-- /kg:uuid=7c69f017-552a-5625-a62b-71131f53050f -->

<!-- kg:uuid=58145a4f-928b-5328-8140-25a215dd7682 tag=entity shared=false readonly-meta -->
## 多代理配置
- **归属**：AI代理能力扩展 / 子代理管理

**摘要**（可编辑）
启用多代理支持的配置项。

**详述**（可编辑）
多代理配置是指在 Codex 配置文件（~/.codex/config.toml）中，通过将 [features] 段下的 multi_agent 设置为 true 来启用对多代理的支持。启用后，系统会提供 spawn_agent、wait_agent、close_agent 等工具，这些工具可用于实现诸如并行代理调度（dispatching-parallel-agents）和子代理驱动开发（subagent-driven-development）等高级技能。
<!-- /kg:uuid=58145a4f-928b-5328-8140-25a215dd7682 -->

<!-- kg:uuid=b600e3bb-e1b3-59cf-afd8-ff6de9ef9a7e shared=true mirror=true source=_shared/ai代理能力扩展/sub-agent-scheduling.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理能力扩展/sub-agent-scheduling.md` 维护，请勿在此编辑。
> **子代理调度** — 涵盖子代理调度工具、并行调度、提示模板填充和通用快捷方式的核心概念，以及管理子代理审查与生命周期的一般规则。
<!-- /kg:uuid=b600e3bb-e1b3-59cf-afd8-ff6de9ef9a7e -->

