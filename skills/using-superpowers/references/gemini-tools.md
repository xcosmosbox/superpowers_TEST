<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=250c47c2-2df0-584a-acf5-d6ba2d09bfa1 tag=concept shared=false readonly-meta -->
## GEMINI.md加载机制
- **归属**：AI代理增强与技能集成 / 技能映射与环境配置

**摘要**（可编辑）
层次化加载GEMINI.md指令文件的方法

**详述**（可编辑）
在 Gemini CLI 中，当技能提到 'your instructions file' 时，指代的是 GEMINI.md 文件。Gemini CLI 层次化地加载 GEMINI.md：全局文件位于 ~/.gemini/GEMINI.md，项目级文件存在于工作区目录及其祖先目录中，并且当工具访问子目录中的文件时，也会加载该子目录中的 GEMINI.md。
<!-- /kg:uuid=250c47c2-2df0-584a-acf5-d6ba2d09bfa1 -->

<!-- kg:uuid=4c2b4149-d103-52fe-be38-5158a4951c8b tag=entity shared=false readonly-meta -->
## activate_skill工具
- **归属**：AI代理增强与技能集成 / 技能映射与环境配置

**摘要**（可编辑）
激活一个技能的工具

**详述**（可编辑）
`activate_skill` 工具用于在 Gemini CLI 中激活并执行一个已安装的技能，它对应于技能请求中的 'Invoke a skill' 动作。
<!-- /kg:uuid=4c2b4149-d103-52fe-be38-5158a4951c8b -->

<!-- kg:uuid=4c753169-fe1b-5e8e-925f-938b006ae1b3 tag=entity shared=false readonly-meta -->
## ask_user工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
向用户提出结构化问题

**详述**（可编辑）
在 Gemini CLI 中，`ask_user` 工具用于向用户提出结构化的问题，支持文本输入、单选和多选三种交互形式。
<!-- /kg:uuid=4c753169-fe1b-5e8e-925f-938b006ae1b3 -->

<!-- kg:uuid=73bbe028-0bc1-52de-88c0-96495a78278e tag=entity shared=false readonly-meta -->
## complete_task工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
表明子代理完成并返回结果

**详述**（可编辑）
在 Gemini CLI 中，`complete_task` 工具用于在子代理完成任务时发出信号，并将结果返回给父代理。
<!-- /kg:uuid=73bbe028-0bc1-52de-88c0-96495a78278e -->

<!-- kg:uuid=e344c64e-63b1-5d7e-9bf8-a5f9feb5daf5 tag=entity shared=false readonly-meta -->
## enter_plan_mode工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
进入只读计划模式

**详述**（可编辑）
在 Gemini CLI 中，`enter_plan_mode` 工具用于切换到只读的计划模式，在此模式下不会修改文件。
<!-- /kg:uuid=e344c64e-63b1-5d7e-9bf8-a5f9feb5daf5 -->

<!-- kg:uuid=9000b877-f295-5fba-abc5-335da0178a13 tag=entity shared=false readonly-meta -->
## exit_plan_mode工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
退出计划模式

**详述**（可编辑）
在 Gemini CLI 中，`exit_plan_mode` 工具用于从只读计划模式中退出，恢复正常操作。
<!-- /kg:uuid=9000b877-f295-5fba-abc5-335da0178a13 -->

<!-- kg:uuid=84bb7002-6d4b-5469-bd09-18e8d09320bb tag=entity shared=false readonly-meta -->
## get_internal_docs工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
查阅Gemini CLI内置文档

**详述**（可编辑）
在 Gemini CLI 中，`get_internal_docs` 工具用于查找和获取 Gemini CLI 捆绑的内部文档。
<!-- /kg:uuid=84bb7002-6d4b-5469-bd09-18e8d09320bb -->

<!-- kg:uuid=7a1473fb-d949-5360-92a0-0c12d4b0cb3a tag=entity shared=false readonly-meta -->
## glob工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
通过通配模式查找文件

**详述**（可编辑）
在 Gemini CLI 中，`glob` 工具对应技能请求中的 'Find files by name' 动作，使用 glob 模式按名称查找文件。
<!-- /kg:uuid=7a1473fb-d949-5360-92a0-0c12d4b0cb3a -->

<!-- kg:uuid=04565458-4937-5de2-8853-85137b4bafe7 tag=entity shared=false readonly-meta -->
## google_web_search工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
执行Google网络搜索

**详述**（可编辑）
在 Gemini CLI 中，`google_web_search` 工具对应技能请求中的 'Search the web' 动作，用于执行 Google 网络搜索。
<!-- /kg:uuid=04565458-4937-5de2-8853-85137b4bafe7 -->

<!-- kg:uuid=ce7af0d2-8ac2-5647-ac5e-13c9a5036bdf tag=entity shared=false readonly-meta -->
## grep_search工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
搜索文件内容

**详述**（可编辑）
在 Gemini CLI 中，`grep_search` 工具对应技能请求中的 'Search file contents' 动作，用于在文件中搜索匹配特定模式的内容。
<!-- /kg:uuid=ce7af0d2-8ac2-5647-ac5e-13c9a5036bdf -->

<!-- kg:uuid=fbf32595-c56e-5db3-940d-1f26d1072778 tag=entity shared=false readonly-meta -->
## list_directory工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
列出目录中的文件和子目录

**详述**（可编辑）
在 Gemini CLI 中，`list_directory` 工具对应技能请求中的 'List files and subdirectories' 动作，用于列出指定目录下的文件和子目录列表。
<!-- /kg:uuid=fbf32595-c56e-5db3-940d-1f26d1072778 -->

<!-- kg:uuid=f1015053-61eb-522b-b40f-bdd94f08218c tag=entity shared=false readonly-meta -->
## list_mcp_resources工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
列出可用的MCP资源

**详述**（可编辑）
在 Gemini CLI 中，`list_mcp_resources` 工具用于列出所有通过 Model Context Protocol (MCP) 提供的可用资源。
<!-- /kg:uuid=f1015053-61eb-522b-b40f-bdd94f08218c -->

<!-- kg:uuid=c1dbed04-2787-5441-952b-5a2d7acfad54 tag=entity shared=false readonly-meta -->
## read_file工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
读取单个文件

**详述**（可编辑）
在 Gemini CLI 中，`read_file` 工具对应技能请求中的 'Read a file' 动作，用于读取单个指定文件的内容。
<!-- /kg:uuid=c1dbed04-2787-5441-952b-5a2d7acfad54 -->

<!-- kg:uuid=67bd180f-b4e6-54cf-8186-d805884ed13e tag=entity shared=false readonly-meta -->
## read_many_files工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
一次性读取多个文件

**详述**（可编辑）
在 Gemini CLI 中，`read_many_files` 工具对应技能请求中的 'Read multiple files at once' 动作，用于一次性读取多个文件的内容。
<!-- /kg:uuid=67bd180f-b4e6-54cf-8186-d805884ed13e -->

<!-- kg:uuid=fd959bdd-45ad-5a00-9dcb-4815851da28f tag=entity shared=false readonly-meta -->
## read_mcp_resource工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
读取MCP资源

**详述**（可编辑）
在 Gemini CLI 中，`read_mcp_resource` 工具用于读取通过 Model Context Protocol (MCP) 提供的资源。
<!-- /kg:uuid=fd959bdd-45ad-5a00-9dcb-4815851da28f -->

<!-- kg:uuid=614130f4-7e57-53da-90fa-ce6e39d34545 tag=entity shared=false readonly-meta -->
## replace工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
编辑文件内容

**详述**（可编辑）
在 Gemini CLI 中，`replace` 工具对应技能请求中的 'Edit a file' 动作，用于修改现有文件的内容。
<!-- /kg:uuid=614130f4-7e57-53da-90fa-ce6e39d34545 -->

<!-- kg:uuid=52f1cd5b-3b10-5b3b-ad8d-276ed301ab2d tag=entity shared=false readonly-meta -->
## run_shell_command工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
运行shell命令

**详述**（可编辑）
在 Gemini CLI 中，`run_shell_command` 工具对应技能请求中的 'Run a shell command' 动作，用于执行任意的 shell 命令。
<!-- /kg:uuid=52f1cd5b-3b10-5b3b-ad8d-276ed301ab2d -->

<!-- kg:uuid=01c61314-6c94-5526-80d2-785fa3052049 tag=entity shared=false readonly-meta -->
## save_memory工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
跨会话持久化事实（遗留工具）

**详述**（可编辑）
在 Gemini CLI 中，`save_memory` 工具是一个遗留工具，用于当 `experimental.memoryV2` 设置为 `false` 时，跨会话持久化事实数据。
<!-- /kg:uuid=01c61314-6c94-5526-80d2-785fa3052049 -->

<!-- kg:uuid=9e2a951b-6eb4-5f09-aa97-4dfe33dfa69b tag=entity shared=false readonly-meta -->
## update_topic工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
更新当前对话的主题元数据

**详述**（可编辑）
在 Gemini CLI 中，`update_topic` 工具用于更新当前对话的主题或战略意图元数据信息。
<!-- /kg:uuid=9e2a951b-6eb4-5f09-aa97-4dfe33dfa69b -->

<!-- kg:uuid=3596b449-5341-5359-b8f9-2cac0240c618 tag=entity shared=false readonly-meta -->
## web_fetch工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
获取URL的内容

**详述**（可编辑）
在 Gemini CLI 中，`web_fetch` 工具对应技能请求中的 'Fetch a URL' 动作，用于获取指定 URL 的网络资源内容。
<!-- /kg:uuid=3596b449-5341-5359-b8f9-2cac0240c618 -->

<!-- kg:uuid=867a24d1-1f9b-5b1d-86cf-355f6a06c138 tag=entity shared=false readonly-meta -->
## write_file工具
- **归属**：AI代理增强与技能集成 / 通用工具集

**摘要**（可编辑）
创建新文件并写入内容

**详述**（可编辑）
在 Gemini CLI 中，`write_file` 工具对应技能请求中的 'Create a new file' 动作，用于创建新文件并写入内容。
<!-- /kg:uuid=867a24d1-1f9b-5b1d-86cf-355f6a06c138 -->

<!-- kg:uuid=9c84c7ae-3d90-583f-a925-18ac5e2222ae tag=entity shared=false readonly-meta -->
## write_todos工具
- **归属**：AI代理增强与技能集成 / 任务追踪与组织

**摘要**（可编辑）
创建和更新任务追踪列表的工具

**详述**（可编辑）
write_todos 工具对应技能请求中的 'Task tracking' 动作，用于创建和更新任务待办列表。它支持多种任务状态，包括 pending（待处理）、in_progress（进行中）、completed（已完成）、cancelled（已取消）和 blocked（阻塞）。通过此工具可以管理任务的生命周期，确保任务跟踪清晰有序。
<!-- /kg:uuid=9c84c7ae-3d90-583f-a925-18ac5e2222ae -->

<!-- kg:uuid=ede1828c-d611-5435-a7a0-a9a59984a766 tag=concept shared=false readonly-meta -->
## 任务追踪器工具集
- **归属**：AI代理增强与技能集成 / 任务追踪与组织

**摘要**（可编辑）
提供依赖管理和可视化的丰富任务追踪工具集合

**详述**（可编辑）
Gemini CLI 提供了一套丰富的任务追踪器工具集，包括 tracker_create_task（创建任务）、tracker_update_task（更新任务）、tracker_get_task（获取任务详情）、tracker_list_tasks（列出所有任务）、tracker_add_dependency（添加任务依赖）和 tracker_visualize（可视化任务关系）。这些工具支持完整的任务生命周期管理，能够创建和更新任务状态，建立任务之间的依赖关系，并以可视化的方式展示任务进展和结构，从而实现对复杂任务的高效组织与追踪。
<!-- /kg:uuid=ede1828c-d611-5435-a7a0-a9a59984a766 -->

<!-- kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 shared=true mirror=true source=_shared/ai代理增强与技能集成/sub-agent-scheduling-tool.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/ai代理增强与技能集成/sub-agent-scheduling-tool.md` 维护，请勿在此编辑。
> **子代理调度工具** — 用于调度子代理执行任务的工具，涵盖多种实现和变体
<!-- /kg:uuid=0c3512bb-01a0-554a-90c2-82ac75464088 -->

<!-- kg:uuid=b3b0ff5f-63b6-5625-ad1e-206b3a54a944 tag=concept shared=false readonly-meta -->
## 并行子代理调度
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
同时调度多个独立的子代理任务

**详述**（可编辑）
Gemini CLI 支持在同一响应中同时调度多个独立的子代理任务，以实现并行执行。这可以通过在一条响应中发出多个 invoke_agent 调用，或在提示中多次使用 @generalist 语法来完成。相互存在依赖关系的子代理任务必须保持顺序执行，但不应为了简化对话历史而将原本相互独立的子代理任务强行串行化，从而浪费并行执行的优势。
<!-- /kg:uuid=b3b0ff5f-63b6-5625-ad1e-206b3a54a944 -->

<!-- kg:uuid=70ad7211-3d09-5661-a000-94b54272c1b0 tag=entity shared=false readonly-meta -->
## 技能存储目录
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
用户级技能的存储位置

**详述**（可编辑）
用户级技能存储在 ~/.gemini/skills/ 目录下。此外，还存在一个跨运行时共享的别名目录 ~/.agents/skills/，该目录与 Codex 和 Copilot CLI 共享。当两个目录在同一作用域内同时存在时，~/.agents/skills/ 具有优先权。每个技能以子目录形式组织，其中必须包含一个 SKILL.md 文件，该文件使用前置元数据定义技能的 name 和 description。
<!-- /kg:uuid=70ad7211-3d09-5661-a000-94b54272c1b0 -->

<!-- kg:uuid=e7ec99a9-55b9-5d63-8677-2a814d2a9ccf tag=concept shared=false readonly-meta -->
## 提示模板填充
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
调度子代理前替换提示模板中的占位符

**详述**（可编辑）
技能中的子代理调度动作可能引用外部提示模板文件（例如 superpowers:subagent-driven-development 的 ./implementer-prompt.md），或者直接提供内联提示。在 Gemini CLI 上，实际调用 invoke_agent 之前，必须将模板中的所有占位符（例如 {WHAT_WAS_IMPLEMENTED} 或 [FULL TEXT of task]）替换为具体内容，然后将填充完整的提示传递给子代理。提示模板本身通常定义了代理的角色定位、评审标准以及期望的输出格式，确保子代理能够按照预定规范执行任务。
<!-- /kg:uuid=e7ec99a9-55b9-5d63-8677-2a814d2a9ccf -->

<!-- kg:uuid=b6c7b813-9d4d-5f61-892d-389a9261fba7 tag=concept shared=false readonly-meta -->
## 通用子代理快捷方式
- **归属**：AI代理增强与技能集成 / 子代理调度与集成

**摘要**（可编辑）
通过@generalist快速调度通用子代理

**详述**（可编辑）
在 Gemini CLI 中，可以通过 @generalist <prompt> 语法快捷调度通用子代理，此操作完全等价于调用 invoke_agent 工具并指定 agent_name: 'generalist'。除了 generalist 外，Gemini CLI 还内置了其他代理名称，如 cli_help（用于 CLI 帮助）和 codebase_investigator（用于代码库调查），以及在启用浏览器工具时提供的 browser_agent。
<!-- /kg:uuid=b6c7b813-9d4d-5f61-892d-389a9261fba7 -->

