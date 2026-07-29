<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=cc7a06b6-4d56-5021-9fe1-a9f0c13da6f2 tag=concept shared=false readonly-meta -->
## GEMINI.md加载机制
- **归属**：环境与配置 / 指令加载

**摘要**（可编辑）
层次化加载GEMINI.md指令文件的方法。

**详述**（可编辑）
在 Gemini CLI 中，当技能提到 'your instructions file' 时，指的是 GEMINI.md 文件。Gemini CLI 层次化地加载 GEMINI.md：全局文件位于 ~/.gemini/GEMINI.md，项目级文件存在于工作区目录及其祖先目录中，并且当工具访问子目录中的文件时，也会加载该子目录中的 GEMINI.md。
<!-- /kg:uuid=cc7a06b6-4d56-5021-9fe1-a9f0c13da6f2 -->

<!-- kg:uuid=2e6689f8-10bc-5713-88d0-0c2b50d6bb31 tag=entity shared=false readonly-meta -->
## MCP资源列表
- **归属**：MCP资源 / MCP资源工具

**摘要**（可编辑）
列出所有可用的MCP资源。

**详述**（可编辑）
list_mcp_resources 工具用于列出所有通过 Model Context Protocol (MCP) 提供的可用资源，通常在 Gemini CLI 中使用。
<!-- /kg:uuid=2e6689f8-10bc-5713-88d0-0c2b50d6bb31 -->

<!-- kg:uuid=4381c2bb-a72e-5a9e-ba21-4a269cec44f7 tag=entity shared=false readonly-meta -->
## MCP资源读取
- **归属**：MCP资源 / MCP资源工具

**摘要**（可编辑）
读取指定的MCP资源内容。

**详述**（可编辑）
read_mcp_resource 工具用于读取通过 Model Context Protocol (MCP) 提供的资源的详细内容，通常在 Gemini CLI 中使用。
<!-- /kg:uuid=4381c2bb-a72e-5a9e-ba21-4a269cec44f7 -->

<!-- kg:uuid=59e1d4a8-358b-5546-8e31-65171b938b0e tag=entity shared=false readonly-meta -->
## Shell执行
- **归属**：Agent核心能力 / 文件系统

**摘要**（可编辑）
运行任意 Shell 命令。

**详述**（可编辑）
提供运行任意 Shell 命令的能力。在 Gemini CLI 中，可以使用 run_shell_command 工具执行任意的 shell 命令。
<!-- /kg:uuid=59e1d4a8-358b-5546-8e31-65171b938b0e -->

<!-- kg:uuid=2fb34dbb-c998-53f7-9fca-bb90e6d7b8f5 tag=entity shared=false readonly-meta -->
## 主题更新
- **归属**：Agent核心能力 / 用户交互

**摘要**（可编辑）
更新当前对话的主题元数据。

**详述**（可编辑）
在 Gemini CLI 中，`update_topic` 工具用于更新当前对话的主题或战略意图元数据信息。
<!-- /kg:uuid=2fb34dbb-c998-53f7-9fca-bb90e6d7b8f5 -->

<!-- kg:uuid=56575c00-70fa-5594-8f1f-c6951a7659c0 tag=entity shared=false readonly-meta -->
## 任务列表
- **归属**：Agent核心能力 / 任务管理

**摘要**（可编辑）
创建和更新任务追踪列表。

**详述**（可编辑）
write_todos 工具用于在技能请求中执行任务跟踪，可创建和更新任务待办列表。它支持完整的任务生命周期管理，任务状态包括 pending（待处理）、in_progress（进行中）、completed（已完成）、cancelled（已取消）和 blocked（阻塞），确保任务跟踪清晰有序。
<!-- /kg:uuid=56575c00-70fa-5594-8f1f-c6951a7659c0 -->

<!-- kg:uuid=98c0729d-8a5a-5d7d-bbed-f6e3f8a8ceac shared=true mirror=true source=_shared/agent核心能力/task-tracking-concept.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/agent核心能力/task-tracking-concept.md` 维护，请勿在此编辑。
> **任务追踪概念** — 包含任务工件和任务追踪器工具集在内的任务跟踪核心概念。
<!-- /kg:uuid=98c0729d-8a5a-5d7d-bbed-f6e3f8a8ceac -->

<!-- kg:uuid=0cbfbcf8-1fb5-528b-b2e5-e8af2a99e1f4 tag=entity shared=false readonly-meta -->
## 内容搜索
- **归属**：Agent核心能力 / 文件系统

**摘要**（可编辑）
在文件内容中执行文本搜索。

**详述**（可编辑）
提供在文件内容中执行文本搜索的能力。在 Gemini CLI 中，可以使用 grep_search 工具在文件中搜索匹配特定模式的内容。
<!-- /kg:uuid=0cbfbcf8-1fb5-528b-b2e5-e8af2a99e1f4 -->

<!-- kg:uuid=372e8553-7229-5a4f-9720-e2ac59222593 tag=entity shared=false readonly-meta -->
## 内置文档查阅
- **归属**：Agent核心能力 / 信息检索

**摘要**（可编辑）
查阅 Gemini CLI 内置文档。

**详述**（可编辑）
查阅 Gemini CLI 内置文档。在 Gemini CLI 中，该能力由 `get_internal_docs` 工具实现，用于查找和获取 Gemini CLI 捆绑的内部文档。
<!-- /kg:uuid=372e8553-7229-5a4f-9720-e2ac59222593 -->

<!-- kg:uuid=0c7d2924-925f-58f6-876b-429fce527abe tag=entity shared=false readonly-meta -->
## 子代理完成工具
- **归属**：子代理系统 / 子代理调度

**摘要**（可编辑）
表示子代理已完成任务并返回结果。

**详述**（可编辑）
complete_task 工具用于在子代理完成任务时发出信号，并将结果返回给父代理。
<!-- /kg:uuid=0c7d2924-925f-58f6-876b-429fce527abe -->

<!-- kg:uuid=e05b5202-a73d-56fe-83bd-8e053c2fe242 shared=true mirror=true source=_shared/子代理系统/sub-agent-scheduling-concept.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/子代理系统/sub-agent-scheduling-concept.md` 维护，请勿在此编辑。
> **子代理调度概念** — 涵盖子代理调度工具、并行调度、提示模板填充和通用快捷方式的核心概念。
<!-- /kg:uuid=e05b5202-a73d-56fe-83bd-8e053c2fe242 -->

<!-- kg:uuid=33a1d445-2cda-5665-9f71-9215f5eef491 tag=entity shared=false readonly-meta -->
## 技能存储
- **归属**：技能系统 / 技能管理

**摘要**（可编辑）
用户级技能的存储目录。

**详述**（可编辑）
用户级技能存储在两个目录中：默认位置 ~/.gemini/skills/ 和与 Codex、Copilot CLI 共享的跨运行时别名目录 ~/.agents/skills/。当两个目录在同一作用域内同时存在时，~/.agents/skills/ 具有优先权。每个技能以子目录形式组织，其中必须包含一个 SKILL.md 文件，该文件使用前置元数据定义技能的 name 和 description。
<!-- /kg:uuid=33a1d445-2cda-5665-9f71-9215f5eef491 -->

<!-- kg:uuid=4888eda3-c581-5f35-8405-9bf6414856fd tag=entity shared=false readonly-meta -->
## 技能激活
- **归属**：技能系统 / 技能管理

**摘要**（可编辑）
激活指定技能的工具。

**详述**（可编辑）
在 Gemini CLI 中，`activate_skill` 工具用于激活并执行一个已安装的技能，它对应于技能请求中的 'Invoke a skill' 动作。
<!-- /kg:uuid=4888eda3-c581-5f35-8405-9bf6414856fd -->

<!-- kg:uuid=f242f987-5180-5710-b924-2ff3d3e66436 tag=entity shared=false readonly-meta -->
## 持久记忆
- **归属**：Agent核心能力 / 记忆与状态

**摘要**（可编辑）
将事实跨会话持久化存储。

**详述**（可编辑）
在 Gemini CLI 中，`save_memory` 工具是一个遗留工具，用于当 `experimental.memoryV2` 设置为 `false` 时，跨会话持久化事实数据。
<!-- /kg:uuid=f242f987-5180-5710-b924-2ff3d3e66436 -->

<!-- kg:uuid=970e496c-86df-5f8d-b645-7f5746a60b82 tag=entity shared=false readonly-meta -->
## 文件浏览
- **归属**：Agent核心能力 / 文件系统

**摘要**（可编辑）
列出目录内容或通过通配模式查找文件。

**详述**（可编辑）
提供列出目录内容或通过通配模式查找文件的能力。在 Gemini CLI 中，可以使用 list_directory 工具列出指定目录下的文件和子目录列表，也可以使用 glob 工具通过 glob 模式按名称查找文件。
<!-- /kg:uuid=970e496c-86df-5f8d-b645-7f5746a60b82 -->

<!-- kg:uuid=4f370efc-6215-5715-83a0-71d395dead68 tag=entity shared=false readonly-meta -->
## 文件编辑
- **归属**：Agent核心能力 / 文件系统

**摘要**（可编辑）
创建新文件或编辑现有文件内容。

**详述**（可编辑）
提供创建新文件或编辑现有文件内容的能力。在 Gemini CLI 中，可以使用 write_file 工具创建新文件并写入内容，也可以使用 replace 工具修改现有文件的内容。
<!-- /kg:uuid=4f370efc-6215-5715-83a0-71d395dead68 -->

<!-- kg:uuid=a25a69eb-0821-535c-a6be-e9e0ac297a1f tag=entity shared=false readonly-meta -->
## 文件读取
- **归属**：Agent核心能力 / 文件系统

**摘要**（可编辑）
提供读取单个或批量文件内容的能力。

**详述**（可编辑）
提供读取单个或批量文件内容的能力。在 Gemini CLI 中，可以使用 read_file 工具读取单个指定文件的内容，也可以使用 read_many_files 工具一次性读取多个文件的内容。
<!-- /kg:uuid=a25a69eb-0821-535c-a6be-e9e0ac297a1f -->

<!-- kg:uuid=5c5e11b8-c2aa-5aa2-a005-edf8fc96bdb3 tag=entity shared=false readonly-meta -->
## 用户询问
- **归属**：Agent核心能力 / 用户交互

**摘要**（可编辑）
向用户提出结构化问题并收集回答。

**详述**（可编辑）
在 Gemini CLI 中，`ask_user` 工具用于向用户提出结构化的问题，支持文本输入、单选和多选三种交互形式。
<!-- /kg:uuid=5c5e11b8-c2aa-5aa2-a005-edf8fc96bdb3 -->

<!-- kg:uuid=9de6724b-a0f0-580a-8040-e75e7d75cf71 tag=entity shared=false readonly-meta -->
## 网络搜索
- **归属**：Agent核心能力 / 信息检索

**摘要**（可编辑）
通过 Google 执行网络搜索。

**详述**（可编辑）
通过 Google 执行网络搜索。在 Gemini CLI 中，该能力由 `google_web_search` 工具实现，对应技能请求中的 'Search the web' 动作，用于执行 Google 网络搜索。
<!-- /kg:uuid=9de6724b-a0f0-580a-8040-e75e7d75cf71 -->

<!-- kg:uuid=8a669388-5b02-5ec7-8996-738c5d14924e tag=entity shared=false readonly-meta -->
## 网页抓取
- **归属**：Agent核心能力 / 信息检索

**摘要**（可编辑）
获取指定 URL 的网页内容。

**详述**（可编辑）
获取指定 URL 的网页内容。在 Gemini CLI 中，该能力由 `web_fetch` 工具实现，对应技能请求中的 'Fetch a URL' 动作，用于获取指定 URL 的网络资源内容。
<!-- /kg:uuid=8a669388-5b02-5ec7-8996-738c5d14924e -->

<!-- kg:uuid=ac27160d-74b0-5e31-885d-c63440c2421b tag=entity shared=false readonly-meta -->
## 计划模式控制工具
- **归属**：计划模式 / 计划模式控制

**摘要**（可编辑）
提供进入和退出只读计划模式的能力。

**详述**（可编辑）
计划模式控制工具提供了在 Gemini CLI 中进入和退出只读计划模式的能力。它包含两个具体操作：一是 `enter_plan_mode`，用于切换到只读的计划模式，此模式下不会修改任何文件；二是 `exit_plan_mode`，用于从只读计划模式中退出，恢复正常操作状态。
<!-- /kg:uuid=ac27160d-74b0-5e31-885d-c63440c2421b -->

