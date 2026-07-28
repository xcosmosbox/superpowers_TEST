<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=c26106ee-12d1-5c0c-8ec4-897c688ab491 tag=concept shared=false readonly-meta -->
## 任务跟踪动作映射
- **归属**：多智能体开发与任务编排 / 任务跟踪与工件管理

**摘要**（可编辑）
将技能动作“Task tracking”映射到实际任务跟踪手段的规则。

**详述**（可编辑）
任务跟踪动作映射规则定义了如何将技能中抽象的“Task tracking”动作（包括“创建待办”和“标记完成”）转化为实际的执行手段。在 Pi 平台上，该动作的等价操作应优先使用已安装的待办或任务管理工具；若此类工具不可用，则回退到使用计划文件、Markdown 检查清单或 TODO.md 文件进行任务跟踪。同时，旧版文档中出现的 TodoWrite 动作在工具映射中也应视为“Task tracking”动作的具体调用，同样遵循上述映射规则。
<!-- /kg:uuid=c26106ee-12d1-5c0c-8ec4-897c688ab491 -->

<!-- kg:uuid=ecb8907c-acc1-571f-9cbd-d034b5d3a1c2 shared=true mirror=true source=_shared/多智能体开发与任务编排/task-tracking-artifacts.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/task-tracking-artifacts.md` 维护，请勿在此编辑。
> **任务跟踪工件** — 用于记录任务状态的Markdown文件、计划文件或检查清单工件，包括TODO.md、Superpowers计划文件和任务artifact。
<!-- /kg:uuid=ecb8907c-acc1-571f-9cbd-d034b5d3a1c2 -->

<!-- kg:uuid=3ff2eeb1-4f02-5e80-a2a2-3e532dae99c4 shared=true mirror=true source=_shared/多智能体开发与任务编排/sub-agent-scheduling-toolset.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/sub-agent-scheduling-toolset.md` 维护，请勿在此编辑。
> **子代理调度工具集** — 包含pi-subagents包、subagent工具和invoke_subagent工具，用于派生子代理。
<!-- /kg:uuid=3ff2eeb1-4f02-5e80-a2a2-3e532dae99c4 -->

<!-- kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc shared=true mirror=true source=_shared/多智能体开发与任务编排/skill-action-mapping-rules.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/skill-action-mapping-rules.md` 维护，请勿在此编辑。
> **技能动作映射规则** — 定义技能语言中的动作如何映射到CLI工具调用，包括通用映射规则和特定于调度子代理、Gemini CLI的映射。
<!-- /kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc -->

