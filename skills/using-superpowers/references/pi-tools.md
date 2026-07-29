<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=6f792a20-2246-5d35-b7fa-78f97a4bf990 tag=entity shared=false readonly-meta -->
## pi-subagents包
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
提供子代理工具的可选伴侣包

**详述**（可编辑）
pi-subagents 是一个为 Pi 平台提供的强力可选伴侣包，并不随 Pi 核心一同发布，需单独安装。该包提供了一个 subagent 工具，能够支持多种子代理工作流，包括单一代理任务、链式调用、并行执行、异步操作、分叉上下文处理以及恢复和状态监控等。当 Pi 环境中需要子代理功能时，推荐使用此包作为标准实现，但若未安装，则不存在内置子代理工具。
<!-- /kg:uuid=6f792a20-2246-5d35-b7fa-78f97a4bf990 -->

<!-- kg:uuid=3935e6c5-9a0f-5c14-aebe-17da8c12f0cb shared=true mirror=true source=_shared/ai代理增强与技能集成/action-mapping-rule.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理增强与技能集成/action-mapping-rule.md` 维护，请勿在此编辑。
> **动作映射规则** — 定义技能动作如何映射到具体工具调用的规则
<!-- /kg:uuid=3935e6c5-9a0f-5c14-aebe-17da8c12f0cb -->

<!-- kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 shared=true mirror=true source=_shared/ai代理增强与技能集成/sub-agent-scheduling-tool.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理增强与技能集成/sub-agent-scheduling-tool.md` 维护，请勿在此编辑。
> **子代理调度工具** — 用于调度子代理执行任务的工具，涵盖多种实现和变体
<!-- /kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 -->

<!-- kg:uuid=614ff5f4-8c27-53a9-91ff-4dbeab5b1b34 tag=concept shared=false readonly-meta -->
## 工具可用性说明
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
关于核心环境缺少某工具时的备选方案和说明

**详述**（可编辑）
Pi 核心环境默认不提供标准的子代理工具或任务列表工具。子代理功能可通过安装可选的 pi-subagents 包获得，该包提供的 subagent 工具支持多种工作流。若未安装任何子代理工具，系统不得虚构 Task 调用，而应在当前会话中顺序执行任务，或明确告知用户可选子代理能力未安装。对于任务跟踪，优先使用已安装的待办事项或任务扩展提供的工具；若无此类扩展，则采用 Superpowers 计划文件、Markdown 检查清单或仓库本地的 TODO.md 文件作为替代方案。此外，旧版 Superpowers 文档中提及的 TodoWrite 应理解为对应当前版本的任务跟踪动作，以保持文档的向后兼容性。
<!-- /kg:uuid=614ff5f4-8c27-53a9-91ff-4dbeab5b1b34 -->

