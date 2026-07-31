<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=895990cb-952f-57a2-8c4c-37e7e72241b4 tag=entity shared=false readonly-meta -->
## MCP资源列表
- **归属**：系统交互与核心工具 / MCP资源集成

**摘要**（可编辑）
列出所有可用的MCP资源

**详述**（可编辑）
列出所有通过Model Context Protocol (MCP)提供的可用资源，该功能由Gemini CLI中的list_mcp_resources工具实现。
<!-- /kg:uuid=895990cb-952f-57a2-8c4c-37e7e72241b4 -->

<!-- kg:uuid=cdade8db-2154-5f75-a75b-acee19ec19a5 tag=entity shared=false readonly-meta -->
## MCP资源读取
- **归属**：系统交互与核心工具 / MCP资源集成

**摘要**（可编辑）
读取指定的MCP资源内容

**详述**（可编辑）
读取指定的通过Model Context Protocol (MCP)提供的资源的详细内容，该功能通过Gemini CLI中的read_mcp_resource工具完成。
<!-- /kg:uuid=cdade8db-2154-5f75-a75b-acee19ec19a5 -->

<!-- kg:uuid=b6c3be06-c596-5ac6-a198-fded64e45e44 tag=entity shared=false readonly-meta -->
## Shell执行
- **归属**：系统交互与核心工具 / 命令行执行

**摘要**（可编辑）
运行任意Shell命令

**详述**（可编辑）
Shell执行能力允许用户运行任意Shell命令，该功能通过Gemini CLI中的run_shell_command工具实现。
<!-- /kg:uuid=b6c3be06-c596-5ac6-a198-fded64e45e44 -->

<!-- kg:uuid=4caa028b-fba8-509b-9f83-6d076ae60596 tag=entity shared=false readonly-meta -->
## 主题更新
- **归属**：系统交互与核心工具 / 会话状态

**摘要**（可编辑）
更新当前对话的主题元数据

**详述**（可编辑）
主题更新是指通过 Gemini CLI 中的 update_topic 工具，更新当前对话的主题或战略意图元数据信息。
<!-- /kg:uuid=4caa028b-fba8-509b-9f83-6d076ae60596 -->

<!-- kg:uuid=6ae54133-86c1-5208-9e93-098f4e7f37c1 tag=entity shared=false readonly-meta -->
## 任务列表
- **归属**：代理编排与智能工作流 / 任务与计划管理

**摘要**（可编辑）
创建和更新任务追踪列表

**详述**（可编辑）
任务列表是一个用于追踪任务的核心实体，通过 write_todos 工具进行创建和更新。它支持完整的任务生命周期管理，包括任务的创建、状态变更和列表维护，确保任务待办事项的清晰跟踪与高效管理。
<!-- /kg:uuid=6ae54133-86c1-5208-9e93-098f4e7f37c1 -->

<!-- kg:uuid=b087b64a-4df8-56a1-aae1-4c1e22a3c273 tag=concept shared=false readonly-meta -->
## 任务追踪概念
- **归属**：代理编排与智能工作流 / 任务与计划管理

**摘要**（可编辑）
任务跟踪的核心概念，包含任务工件和任务追踪器工具集

**详述**（可编辑）
任务追踪概念是任务跟踪功能的核心设计抽象，它涵盖了任务工件（例如任务列表）和任务追踪器工具集。该概念实现了任务的创建、状态更新和完整的生命周期管理，为任务跟踪机制提供了一致且可扩展的整体框架。
<!-- /kg:uuid=b087b64a-4df8-56a1-aae1-4c1e22a3c273 -->

<!-- kg:uuid=0fc9307b-2a8b-5e16-8d9d-643ef5e58067 tag=entity shared=false readonly-meta -->
## 内容搜索
- **归属**：系统交互与核心工具 / 文件系统操作

**摘要**（可编辑）
在文件内容中执行文本搜索

**详述**（可编辑）
内容搜索能力允许在文件内容中执行文本搜索。在 Gemini CLI 中，可以使用 grep_search 工具在文件中搜索匹配特定模式的内容。
<!-- /kg:uuid=0fc9307b-2a8b-5e16-8d9d-643ef5e58067 -->

<!-- kg:uuid=91b73421-43dd-5fcd-b95b-48808c522255 tag=entity shared=false readonly-meta -->
## 内置文档查阅
- **归属**：系统交互与核心工具 / 帮助与文档

**摘要**（可编辑）
查阅Gemini CLI内置文档

**详述**（可编辑）
查阅Gemini CLI内置文档，使用`get_internal_docs`工具查找和获取捆绑的内部文档。
<!-- /kg:uuid=91b73421-43dd-5fcd-b95b-48808c522255 -->

<!-- kg:uuid=0c7d2924-925f-58f6-876b-429fce527abe tag=entity shared=false readonly-meta -->
## 子代理完成工具
- **归属**：代理编排与智能工作流 / 子代理与技能

**摘要**（可编辑）
表示子代理已完成任务并返回结果

**详述**（可编辑）
子代理完成工具（complete_task）用于当子代理完成其分配的任务时，向父代理发出完成信号，并将执行结果返回给父代理。该工具负责终结子代理的执行流程，并将产出无缝传递回父代理的上下文中。
<!-- /kg:uuid=0c7d2924-925f-58f6-876b-429fce527abe -->

<!-- kg:uuid=3e94ca73-6887-5102-9e05-971998aa1c96 tag=concept shared=false readonly-meta -->
## 子代理调度
- **归属**：代理编排与智能工作流 / 子代理与技能

**摘要**（可编辑）
子代理调度的核心概念与规则

**详述**（可编辑）
子代理调度是 Gemini CLI 中关于子代理任务调度、并行执行、提示模板填充和通用快捷方式的核心概念与规则，涵盖子代理调度工具以及相关的调度策略。它定义了如何高效协调多个子代理的执行顺序、资源分配与结果汇合，以实现复杂的多步骤任务自动化。
<!-- /kg:uuid=3e94ca73-6887-5102-9e05-971998aa1c96 -->

<!-- kg:uuid=19c8f290-b8eb-5581-8118-5227dc3f97fb shared=true mirror=true source=_shared/代理编排与智能工作流/hierarchical-instruction-file-loading.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/代理编排与智能工作流/hierarchical-instruction-file-loading.md` 维护，请勿在此编辑。
> **层次化指令文件加载机制** — 按优先级从全局、项目到子目录逐层合并指令文件内容的加载机制
<!-- /kg:uuid=19c8f290-b8eb-5581-8118-5227dc3f97fb -->

<!-- kg:uuid=dad4cdba-1f70-5352-890c-76d14ecf2ce5 tag=entity shared=false readonly-meta -->
## 技能存储
- **归属**：代理编排与智能工作流 / 子代理与技能

**摘要**（可编辑）
用户级技能的存储目录

**详述**（可编辑）
用户级技能存储在两个目录中：默认位置 `~/.gemini/skills/` 和与 Codex、Copilot CLI 共享的跨运行时别名目录 `~/.agents/skills/`。当两个目录在同一作用域内同时存在时，`~/.agents/skills/` 具有优先权。每个技能以子目录形式组织，其中必须包含一个 `SKILL.md` 文件，该文件使用前置元数据定义技能的 `name` 和 `description`。
<!-- /kg:uuid=dad4cdba-1f70-5352-890c-76d14ecf2ce5 -->

<!-- kg:uuid=70d30298-1e84-5b0a-ab9f-87323d13ebcc tag=entity shared=false readonly-meta -->
## 技能激活
- **归属**：代理编排与智能工作流 / 子代理与技能

**摘要**（可编辑）
激活指定技能

**详述**（可编辑）
在 Gemini CLI 中，`activate_skill` 工具用于激活并执行一个已安装的技能，它对应于技能请求中的“Invoke a skill”动作。该工具负责加载技能定义并触发其对应的功能实现。
<!-- /kg:uuid=70d30298-1e84-5b0a-ab9f-87323d13ebcc -->

<!-- kg:uuid=d8e14887-48be-5882-9b81-9d01c4783133 tag=entity shared=false readonly-meta -->
## 持久记忆
- **归属**：系统交互与核心工具 / 会话状态

**摘要**（可编辑）
将事实跨会话持久化存储

**详述**（可编辑）
在 Gemini CLI 中，`save_memory` 是一个遗留工具，用于在 `experimental.memoryV2` 被设置为 `false` 时跨会话持久化存储事实数据。
<!-- /kg:uuid=d8e14887-48be-5882-9b81-9d01c4783133 -->

<!-- kg:uuid=12a21afc-f5f6-5161-8334-78682108dfd3 tag=entity shared=false readonly-meta -->
## 文件浏览
- **归属**：系统交互与核心工具 / 文件系统操作

**摘要**（可编辑）
列出目录内容或使用通配模式查找文件

**详述**（可编辑）
文件浏览能力允许列出目录内容或通过通配模式查找文件。在 Gemini CLI 中，可以使用 list_directory 工具列出指定目录下的文件和子目录列表，也可以使用 glob 工具通过 glob 模式按名称查找文件。
<!-- /kg:uuid=12a21afc-f5f6-5161-8334-78682108dfd3 -->

<!-- kg:uuid=0fd1f1a4-e2ed-5ad4-a6e4-a31aa8282409 tag=entity shared=false readonly-meta -->
## 文件编辑
- **归属**：系统交互与核心工具 / 文件系统操作

**摘要**（可编辑）
创建新文件或编辑现有文件内容

**详述**（可编辑）
文件编辑能力允许创建新文件或编辑现有文件内容。在 Gemini CLI 中，可以使用 write_file 工具创建新文件并写入内容，也可以使用 replace 工具修改现有文件的内容。
<!-- /kg:uuid=0fd1f1a4-e2ed-5ad4-a6e4-a31aa8282409 -->

<!-- kg:uuid=039a773e-f06a-5259-8306-2bcbcef49723 tag=entity shared=false readonly-meta -->
## 文件读取
- **归属**：系统交互与核心工具 / 文件系统操作

**摘要**（可编辑）
读取单个或多个文件的内容

**详述**（可编辑）
文件读取能力允许读取单个或多个文件的内容。在 Gemini CLI 中，可以使用 read_file 工具读取单个指定文件的内容，也可以使用 read_many_files 工具一次性读取多个文件的内容。
<!-- /kg:uuid=039a773e-f06a-5259-8306-2bcbcef49723 -->

<!-- kg:uuid=9a5c8f4c-9f83-5d19-8aa5-e058d560fba0 tag=entity shared=false readonly-meta -->
## 用户询问
- **归属**：系统交互与核心工具 / 用户交互

**摘要**（可编辑）
向用户提出结构化问题并收集回答

**详述**（可编辑）
向用户提出结构化问题并收集回答。支持文本输入、单选和多选三种交互形式。该功能通过Gemini CLI中的ask_user工具实现。
<!-- /kg:uuid=9a5c8f4c-9f83-5d19-8aa5-e058d560fba0 -->

<!-- kg:uuid=4f479c89-cccd-519a-987c-3f26d13e9bac tag=entity shared=false readonly-meta -->
## 网络搜索
- **归属**：系统交互与核心工具 / 网络访问

**摘要**（可编辑）
通过Google执行网络搜索

**详述**（可编辑）
通过 Google 执行网络搜索。在 Gemini CLI 中，该能力由 `google_web_search` 工具实现，对应技能请求中的 'Search the web' 动作，用于执行 Google 网络搜索。
<!-- /kg:uuid=4f479c89-cccd-519a-987c-3f26d13e9bac -->

<!-- kg:uuid=424ce2fb-bbb5-528c-8e9a-41b39dd93d94 tag=entity shared=false readonly-meta -->
## 网页抓取
- **归属**：系统交互与核心工具 / 网络访问

**摘要**（可编辑）
获取指定URL的网页内容

**详述**（可编辑）
获取指定 URL 的网页内容。在 Gemini CLI 中，该能力由 `web_fetch` 工具实现，对应技能请求中的 'Fetch a URL' 动作，用于获取指定 URL 的网络资源内容。
<!-- /kg:uuid=424ce2fb-bbb5-528c-8e9a-41b39dd93d94 -->

<!-- kg:uuid=d1871017-e8c0-57c1-952e-799111e00958 tag=entity shared=false readonly-meta -->
## 计划模式控制
- **归属**：代理编排与智能工作流 / 任务与计划管理

**摘要**（可编辑）
进入和退出只读计划模式

**详述**（可编辑）
计划模式控制工具提供了在 Gemini CLI 中切换只读计划模式的能力。使用 enter_plan_mode 操作可进入只读计划模式，该模式下不会对任何文件进行修改，便于安全地查阅和规划；使用 exit_plan_mode 操作可从只读计划模式退出，恢复正常操作状态，允许对文件进行修改。
<!-- /kg:uuid=d1871017-e8c0-57c1-952e-799111e00958 -->

