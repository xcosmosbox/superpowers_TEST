<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=2b329f45-0fae-5627-81ee-b20ac9c7d113 shared=true mirror=true source=_shared/多智能体开发与任务编排/cli-configuration-skill-directory.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/cli-configuration-skill-directory.md` 维护，请勿在此编辑。
> **CLI配置与技能目录** — 包括Antigravity CLI工具、GEMINI.md指令文件以及Gemini和跨运行时技能目录。
<!-- /kg:uuid=2b329f45-0fae-5627-81ee-b20ac9c7d113 -->

<!-- kg:uuid=196c2775-69d6-530a-8225-e924366ccb75 tag=concept shared=false readonly-meta -->
## Gemini CLI额外工具集
- **归属**：多智能体开发与任务编排 / CLI环境与配置

**摘要**（可编辑）
Gemini CLI独有的会话记忆、计划模式、任务跟踪和MCP资源访问等额外工具。

**详述**（可编辑）
Gemini CLI 提供一系列独有工具，覆盖记忆、计划、交互、任务跟踪与外部资源访问等场景：save_memory 用于持久化记忆（当 experimental.memoryV2 设为 false 时启用）；get_internal_docs 用于查找 Gemini CLI 内部捆绑的文档；ask_user 可向用户发起结构化提问，支持文本输入、单选与多选形式；enter_plan_mode 与 exit_plan_mode 分别用于进入和退出只读计划模式；update_topic 则用于更新当前对话的主题或策略意图元数据；complete_task 作为信号通知子代理任务完成并将结果返回父代理；此外，还包括一套具有依赖管理与可视化能力的任务跟踪器，内含 tracker_create_task、tracker_update_task、tracker_get_task、tracker_list_tasks、tracker_add_dependency 与 tracker_visualize；最后，提供 read_mcp_resource 与 list_mcp_resources 以支持对 MCP 资源的读取与列举。
<!-- /kg:uuid=196c2775-69d6-530a-8225-e924366ccb75 -->

<!-- kg:uuid=b34c79f5-5c48-5049-8b58-961dfdb307b0 shared=true mirror=true source=_shared/多智能体开发与任务编排/sub-agent-scheduling-strategy-lifecycle.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/sub-agent-scheduling-strategy-lifecycle.md` 维护，请勿在此编辑。
> **子代理调度策略与生命周期** — 涵盖多代理启用配置、子代理生命周期管理、并行调度、提示模板填充等调度机制。
<!-- /kg:uuid=b34c79f5-5c48-5049-8b58-961dfdb307b0 -->

<!-- kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc shared=true mirror=true source=_shared/多智能体开发与任务编排/skill-action-mapping-rules.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/多智能体开发与任务编排/skill-action-mapping-rules.md` 维护，请勿在此编辑。
> **技能动作映射规则** — 定义技能语言中的动作如何映射到CLI工具调用，包括通用映射规则和特定于调度子代理、Gemini CLI的映射。
<!-- /kg:uuid=68ba2305-3366-5535-b8c8-b0297710bbfc -->

