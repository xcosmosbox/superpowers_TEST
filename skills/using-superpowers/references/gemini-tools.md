<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=cc7a06b6-4d56-5021-9fe1-a9f0c13da6f2 tag=concept shared=false readonly-meta -->
## GEMINI.md加载机制
- **归属**：技能与配置管理 / 技能激活与存储

**摘要**（可编辑）
层次化加载GEMINI.md指令文件的方法。

**详述**（可编辑）
在 Gemini CLI 中，当技能提到 'your instructions file' 时，指代的是 GEMINI.md 文件。Gemini CLI 层次化地加载 GEMINI.md：全局文件位于 ~/.gemini/GEMINI.md，项目级文件存在于工作区目录及其祖先目录中，并且当工具访问子目录中的文件时，也会加载该子目录中的 GEMINI.md。
<!-- /kg:uuid=cc7a06b6-4d56-5021-9fe1-a9f0c13da6f2 -->

<!-- kg:uuid=9de6724b-a0f0-580a-8040-e75e7d75cf71 tag=entity shared=false readonly-meta -->
## Google搜索工具
- **归属**：核心工具集 / 搜索与信息检索

**摘要**（可编辑）
执行Google网络搜索。

**详述**（可编辑）
在 Gemini CLI 中，Google搜索工具对应 `google_web_search` 工具，用于执行 Google 网络搜索，其技能请求动作为 'Search the web'。
<!-- /kg:uuid=9de6724b-a0f0-580a-8040-e75e7d75cf71 -->

<!-- kg:uuid=56575c00-70fa-5594-8f1f-c6951a7659c0 tag=entity shared=false readonly-meta -->
## 任务列表工具
- **归属**：代理协作与任务管理 / 任务追踪

**摘要**（可编辑）
创建和更新任务追踪列表。

**详述**（可编辑）
write_todos 工具是用于在技能请求中执行“任务跟踪”动作的专用工具，可创建和更新任务待办列表。它支持完整的任务生命周期管理，任务状态包括 pending（待处理）、in_progress（进行中）、completed（已完成）、cancelled（已取消）和 blocked（阻塞），从而确保任务跟踪清晰有序。
<!-- /kg:uuid=56575c00-70fa-5594-8f1f-c6951a7659c0 -->

<!-- kg:uuid=ede1828c-d611-5435-a7a0-a9a59984a766 tag=concept shared=false readonly-meta -->
## 任务追踪器工具集
- **归属**：代理协作与任务管理 / 任务追踪

**摘要**（可编辑）
提供依赖管理和可视化的丰富任务追踪工具集合。

**详述**（可编辑）
Gemini CLI 提供了一套丰富的任务追踪器工具集，包括 tracker_create_task（创建任务）、tracker_update_task（更新任务）、tracker_get_task（获取任务详情）、tracker_list_tasks（列出所有任务）、tracker_add_dependency（添加任务依赖）和 tracker_visualize（可视化任务关系）。这些工具支持完整的任务生命周期管理，能够创建和更新任务状态，建立任务之间的依赖关系，并以可视化的方式展示任务进展和结构，从而实现对复杂任务的高效组织与追踪。
<!-- /kg:uuid=ede1828c-d611-5435-a7a0-a9a59984a766 -->

<!-- kg:uuid=f242f987-5180-5710-b924-2ff3d3e66436 tag=entity shared=false readonly-meta -->
## 保存记忆工具
- **归属**：核心工具集 / 记忆与持久化

**摘要**（可编辑）
跨会话持久化事实的遗留工具。

**详述**（可编辑）
在 Gemini CLI 中，`save_memory` 工具是一个遗留工具，用于当 `experimental.memoryV2` 设置为 `false` 时，跨会话持久化事实数据。
<!-- /kg:uuid=f242f987-5180-5710-b924-2ff3d3e66436 -->

<!-- kg:uuid=0cbfbcf8-1fb5-528b-b2e5-e8af2a99e1f4 tag=entity shared=false readonly-meta -->
## 内容搜索工具
- **归属**：核心工具集 / 搜索与信息检索

**摘要**（可编辑）
搜索文件内容。

**详述**（可编辑）
在 Gemini CLI 中，内容搜索工具对应 `grep_search` 工具，用于在文件中搜索匹配特定模式的内容，其技能请求动作为 'Search file contents'。
<!-- /kg:uuid=0cbfbcf8-1fb5-528b-b2e5-e8af2a99e1f4 -->

<!-- kg:uuid=372e8553-7229-5a4f-9720-e2ac59222593 tag=entity shared=false readonly-meta -->
## 内置文档查阅工具
- **归属**：核心工具集 / 搜索与信息检索

**摘要**（可编辑）
查阅Gemini CLI内置文档。

**详述**（可编辑）
在 Gemini CLI 中，内置文档查阅工具对应 `get_internal_docs` 工具，用于查找和获取 Gemini CLI 捆绑的内部文档。
<!-- /kg:uuid=372e8553-7229-5a4f-9720-e2ac59222593 -->

<!-- kg:uuid=955e2a96-ac25-5d4e-b04e-1b68fe23edfa tag=entity shared=false readonly-meta -->
## 写入文件工具
- **归属**：核心工具集 / 文件系统操作

**摘要**（可编辑）
创建新文件并写入内容。

**详述**（可编辑）
在 Gemini CLI 中，`write_file` 工具对应技能请求中的 'Create a new file' 动作，用于创建新文件并写入内容。
<!-- /kg:uuid=955e2a96-ac25-5d4e-b04e-1b68fe23edfa -->

<!-- kg:uuid=2e6689f8-10bc-5713-88d0-0c2b50d6bb31 tag=entity shared=false readonly-meta -->
## 列出MCP资源工具
- **归属**：核心工具集 / MCP集成

**摘要**（可编辑）
列出可用MCP资源。

**详述**（可编辑）
在 Gemini CLI 中，list_mcp_resources 工具用于列出所有通过 Model Context Protocol (MCP) 提供的可用资源，以便发现和访问这些资源。
<!-- /kg:uuid=2e6689f8-10bc-5713-88d0-0c2b50d6bb31 -->

<!-- kg:uuid=3958859c-5986-547e-b01f-3ee90a9b578b tag=entity shared=false readonly-meta -->
## 列出目录工具
- **归属**：核心工具集 / 文件系统操作

**摘要**（可编辑）
列出目录中的文件和子目录。

**详述**（可编辑）
在 Gemini CLI 中，`list_directory` 工具对应技能请求中的 'List files and subdirectories' 动作，用于列出指定目录下的文件和子目录列表。
<!-- /kg:uuid=3958859c-5986-547e-b01f-3ee90a9b578b -->

<!-- kg:uuid=0c7d2924-925f-58f6-876b-429fce527abe tag=entity shared=false readonly-meta -->
## 子代理完成工具
- **归属**：代理协作与任务管理 / 子代理调度

**摘要**（可编辑）
表明子代理完成并返回结果。

**详述**（可编辑）
子代理完成工具（complete_task）用于在子代理完成任务时向父代理发出完成信号，并返回执行结果，确保父子代理之间的任务状态同步和结果传递。
<!-- /kg:uuid=0c7d2924-925f-58f6-876b-429fce527abe -->

<!-- kg:uuid=b3b0ff5f-63b6-5625-ad1e-206b3a54a944 tag=concept shared=false readonly-meta -->
## 并行子代理调度
- **归属**：代理协作与任务管理 / 子代理调度

**摘要**（可编辑）
同时调度多个独立的子代理任务。

**详述**（可编辑）
并行子代理调度指在 Gemini CLI 中，在同一响应内同时发起多个独立的子代理任务。可通过单次响应中调用多个 invoke_agent，或在提示中多次使用 @generalist 语法实现。存在依赖关系的子代理任务必须顺序执行，但不应将原本独立的子代理任务强行串行化，以避免浪费并行执行的优势。
<!-- /kg:uuid=b3b0ff5f-63b6-5625-ad1e-206b3a54a944 -->

<!-- kg:uuid=f044857a-8453-5521-ac67-d704f10d4128 tag=entity shared=false readonly-meta -->
## 批量读取文件工具
- **归属**：核心工具集 / 文件系统操作

**摘要**（可编辑）
一次性读取多个文件内容。

**详述**（可编辑）
在 Gemini CLI 中，`read_many_files` 工具对应技能请求中的 'Read multiple files at once' 动作，用于一次性读取多个文件的内容。
<!-- /kg:uuid=f044857a-8453-5521-ac67-d704f10d4128 -->

<!-- kg:uuid=33a1d445-2cda-5665-9f71-9215f5eef491 tag=entity shared=false readonly-meta -->
## 技能存储目录
- **归属**：技能与配置管理 / 技能激活与存储

**摘要**（可编辑）
用户级技能的存储位置。

**详述**（可编辑）
用户级技能存储在两个目录中：默认位置 ~/.gemini/skills/ 和与 Codex、Copilot CLI 共享的跨运行时别名目录 ~/.agents/skills/。当两个目录在同一作用域内同时存在时，~/.agents/skills/ 具有优先权。每个技能以子目录形式组织，其中必须包含一个 SKILL.md 文件，该文件使用前置元数据定义技能的 name 和 description。
<!-- /kg:uuid=33a1d445-2cda-5665-9f71-9215f5eef491 -->

<!-- kg:uuid=e7ec99a9-55b9-5d63-8677-2a814d2a9ccf tag=concept shared=false readonly-meta -->
## 提示模板填充
- **归属**：代理协作与任务管理 / 子代理调度

**摘要**（可编辑）
调度子代理前替换提示模板中的占位符。

**详述**（可编辑）
提示模板填充是指在调度子代理前，将提示模板中的占位符替换为具体内容的过程。技能中的子代理调度动作可能引用外部提示模板文件（例如 superpowers:subagent-driven-development 的 ./implementer-prompt.md）或直接提供内联提示。在 Gemini CLI 调用 invoke_agent 之前，必须将模板中的所有占位符（如 {WHAT_WAS_IMPLEMENTED} 或 [FULL TEXT of task]）替换为具体内容，然后将完整提示传递给子代理。提示模板通常定义了代理的角色定位、评审标准及期望的输出格式，确保子代理按规范执行任务。
<!-- /kg:uuid=e7ec99a9-55b9-5d63-8677-2a814d2a9ccf -->

<!-- kg:uuid=386f78a7-1684-5a70-8e32-b7f81caff086 tag=entity shared=false readonly-meta -->
## 文件查找工具
- **归属**：核心工具集 / 文件系统操作

**摘要**（可编辑）
通过通配模式查找文件。

**详述**（可编辑）
在 Gemini CLI 中，`glob` 工具对应技能请求中的 'Find files by name' 动作，使用 glob 模式按名称查找文件。
<!-- /kg:uuid=386f78a7-1684-5a70-8e32-b7f81caff086 -->

<!-- kg:uuid=2fb34dbb-c998-53f7-9fca-bb90e6d7b8f5 tag=entity shared=false readonly-meta -->
## 更新主题工具
- **归属**：技能与配置管理 / 配置与元数据

**摘要**（可编辑）
更新当前对话的主题元数据。

**详述**（可编辑）
在 Gemini CLI 中，`update_topic` 工具用于更新当前对话的主题或战略意图元数据信息。
<!-- /kg:uuid=2fb34dbb-c998-53f7-9fca-bb90e6d7b8f5 -->

<!-- kg:uuid=4888eda3-c581-5f35-8405-9bf6414856fd tag=entity shared=false readonly-meta -->
## 激活技能工具
- **归属**：技能与配置管理 / 技能激活与存储

**摘要**（可编辑）
激活一个技能的工具。

**详述**（可编辑）
在 Gemini CLI 中，`activate_skill` 工具用于激活并执行一个已安装的技能，它对应于技能请求中的 'Invoke a skill' 动作。
<!-- /kg:uuid=4888eda3-c581-5f35-8405-9bf6414856fd -->

<!-- kg:uuid=c5b14da6-18b3-5d9e-9253-51f8c2bfc97e tag=entity shared=false readonly-meta -->
## 编辑文件工具
- **归属**：核心工具集 / 文件系统操作

**摘要**（可编辑）
编辑文件内容。

**详述**（可编辑）
在 Gemini CLI 中，`replace` 工具对应技能请求中的 'Edit a file' 动作，用于修改现有文件的内容。
<!-- /kg:uuid=c5b14da6-18b3-5d9e-9253-51f8c2bfc97e -->

<!-- kg:uuid=8a669388-5b02-5ec7-8996-738c5d14924e tag=entity shared=false readonly-meta -->
## 网页抓取工具
- **归属**：核心工具集 / 搜索与信息检索

**摘要**（可编辑）
获取URL内容。

**详述**（可编辑）
在 Gemini CLI 中，网页抓取工具对应 `web_fetch` 工具，用于获取指定 URL 的网络资源内容，其技能请求动作为 'Fetch a URL'。
<!-- /kg:uuid=8a669388-5b02-5ec7-8996-738c5d14924e -->

<!-- kg:uuid=5c5e11b8-c2aa-5aa2-a005-edf8fc96bdb3 tag=entity shared=false readonly-meta -->
## 询问用户工具
- **归属**：核心工具集 / 用户交互

**摘要**（可编辑）
向用户提出结构化问题。

**详述**（可编辑）
在 Gemini CLI 中，`ask_user` 工具用于向用户提出结构化的问题，支持文本输入、单选和多选三种交互形式。
<!-- /kg:uuid=5c5e11b8-c2aa-5aa2-a005-edf8fc96bdb3 -->

<!-- kg:uuid=4381c2bb-a72e-5a9e-ba21-4a269cec44f7 tag=entity shared=false readonly-meta -->
## 读取MCP资源工具
- **归属**：核心工具集 / MCP集成

**摘要**（可编辑）
读取MCP资源。

**详述**（可编辑）
在 Gemini CLI 中，read_mcp_resource 工具用于读取通过 Model Context Protocol (MCP) 提供的指定资源的内容。
<!-- /kg:uuid=4381c2bb-a72e-5a9e-ba21-4a269cec44f7 -->

<!-- kg:uuid=353fac31-2dbf-5bbc-b96d-a7cdb5ffcad7 tag=entity shared=false readonly-meta -->
## 读取文件工具
- **归属**：核心工具集 / 文件系统操作

**摘要**（可编辑）
读取单个文件内容。

**详述**（可编辑）
在 Gemini CLI 中，`read_file` 工具对应技能请求中的 'Read a file' 动作，用于读取单个指定文件的内容。
<!-- /kg:uuid=353fac31-2dbf-5bbc-b96d-a7cdb5ffcad7 -->

<!-- kg:uuid=59e1d4a8-358b-5546-8e31-65171b938b0e tag=entity shared=false readonly-meta -->
## 运行Shell命令工具
- **归属**：核心工具集 / 执行与环境交互

**摘要**（可编辑）
运行Shell命令。

**详述**（可编辑）
在 Gemini CLI 中，`run_shell_command` 工具对应技能请求中的 'Run a shell command' 动作，用于执行任意的 shell 命令。
<!-- /kg:uuid=59e1d4a8-358b-5546-8e31-65171b938b0e -->

<!-- kg:uuid=e732af64-12cb-56b8-b52c-c29588ddf755 tag=entity shared=false readonly-meta -->
## 进入计划模式工具
- **归属**：代理协作与任务管理 / 计划与工作流

**摘要**（可编辑）
进入只读计划模式。

**详述**（可编辑）
在 Gemini CLI 中，`enter_plan_mode` 工具用于切换到只读的计划模式，在此模式下不会修改文件。
<!-- /kg:uuid=e732af64-12cb-56b8-b52c-c29588ddf755 -->

<!-- kg:uuid=70467480-7d2a-5383-bc75-23a550eeae1c tag=entity shared=false readonly-meta -->
## 退出计划模式工具
- **归属**：代理协作与任务管理 / 计划与工作流

**摘要**（可编辑）
退出计划模式。

**详述**（可编辑）
在 Gemini CLI 中，`exit_plan_mode` 工具用于从只读计划模式中退出，恢复正常操作。
<!-- /kg:uuid=70467480-7d2a-5383-bc75-23a550eeae1c -->

<!-- kg:uuid=82c5c068-40b0-5e5f-aade-368ede57e32d tag=concept shared=false readonly-meta -->
## 通用子代理快捷方式
- **归属**：代理协作与任务管理 / 子代理调度

**摘要**（可编辑）
通过@generalist快速调度通用子代理。

**详述**（可编辑）
在 Gemini CLI 中，可通过 @generalist <prompt> 语法快捷调度通用子代理，该语法等价于调用 invoke_agent 工具并指定 agent_name: 'generalist'。此外，Gemini CLI 还内置了其他代理名称，如 cli_help（用于 CLI 帮助）、codebase_investigator（用于代码库调查），以及启用浏览器工具时提供的 browser_agent。
<!-- /kg:uuid=82c5c068-40b0-5e5f-aade-368ede57e32d -->

