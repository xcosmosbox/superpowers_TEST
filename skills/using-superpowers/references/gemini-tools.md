<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=cc7a06b6-4d56-5021-9fe1-a9f0c13da6f2 tag=concept shared=false readonly-meta -->
## GEMINI.md加载机制
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
层次化加载GEMINI.md指令文件的方法。

**详述**（可编辑）
在 Gemini CLI 中，当技能提到 'your instructions file' 时，指代的是 GEMINI.md 文件。Gemini CLI 层次化地加载 GEMINI.md：全局文件位于 ~/.gemini/GEMINI.md，项目级文件存在于工作区目录及其祖先目录中，并且当工具访问子目录中的文件时，也会加载该子目录中的 GEMINI.md。
<!-- /kg:uuid=cc7a06b6-4d56-5021-9fe1-a9f0c13da6f2 -->

<!-- kg:uuid=254b4302-834a-5548-bba8-8f4e899da220 tag=entity shared=false readonly-meta -->
## activate_skill工具
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
激活一个技能的工具。

**详述**（可编辑）
在 Gemini CLI 中，`activate_skill` 工具用于激活并执行一个已安装的技能，它对应于技能请求中的 'Invoke a skill' 动作。
<!-- /kg:uuid=254b4302-834a-5548-bba8-8f4e899da220 -->

<!-- kg:uuid=005bc38e-9595-5fcf-87f6-32d35a2f1922 tag=entity shared=false readonly-meta -->
## ask_user工具
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
向用户提出结构化问题的工具。

**详述**（可编辑）
在 Gemini CLI 中，`ask_user` 工具用于向用户提出结构化的问题，支持文本输入、单选和多选三种交互形式。
<!-- /kg:uuid=005bc38e-9595-5fcf-87f6-32d35a2f1922 -->

<!-- kg:uuid=5e7bd950-fa28-50c8-ae76-55b6bf661a1a tag=entity shared=false readonly-meta -->
## complete_task工具
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
表明子代理完成并返回结果的工具。

**详述**（可编辑）
在 Gemini CLI 中，`complete_task` 工具用于在子代理完成任务时发出信号，并将结果返回给父代理。
<!-- /kg:uuid=5e7bd950-fa28-50c8-ae76-55b6bf661a1a -->

<!-- kg:uuid=9a69a2d8-c5a7-5405-abbe-8260ef3f5267 tag=entity shared=false readonly-meta -->
## enter_plan_mode工具
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
进入只读计划模式的工具。

**详述**（可编辑）
在 Gemini CLI 中，`enter_plan_mode` 工具用于切换到只读的计划模式，在此模式下不会修改文件。
<!-- /kg:uuid=9a69a2d8-c5a7-5405-abbe-8260ef3f5267 -->

<!-- kg:uuid=b321daf8-9c2c-5f1c-81e6-d3c0d5849860 tag=entity shared=false readonly-meta -->
## exit_plan_mode工具
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
退出计划模式的工具。

**详述**（可编辑）
在 Gemini CLI 中，`exit_plan_mode` 工具用于从只读计划模式中退出，恢复正常操作。
<!-- /kg:uuid=b321daf8-9c2c-5f1c-81e6-d3c0d5849860 -->

<!-- kg:uuid=73460a5e-e7fe-519c-8b4e-346ef71257be tag=entity shared=false readonly-meta -->
## get_internal_docs工具
- **归属**：对话式AI代理基础设施 / 外部信息访问

**摘要**（可编辑）
查阅Gemini CLI内置文档的工具。

**详述**（可编辑）
在 Gemini CLI 中，`get_internal_docs` 工具用于查找和获取 Gemini CLI 捆绑的内部文档。
<!-- /kg:uuid=73460a5e-e7fe-519c-8b4e-346ef71257be -->

<!-- kg:uuid=834c6a64-5d5d-5517-a48b-da48560c2299 tag=entity shared=false readonly-meta -->
## glob工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
通过通配模式查找文件的工具。

**详述**（可编辑）
在 Gemini CLI 中，`glob` 工具对应技能请求中的 'Find files by name' 动作，使用 glob 模式按名称查找文件。
<!-- /kg:uuid=834c6a64-5d5d-5517-a48b-da48560c2299 -->

<!-- kg:uuid=1dd03498-9603-5b25-9b0f-0b9f5700eaeb tag=entity shared=false readonly-meta -->
## google_web_search工具
- **归属**：对话式AI代理基础设施 / 外部信息访问

**摘要**（可编辑）
执行Google网络搜索的工具。

**详述**（可编辑）
在 Gemini CLI 中，`google_web_search` 工具对应技能请求中的 'Search the web' 动作，用于执行 Google 网络搜索。
<!-- /kg:uuid=1dd03498-9603-5b25-9b0f-0b9f5700eaeb -->

<!-- kg:uuid=c6cf6bba-2c05-5575-86af-6a197b7173be tag=entity shared=false readonly-meta -->
## grep_search工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
搜索文件内容的工具。

**详述**（可编辑）
在 Gemini CLI 中，`grep_search` 工具对应技能请求中的 'Search file contents' 动作，用于在文件中搜索匹配特定模式的内容。
<!-- /kg:uuid=c6cf6bba-2c05-5575-86af-6a197b7173be -->

<!-- kg:uuid=f0352815-9824-5bc7-bbcf-08d82f9b7713 tag=entity shared=false readonly-meta -->
## list_directory工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
列出目录中文件和子目录的工具。

**详述**（可编辑）
在 Gemini CLI 中，`list_directory` 工具对应技能请求中的 'List files and subdirectories' 动作，用于列出指定目录下的文件和子目录列表。
<!-- /kg:uuid=f0352815-9824-5bc7-bbcf-08d82f9b7713 -->

<!-- kg:uuid=9c176b80-b9b7-52c9-8b27-5dc96dbd76de tag=entity shared=false readonly-meta -->
## list_mcp_resources工具
- **归属**：对话式AI代理基础设施 / 外部信息访问

**摘要**（可编辑）
列出可用MCP资源的工具。

**详述**（可编辑）
在 Gemini CLI 中，`list_mcp_resources` 工具用于列出所有通过 Model Context Protocol (MCP) 提供的可用资源。
<!-- /kg:uuid=9c176b80-b9b7-52c9-8b27-5dc96dbd76de -->

<!-- kg:uuid=0207d31f-739a-547b-8845-c9d0b67dfa1d tag=entity shared=false readonly-meta -->
## read_file工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
读取单个文件的工具。

**详述**（可编辑）
在 Gemini CLI 中，`read_file` 工具对应技能请求中的 'Read a file' 动作，用于读取单个指定文件的内容。
<!-- /kg:uuid=0207d31f-739a-547b-8845-c9d0b67dfa1d -->

<!-- kg:uuid=c77570a2-180a-5c6c-8623-a529e99202fd tag=entity shared=false readonly-meta -->
## read_many_files工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
一次性读取多个文件的工具。

**详述**（可编辑）
在 Gemini CLI 中，`read_many_files` 工具对应技能请求中的 'Read multiple files at once' 动作，用于一次性读取多个文件的内容。
<!-- /kg:uuid=c77570a2-180a-5c6c-8623-a529e99202fd -->

<!-- kg:uuid=46134c70-f37f-54bb-b34f-8742a65b610d tag=entity shared=false readonly-meta -->
## read_mcp_resource工具
- **归属**：对话式AI代理基础设施 / 外部信息访问

**摘要**（可编辑）
读取MCP资源的工具。

**详述**（可编辑）
在 Gemini CLI 中，`read_mcp_resource` 工具用于读取通过 Model Context Protocol (MCP) 提供的资源。
<!-- /kg:uuid=46134c70-f37f-54bb-b34f-8742a65b610d -->

<!-- kg:uuid=a7a1fa53-000a-5812-aa05-c9ee3ce7dfc2 tag=entity shared=false readonly-meta -->
## replace工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
编辑文件内容的工具。

**详述**（可编辑）
在 Gemini CLI 中，`replace` 工具对应技能请求中的 'Edit a file' 动作，用于修改现有文件的内容。
<!-- /kg:uuid=a7a1fa53-000a-5812-aa05-c9ee3ce7dfc2 -->

<!-- kg:uuid=fe22b237-61aa-55a1-9722-2c9b040c38df tag=entity shared=false readonly-meta -->
## run_shell_command工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
运行Shell命令的工具。

**详述**（可编辑）
在 Gemini CLI 中，`run_shell_command` 工具对应技能请求中的 'Run a shell command' 动作，用于执行任意的 shell 命令。
<!-- /kg:uuid=fe22b237-61aa-55a1-9722-2c9b040c38df -->

<!-- kg:uuid=b8f17c35-3620-56d4-9c9d-554fdd1577e5 tag=entity shared=false readonly-meta -->
## save_memory工具
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
跨会话持久化事实的遗留工具。

**详述**（可编辑）
在 Gemini CLI 中，`save_memory` 工具是一个遗留工具，用于当 `experimental.memoryV2` 设置为 `false` 时，跨会话持久化事实数据。
<!-- /kg:uuid=b8f17c35-3620-56d4-9c9d-554fdd1577e5 -->

<!-- kg:uuid=bbb51b6a-820b-5234-811f-d44b2cb3a9ce tag=entity shared=false readonly-meta -->
## update_topic工具
- **归属**：对话式AI代理基础设施 / 对话会话管理

**摘要**（可编辑）
更新当前对话的主题元数据的工具。

**详述**（可编辑）
在 Gemini CLI 中，`update_topic` 工具用于更新当前对话的主题或战略意图元数据信息。
<!-- /kg:uuid=bbb51b6a-820b-5234-811f-d44b2cb3a9ce -->

<!-- kg:uuid=9737423a-34cf-5e61-818d-a5204ab35e10 tag=entity shared=false readonly-meta -->
## web_fetch工具
- **归属**：对话式AI代理基础设施 / 外部信息访问

**摘要**（可编辑）
获取URL内容的工具。

**详述**（可编辑）
在 Gemini CLI 中，`web_fetch` 工具对应技能请求中的 'Fetch a URL' 动作，用于获取指定 URL 的网络资源内容。
<!-- /kg:uuid=9737423a-34cf-5e61-818d-a5204ab35e10 -->

<!-- kg:uuid=fefead5d-b1c4-55dd-9808-39b45cad3854 tag=entity shared=false readonly-meta -->
## write_file工具
- **归属**：对话式AI代理基础设施 / 文件系统与Shell操作

**摘要**（可编辑）
创建新文件并写入内容的工具。

**详述**（可编辑）
在 Gemini CLI 中，`write_file` 工具对应技能请求中的 'Create a new file' 动作，用于创建新文件并写入内容。
<!-- /kg:uuid=fefead5d-b1c4-55dd-9808-39b45cad3854 -->

<!-- kg:uuid=67e3eea8-78d9-52ed-bd99-3a6b23c544a5 tag=entity shared=false readonly-meta -->
## write_todos工具
- **归属**：对话式AI代理基础设施 / 任务追踪

**摘要**（可编辑）
创建和更新任务追踪列表的工具。

**详述**（可编辑）
write_todos 工具用于在技能请求中执行 'Task tracking' 动作，创建和更新任务待办列表。它支持多种任务状态，包括 pending（待处理）、in_progress（进行中）、completed（已完成）、cancelled（已取消）和 blocked（阻塞），从而管理任务生命周期，确保任务跟踪清晰有序。
<!-- /kg:uuid=67e3eea8-78d9-52ed-bd99-3a6b23c544a5 -->

<!-- kg:uuid=ede1828c-d611-5435-a7a0-a9a59984a766 tag=concept shared=false readonly-meta -->
## 任务追踪器工具集
- **归属**：对话式AI代理基础设施 / 任务追踪

**摘要**（可编辑）
提供依赖管理和可视化的丰富任务追踪工具集合。

**详述**（可编辑）
Gemini CLI 提供了一套丰富的任务追踪器工具集，包括 tracker_create_task（创建任务）、tracker_update_task（更新任务）、tracker_get_task（获取任务详情）、tracker_list_tasks（列出所有任务）、tracker_add_dependency（添加任务依赖）和 tracker_visualize（可视化任务关系）。这些工具支持完整的任务生命周期管理，能够创建和更新任务状态，建立任务之间的依赖关系，并以可视化的方式展示任务进展和结构，从而实现对复杂任务的高效组织与追踪。
<!-- /kg:uuid=ede1828c-d611-5435-a7a0-a9a59984a766 -->

<!-- kg:uuid=b3b0ff5f-63b6-5625-ad1e-206b3a54a944 tag=concept shared=false readonly-meta -->
## 并行子代理调度
- **归属**：对话式AI代理基础设施 / 子代理调度

**摘要**（可编辑）
同时调度多个独立的子代理任务。

**详述**（可编辑）
在 Gemini CLI 中，并行子代理调度指在同一响应中同时调度多个独立的子代理任务。可通过在一条响应中发出多个 invoke_agent 调用，或在提示中多次使用 @generalist 语法来完成。相互存在依赖关系的子代理任务必须保持顺序执行，但不应为了简化对话历史而将原本相互独立的子代理任务强行串行化，从而浪费并行执行的优势。
<!-- /kg:uuid=b3b0ff5f-63b6-5625-ad1e-206b3a54a944 -->

<!-- kg:uuid=33a1d445-2cda-5665-9f71-9215f5eef491 tag=entity shared=false readonly-meta -->
## 技能存储目录
- **归属**：对话式AI代理基础设施 / 技能与工作流

**摘要**（可编辑）
用户级技能的存储位置。

**详述**（可编辑）
用户级技能存储在 ~/.gemini/skills/ 目录下。此外，还有一个与 Codex 和 Copilot CLI 共享的跨运行时别名目录 ~/.agents/skills/。当两个目录在同一作用域内同时存在时，~/.agents/skills/ 具有优先权。每个技能以子目录形式组织，其中必须包含一个 SKILL.md 文件，该文件使用前置元数据定义技能的 name 和 description。
<!-- /kg:uuid=33a1d445-2cda-5665-9f71-9215f5eef491 -->

<!-- kg:uuid=e7ec99a9-55b9-5d63-8677-2a814d2a9ccf tag=concept shared=false readonly-meta -->
## 提示模板填充
- **归属**：对话式AI代理基础设施 / 子代理调度

**摘要**（可编辑）
调度子代理前替换提示模板中的占位符。

**详述**（可编辑）
提示模板填充是指在调度子代理前，将提示模板中的占位符替换为具体内容。技能中的子代理调度动作可能引用外部提示模板文件（例如 superpowers:subagent-driven-development 的 ./implementer-prompt.md），或者直接提供内联提示。在 Gemini CLI 上，实际调用 invoke_agent 之前，必须将模板中的所有占位符（例如 {WHAT_WAS_IMPLEMENTED} 或 [FULL TEXT of task]）替换为具体内容，然后将填充完整的提示传递给子代理。提示模板本身通常定义了代理的角色定位、评审标准以及期望的输出格式，确保子代理能够按照预定规范执行任务。
<!-- /kg:uuid=e7ec99a9-55b9-5d63-8677-2a814d2a9ccf -->

<!-- kg:uuid=82c5c068-40b0-5e5f-aade-368ede57e32d tag=concept shared=false readonly-meta -->
## 通用子代理快捷方式
- **归属**：对话式AI代理基础设施 / 子代理调度

**摘要**（可编辑）
通过@generalist快速调度通用子代理。

**详述**（可编辑）
在 Gemini CLI 中，可以通过 @generalist <prompt> 语法快捷调度通用子代理，此操作完全等价于调用 invoke_agent 工具并指定 agent_name: 'generalist'。除了 generalist 外，Gemini CLI 还内置了其他代理名称，如 cli_help（用于 CLI 帮助）和 codebase_investigator（用于代码库调查），以及在启用浏览器工具时提供的 browser_agent。
<!-- /kg:uuid=82c5c068-40b0-5e5f-aade-368ede57e32d -->

