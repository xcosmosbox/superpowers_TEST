<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=8f4b2cda-0716-5bc8-a5d2-bce7cb1c05eb tag=concept shared=false readonly-meta -->
## GEMINI.md指令文件
- **归属**：AI代理技能操作 / 环境配置与初始化

**摘要**（可编辑）
Gemini CLI中支持层次化加载的技能指令文件。

**详述**（可编辑）
在Gemini CLI中，当技能提到“你的指令文件”时，所指的就是GEMINI.md。Gemini CLI以层次化方式加载GEMINI.md：全局文件位于~/.gemini/GEMINI.md，项目级文件存在于工作区目录及其祖先目录中，此外还有子目录中的GEMINI.md文件，在工具访问这些目录中的文件时使用。
<!-- /kg:uuid=8f4b2cda-0716-5bc8-a5d2-bce7cb1c05eb -->

<!-- kg:uuid=fcd3b3f2-079f-5013-b3bf-adf9ba4a4043 tag=entity shared=false readonly-meta -->
## Gemini CLI任务跟踪器
- **归属**：AI代理技能操作 / 任务跟踪与流程控制

**摘要**（可编辑）
一组丰富的任务跟踪工具，支持依赖关系和可视化。

**详述**（可编辑）
Gemini CLI 提供了一组丰富的任务跟踪工具，包括 tracker_create_task、tracker_update_task、tracker_get_task、tracker_list_tasks、tracker_add_dependency 和 tracker_visualize，用于管理任务、依赖关系和可视化。
<!-- /kg:uuid=fcd3b3f2-079f-5013-b3bf-adf9ba4a4043 -->

<!-- kg:uuid=f6e40603-50b0-5c25-8347-b04a7bedf351 tag=entity shared=false readonly-meta -->
## MCP资源工具
- **归属**：AI代理技能操作 / 辅助工具与交互

**摘要**（可编辑）
read_mcp_resource和list_mcp_resources用于访问MCP资源。

**详述**（可编辑）
read_mcp_resource 和 list_mcp_resources 是 Gemini CLI 中的两个工具，用于访问 MCP（Model Context Protocol）资源。
<!-- /kg:uuid=f6e40603-50b0-5c25-8347-b04a7bedf351 -->

<!-- kg:uuid=b88bc5e8-aada-5467-b9e9-5dd68de4894f tag=entity shared=false readonly-meta -->
## ask_user工具
- **归属**：AI代理技能操作 / 辅助工具与交互

**摘要**（可编辑）
向用户提出结构化问题的工具，支持文本、单选、多选。

**详述**（可编辑）
ask_user 是 Gemini CLI 中的一个工具，用于向用户提出结构化问题，支持文本输入、单选和多选问题类型。
<!-- /kg:uuid=b88bc5e8-aada-5467-b9e9-5dd68de4894f -->

<!-- kg:uuid=027fd4a0-fd47-562c-83bc-bd49cd79072e tag=entity shared=false readonly-meta -->
## complete_task工具
- **归属**：AI代理技能操作 / 子代理调度与管理

**摘要**（可编辑）
表明Gemini子代理已完成并返回结果给父代理。

**详述**（可编辑）
complete_task 是 Gemini CLI 的工具，用于向父代理发出信号，表明某个 Gemini 子代理任务已完成，并将结果返回给父代理。
<!-- /kg:uuid=027fd4a0-fd47-562c-83bc-bd49cd79072e -->

<!-- kg:uuid=ec880575-37bf-5a06-b4d5-aeb1dcdd8c16 tag=entity shared=false readonly-meta -->
## get_internal_docs工具
- **归属**：AI代理技能操作 / 辅助工具与交互

**摘要**（可编辑）
查阅Gemini CLI内置文档的工具。

**详述**（可编辑）
get_internal_docs 是 Gemini CLI 中的一个工具，用于查找和访问 Gemini CLI 绑定的内置文档。
<!-- /kg:uuid=ec880575-37bf-5a06-b4d5-aeb1dcdd8c16 -->

<!-- kg:uuid=79afc46d-c427-566e-92bd-92dbd23ba37a tag=entity shared=false readonly-meta -->
## save_memory（旧版）
- **归属**：AI代理技能操作 / 辅助工具与交互

**摘要**（可编辑）
在experimental.memoryV2为false时，跨会话持久化事实的工具。

**详述**（可编辑）
save_memory 是 Gemini CLI 的遗留工具，在 experimental.memoryV2 设置为 false 时启用，用于跨会话持久化保存事实。
<!-- /kg:uuid=79afc46d-c427-566e-92bd-92dbd23ba37a -->

<!-- kg:uuid=8fe9c7e5-fb54-5df7-a056-bffea1e64588 tag=entity shared=false readonly-meta -->
## update_topic工具
- **归属**：AI代理技能操作 / 辅助工具与交互

**摘要**（可编辑）
更新当前对话的话题或战略意图元数据。

**详述**（可编辑）
update_topic 是 Gemini CLI 中的一个工具，用于更新当前对话的话题或战略意图元数据。
<!-- /kg:uuid=8fe9c7e5-fb54-5df7-a056-bffea1e64588 -->

<!-- kg:uuid=c16bad34-259d-5ce2-a72e-7cef0d77e9e5 tag=concept shared=false readonly-meta -->
## 个人技能目录
- **归属**：AI代理技能操作 / 环境配置与初始化

**摘要**（可编辑）
用户级技能存放在~/.gemini/skills/和~/.agents/skills/，后者优先。

**详述**（可编辑）
用户级技能存放在~/.gemini/skills/目录中，同时~/.agents/skills/作为跨运行时别名，与Codex和Copilot CLI共享。当两个目录在同一作用域都存在时，.agents/skills/优先。每个技能为一个子目录，其中包含一个SKILL.md文件，该文件必须含有name和description前置元数据。
<!-- /kg:uuid=c16bad34-259d-5ce2-a72e-7cef0d77e9e5 -->

<!-- kg:uuid=73136ab9-5367-546f-be07-0a45e47f3113 tag=concept shared=false readonly-meta -->
## 子代理提示填充
- **归属**：AI代理技能操作 / 子代理调度与管理

**摘要**（可编辑）
调用invoke_agent前，须用实际内容替换提示模板中的占位符。

**详述**（可编辑）
在调用 invoke_agent 之前，必须将技能提供的提示模板中的所有占位符替换为实际内容。常见占位符如 {WHAT_WAS_IMPLEMENTED} 或 [FULL TEXT of task] 等。填充完毕后，将完整的提示文本传递给 invoke_agent。提示模板本身定义了子代理的角色、审查标准和期望的输出格式，子代理会遵循这些指示。
<!-- /kg:uuid=73136ab9-5367-546f-be07-0a45e47f3113 -->

<!-- kg:uuid=e9c1f125-7819-5c81-b1f3-123c9bef89e8 shared=true mirror=true source=_shared/ai代理技能操作/e9c1f125-7819-5c81-b1f3-123c9bef89e8.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理技能操作/e9c1f125-7819-5c81-b1f3-123c9bef89e8.md` 维护，请勿在此编辑。
> **子代理支持** — 启用多代理/子代理支持功能，在Codex中通过配置multi_agent=true，在Gemini CLI中通过invoke_agent工具调度。
<!-- /kg:uuid=e9c1f125-7819-5c81-b1f3-123c9bef89e8 -->

<!-- kg:uuid=5053fce6-6146-5ce3-8d22-1617c933d23c shared=true mirror=true source=_shared/ai代理技能操作/5053fce6-6146-5ce3-8d22-1617c933d23c.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理技能操作/5053fce6-6146-5ce3-8d22-1617c933d23c.md` 维护，请勿在此编辑。
> **工具映射规则** — 将技能动作映射到平台特定工具（如Pi或Gemini CLI）的规则。
<!-- /kg:uuid=5053fce6-6146-5ce3-8d22-1617c933d23c -->

<!-- kg:uuid=d2ad638d-aab0-5cee-8ee6-cf6e33ee28ac tag=concept shared=false readonly-meta -->
## 并行子代理调度
- **归属**：AI代理技能操作 / 子代理调度与管理

**摘要**（可编辑）
Gemini CLI支持在同一响应中并行调用多个子代理。

**详述**（可编辑）
Gemini CLI 支持并行子代理调度：可在同一响应中发出多个 invoke_agent 调用，或在同一条提示中多次使用 @generalist 等快捷方式，使独立的子代理任务并行执行，以提高效率。对于存在依赖关系的任务，必须保持顺序执行；但不应仅为简化对话历史而将原本可并行的独立子代理任务强制序列化。
<!-- /kg:uuid=d2ad638d-aab0-5cee-8ee6-cf6e33ee28ac -->

<!-- kg:uuid=e94d92d9-795e-502f-847c-9f4e5a9c07d0 tag=entity shared=false readonly-meta -->
## 计划模式管理
- **归属**：AI代理技能操作 / 任务跟踪与流程控制

**摘要**（可编辑）
进入和退出只读计划模式的工具对。

**详述**（可编辑）
enter_plan_mode 和 exit_plan_mode 是 Gemini CLI 的一对工具，用于切换进入和退出只读计划模式。
<!-- /kg:uuid=e94d92d9-795e-502f-847c-9f4e5a9c07d0 -->

