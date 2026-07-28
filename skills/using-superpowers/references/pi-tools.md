<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=ffd7a4f5-9c6d-5b1b-bf2b-3f842ef77cbf tag=concept shared=false readonly-meta -->
## 任务跟踪规则
- **归属**：AI代理技能操作 / 任务跟踪与流程控制

**摘要**（可编辑）
对于任务跟踪，使用已安装的待办工具或回退到Superpowers计划文件、Markdown清单或TODO.md。

**详述**（可编辑）
Pi 核心不提供标准任务列表工具。如果已安装待办/任务扩展，请使用其文档化的工具；否则，使用 Superpowers 计划文件、Markdown 清单或仓库本地的 TODO.md 进行任务跟踪。较旧的 Superpowers 文档可能提及 TodoWrite，将其视为上述任务跟踪操作。
<!-- /kg:uuid=ffd7a4f5-9c6d-5b1b-bf2b-3f842ef77cbf -->

<!-- kg:uuid=40951761-5450-5a4f-9c52-6086078c3b16 tag=concept shared=false readonly-meta -->
## 子代理回退规则
- **归属**：AI代理技能操作 / 子代理调度与管理

**摘要**（可编辑）
如果子代理工具不可用，则按顺序执行或说明可选功能未安装，不虚构Task调用。

**详述**（可编辑）
如果没有任何可用的子代理工具，不得虚构 Task 调用；应在当前会话中按顺序执行任务，或向用户说明可选的子代理功能尚未安装。此回退规则适用于 Pi 核心环境，当缺少 pi-subagents 包时生效，因为 Pi 核心本身不包含标准的子代理工具。
<!-- /kg:uuid=40951761-5450-5a4f-9c52-6086078c3b16 -->

<!-- kg:uuid=6af7c6be-2e73-5830-afdf-46dcd95e4404 shared=true mirror=true source=_shared/ai代理技能操作/6af7c6be-2e73-5830-afdf-46dcd95e4404.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理技能操作/6af7c6be-2e73-5830-afdf-46dcd95e4404.md` 维护，请勿在此编辑。
> **子代理调度工具** — 调度子代理的底层工具，如Codex的invoke_subagent和pi-subagents包，支持单个、链式、并行等调度模式。
<!-- /kg:uuid=6af7c6be-2e73-5830-afdf-46dcd95e4404 -->

<!-- kg:uuid=5053fce6-6146-5ce3-8d22-1617c933d23c shared=true mirror=true source=_shared/ai代理技能操作/5053fce6-6146-5ce3-8d22-1617c933d23c.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理技能操作/5053fce6-6146-5ce3-8d22-1617c933d23c.md` 维护，请勿在此编辑。
> **工具映射规则** — 将技能动作映射到平台特定工具（如Pi或Gemini CLI）的规则。
<!-- /kg:uuid=5053fce6-6146-5ce3-8d22-1617c933d23c -->

