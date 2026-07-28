<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=91a32b0a-bdca-5683-9472-1a104e74f55b tag=entity shared=false readonly-meta -->
## Ask User 工具
- **归属**：配置与上下文 / 助手工具集

**摘要**（可编辑）
Gemini CLI 独有的工具，向用户提出结构化问题。

**详述**（可编辑）
ask_user 工具用于向用户提出结构化查询，支持文本输入、单选和多选等类型，以便在交互过程中获取明确的用户反馈或决策。
<!-- /kg:uuid=91a32b0a-bdca-5683-9472-1a104e74f55b -->

<!-- kg:uuid=8beb652f-8b58-5eed-a6df-73781cb8a631 tag=entity shared=false readonly-meta -->
## Browser Agent
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Gemini CLI 内置的子代理，在启用浏览器工具时可用，处理浏览器操作。

**详述**（可编辑）
browser_agent 是 Gemini CLI 的内置子代理名称，仅在浏览器工具被启用时可用。通过 invoke_agent 调用，用于执行网页浏览相关的自动化任务，例如获取网页内容、模拟用户交互等。
<!-- /kg:uuid=8beb652f-8b58-5eed-a6df-73781cb8a631 -->

<!-- kg:uuid=1c1f16d2-b511-50e0-97dc-13258b97c6b3 tag=entity shared=false readonly-meta -->
## CLI Help Agent
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Gemini CLI 内置的命令行帮助子代理。

**详述**（可编辑）
cli_help 是 Gemini CLI 的内置子代理名称，可通过 invoke_agent 工具调用，主要用于提供 CLI 相关的帮助信息，协助用户理解命令行工具的使用方法和参数。
<!-- /kg:uuid=1c1f16d2-b511-50e0-97dc-13258b97c6b3 -->

<!-- kg:uuid=484844eb-6b89-5174-abe4-1627a5fc6d7c tag=entity shared=false readonly-meta -->
## Codebase Investigator Agent
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Gemini CLI 内置的子代理，用于代码库调查。

**详述**（可编辑）
codebase_investigator 是 Gemini CLI 的内置子代理名称，可通过 invoke_agent 工具调用，专注于分析和探索代码库，帮助理解代码结构、依赖关系以及查找特定实现细节。
<!-- /kg:uuid=484844eb-6b89-5174-abe4-1627a5fc6d7c -->

<!-- kg:uuid=88d40a6f-7cde-5259-bdfe-7306b64f20d8 tag=entity shared=false readonly-meta -->
## Complete Task 工具
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Gemini CLI 独有工具，表示子代理完成并返回结果。

**详述**（可编辑）
complete_task 工具用于在 Gemini CLI 环境中，由子代理发出信号表明其任务已完成，并将结果返回给父代理。这对于协调多代理工作流至关重要，确保父代理能够正确获取子代理的执行结果。
<!-- /kg:uuid=88d40a6f-7cde-5259-bdfe-7306b64f20d8 -->

<!-- kg:uuid=ad82535a-ee3a-5916-910b-ceccd78eeffd tag=concept shared=false readonly-meta -->
## Create File 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Create a new file”映射到 write_file 工具。

**详述**（可编辑）
技能中创建新文件的指令在 Gemini CLI 上通过 write_file 工具执行，该工具负责在指定路径写入新文件内容。
<!-- /kg:uuid=ad82535a-ee3a-5916-910b-ceccd78eeffd -->

<!-- kg:uuid=e17ab4e3-4527-5aa7-9a04-ccef96139123 tag=concept shared=false readonly-meta -->
## Edit File 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Edit a file”映射到 replace 工具。

**详述**（可编辑）
当技能需要对现有文件进行编辑时，Gemini CLI 使用 replace 工具实现部分内容替换，完成文件的修改操作。
<!-- /kg:uuid=e17ab4e3-4527-5aa7-9a04-ccef96139123 -->

<!-- kg:uuid=e2f152a4-b2af-5c93-bea0-4044bbb24c34 tag=entity shared=false readonly-meta -->
## Enter Plan Mode 工具
- **归属**：配置与上下文 / 助手工具集

**摘要**（可编辑）
Gemini CLI 独有的工具，切换到只读计划模式。

**详述**（可编辑）
enter_plan_mode 工具允许 Gemini CLI 切换到计划模式，在此模式下系统处于只读状态，用于规划和分析而不执行修改操作。通常与 exit_plan_mode 搭配使用。
<!-- /kg:uuid=e2f152a4-b2af-5c93-bea0-4044bbb24c34 -->

<!-- kg:uuid=e91e8444-5653-5ca5-bba5-30c95ca9de29 tag=entity shared=false readonly-meta -->
## Exit Plan Mode 工具
- **归属**：配置与上下文 / 助手工具集

**摘要**（可编辑）
Gemini CLI 独有的工具，退出只读计划模式。

**详述**（可编辑）
exit_plan_mode 工具用于退出计划模式，使 Gemini CLI 恢复到可执行写操作的状态。它与 enter_plan_mode 工具配对，控制会话的读写能力切换。
<!-- /kg:uuid=e91e8444-5653-5ca5-bba5-30c95ca9de29 -->

<!-- kg:uuid=59479444-2629-5162-8e01-72d0cb361940 tag=concept shared=false readonly-meta -->
## Fetch URL 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Fetch a URL”映射到 web_fetch 工具。

**详述**（可编辑）
当技能需要获取一个 URL 的内容时，Gemini CLI 使用 web_fetch 工具执行 HTTP 请求，抓取并返回网页或资源内容。
<!-- /kg:uuid=59479444-2629-5162-8e01-72d0cb361940 -->

<!-- kg:uuid=0f41acf4-47b6-5b15-aa81-5655e205b29b tag=concept shared=false readonly-meta -->
## Find Files by Name 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Find files by name”映射到 glob 工具。

**详述**（可编辑）
技能中按名称模式查找文件的动作在 Gemini CLI 上通过 glob 工具执行，支持通配符模式匹配文件路径。
<!-- /kg:uuid=0f41acf4-47b6-5b15-aa81-5655e205b29b -->

<!-- kg:uuid=b0f8a44a-778e-53c4-a322-bbf1a33e2105 tag=concept shared=false readonly-meta -->
## GEMINI.md 分层加载
- **归属**：配置与上下文 / 环境配置

**摘要**（可编辑）
Gemini CLI 按全局、项目、子目录的层次加载 GEMINI.md 文件。

**详述**（可编辑）
Gemini CLI 采用层次化策略加载 GEMINI.md 文件：首先加载全局级别的 `~/.gemini/GEMINI.md`；然后加载项目级别，即工作区目录及其所有祖先目录中的 GEMINI.md；当工具访问特定子目录时，还会额外加载该子目录下的 GEMINI.md。这种机制使得不同粒度的指令和配置可以组合生效，提供灵活的个性化设置。
<!-- /kg:uuid=b0f8a44a-778e-53c4-a322-bbf1a33e2105 -->

<!-- kg:uuid=000814c4-947a-5129-8be2-12169895f61e tag=entity shared=false readonly-meta -->
## GEMINI.md 指令文件
- **归属**：配置与上下文 / 环境配置

**摘要**（可编辑）
Gemini CLI 的指令文件，包含个性化的行为配置。

**详述**（可编辑）
GEMINI.md 是 Gemini CLI 用于加载指令和个性化行为配置的文件。它采用分层加载方式：全局级别文件为 `~/.gemini/GEMINI.md`，项目级别位于工作区目录及其祖先目录中，此外当工具访问某个子目录时，也会加载该子目录下的 GEMINI.md。在技能文档中提及“your instructions file”时，在 Gemini CLI 上下文中即指 GEMINI.md。
<!-- /kg:uuid=000814c4-947a-5129-8be2-12169895f61e -->

<!-- kg:uuid=09d59216-e308-5bdd-acc5-1e483ea1ec0a tag=entity shared=false readonly-meta -->
## Generalist Agent
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
Gemini CLI 内置的通用子代理。

**详述**（可编辑）
generalist 是 Gemini CLI 的内置子代理名称之一，通过 invoke_agent 工具调用，也可通过 chat 语法 @generalist <prompt> 快捷分派。它被设计为处理通用任务，是技能分派的主要目标代理。
<!-- /kg:uuid=09d59216-e308-5bdd-acc5-1e483ea1ec0a -->

<!-- kg:uuid=ba1c41ac-87ce-5059-9a9a-135202f1ef50 tag=entity shared=false readonly-meta -->
## Get Internal Docs 工具
- **归属**：配置与上下文 / 助手工具集

**摘要**（可编辑）
Gemini CLI 独有的工具，用于查阅捆绑的内部文档。

**详述**（可编辑）
get_internal_docs 工具允许 Gemini CLI 查阅其自身捆绑的文档，为 CLI 的使用和配置提供内置帮助。
<!-- /kg:uuid=ba1c41ac-87ce-5059-9a9a-135202f1ef50 -->

<!-- kg:uuid=d102e92f-be6e-5a5d-b759-522e30fe0218 tag=concept shared=false readonly-meta -->
## Invoke Skill 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Invoke a skill”映射到 activate_skill 工具。

**详述**（可编辑）
当技能需要调用另一个已定义的技能时，Gemini CLI 将该请求映射到 activate_skill 工具，从而激活并执行目标技能。
<!-- /kg:uuid=d102e92f-be6e-5a5d-b759-522e30fe0218 -->

<!-- kg:uuid=2f47532d-b225-503d-a4cc-150dd1c927e6 tag=concept shared=false readonly-meta -->
## List Directory 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“List files and subdirectories”映射到 list_directory 工具。

**详述**（可编辑）
技能中列出目录下文件和子目录的请求在 Gemini CLI 中映射为 list_directory 工具调用，返回指定目录的内容列表。
<!-- /kg:uuid=2f47532d-b225-503d-a4cc-150dd1c927e6 -->

<!-- kg:uuid=fb6416ff-e4fa-5e13-bec5-aa2e265df5d4 tag=entity shared=false readonly-meta -->
## List MCP Resources 工具
- **归属**：配置与上下文 / MCP 资源访问

**摘要**（可编辑）
Gemini CLI 独有工具，用于列出可用的 MCP 资源。

**详述**（可编辑）
list_mcp_resources 是 Gemini CLI 独有的工具，用于列出当前可访问的 MCP 资源列表。它常与 read_mcp_resource 工具配合使用，以便发现和访问所需的外部数据源。
<!-- /kg:uuid=fb6416ff-e4fa-5e13-bec5-aa2e265df5d4 -->

<!-- kg:uuid=a2fd1c52-0ad8-54dd-bb86-baf6f0444345 tag=concept shared=false readonly-meta -->
## Read File 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Read a file”映射到 read_file 工具。

**详述**（可编辑）
在 Gemini CLI 环境中，当技能请求执行读取单个文件的操作时，该动作会被映射并调用底层工具 read_file，从而实现文件内容的读取。
<!-- /kg:uuid=a2fd1c52-0ad8-54dd-bb86-baf6f0444345 -->

<!-- kg:uuid=e84da447-2ee9-5cfd-a32b-0539b7c2d191 tag=entity shared=false readonly-meta -->
## Read MCP Resource 工具
- **归属**：配置与上下文 / MCP 资源访问

**摘要**（可编辑）
Gemini CLI 独有工具，用于读取 MCP 资源。

**详述**（可编辑）
read_mcp_resource 是 Gemini CLI 独有的工具，用于读取 MCP（Model Context Protocol）资源。它提供对 MCP 资源的直接读取访问能力，允许 Gemini CLI 集成外部数据源，从而在会话中利用这些资源。
<!-- /kg:uuid=e84da447-2ee9-5cfd-a32b-0539b7c2d191 -->

<!-- kg:uuid=d2317232-7bfa-5508-8037-909825bcc0aa tag=concept shared=false readonly-meta -->
## Read Multiple Files 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Read multiple files”映射到 read_many_files 工具。

**详述**（可编辑）
当技能需要一次读取多个文件时，Gemini CLI 将该请求映射到 read_many_files 工具，允许批量读取多个指定文件的内容，提高效率。
<!-- /kg:uuid=d2317232-7bfa-5508-8037-909825bcc0aa -->

<!-- kg:uuid=670e2be6-8181-5f12-9c12-0e45a1d21c45 tag=concept shared=false readonly-meta -->
## Run Shell Command 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Run a shell command”映射到 run_shell_command 工具。

**详述**（可编辑）
技能中执行 shell 命令的请求在 Gemini CLI 中通过 run_shell_command 工具实现，允许直接调用系统 shell 执行命令并获取输出。
<!-- /kg:uuid=670e2be6-8181-5f12-9c12-0e45a1d21c45 -->

<!-- kg:uuid=7107fd7e-ab69-5378-b259-c22e56e1f627 tag=entity shared=false readonly-meta -->
## Save Memory 工具
- **归属**：配置与上下文 / 助手工具集

**摘要**（可编辑）
Gemini CLI 独有的工具，用于跨会话持久化事实。

**详述**（可编辑）
save_memory 是一个遗留工具，当 `experimental.memoryV2` 设置为 false 时，它能够跨会话保存信息，以便后续会话可以回忆这些事实。
<!-- /kg:uuid=7107fd7e-ab69-5378-b259-c22e56e1f627 -->

<!-- kg:uuid=8dd09ae4-79dc-58cd-bcc9-a7853e5a5e31 tag=concept shared=false readonly-meta -->
## Search File Contents 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Search file contents”映射到 grep_search 工具。

**详述**（可编辑）
当技能需要根据内容模式搜索文件时，Gemini CLI 将请求映射到 grep_search 工具，用于在文件内容中进行正则或文本匹配搜索。
<!-- /kg:uuid=8dd09ae4-79dc-58cd-bcc9-a7853e5a5e31 -->

<!-- kg:uuid=6dd19fbb-34fa-5d42-b777-fd5e21d74e73 tag=concept shared=false readonly-meta -->
## Search Web 映射
- **归属**：技能动作映射 / 动作到工具映射

**摘要**（可编辑）
技能动作“Search the web”映射到 google_web_search 工具。

**详述**（可编辑）
技能中执行网络搜索的请求在 Gemini CLI 上通过 google_web_search 工具实现，利用 Google 搜索引擎返回相关结果。
<!-- /kg:uuid=6dd19fbb-34fa-5d42-b777-fd5e21d74e73 -->

<!-- kg:uuid=e6bb2f2a-cae1-5305-9601-b35073542add tag=entity shared=false readonly-meta -->
## Tracker Add Dependency 工具
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
Gemini CLI 的任务跟踪工具，用于添加任务依赖。

**详述**（可编辑）
tracker_add_dependency 工具允许在任务之间建立依赖关系，确保任务按正确顺序执行，增强任务规划能力。
<!-- /kg:uuid=e6bb2f2a-cae1-5305-9601-b35073542add -->

<!-- kg:uuid=0e175b1e-3ca4-50b0-8026-a1c59e19e315 tag=entity shared=false readonly-meta -->
## Tracker Create Task 工具
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
Gemini CLI 的任务跟踪工具，用于创建任务。

**详述**（可编辑）
tracker_create_task 是 Gemini CLI 提供的更丰富的任务跟踪系统的一部分，用于创建任务并可能包含依赖关系。与传统的 write_todos 相比，它提供了更高级的任务管理能力。
<!-- /kg:uuid=0e175b1e-3ca4-50b0-8026-a1c59e19e315 -->

<!-- kg:uuid=c68cce9b-a706-5de8-ac39-d27cc2c209bf tag=entity shared=false readonly-meta -->
## Tracker Get Task 工具
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
Gemini CLI 的任务跟踪工具，用于获取任务详情。

**详述**（可编辑）
tracker_get_task 工具用于检索特定任务的详细信息，支持查询任务的状态、属性等。
<!-- /kg:uuid=c68cce9b-a706-5de8-ac39-d27cc2c209bf -->

<!-- kg:uuid=bf7ce9eb-ea18-5ee2-97fa-85a32fa512a9 tag=entity shared=false readonly-meta -->
## Tracker List Tasks 工具
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
Gemini CLI 的任务跟踪工具，用于列出任务。

**详述**（可编辑）
tracker_list_tasks 工具提供列出所有任务或按条件过滤任务的功能，是任务跟踪系统的一部分。
<!-- /kg:uuid=bf7ce9eb-ea18-5ee2-97fa-85a32fa512a9 -->

<!-- kg:uuid=f78e39af-80a2-55f3-9521-c4951d8d1f50 tag=entity shared=false readonly-meta -->
## Tracker Update Task 工具
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
Gemini CLI 的任务跟踪工具，用于更新任务。

**详述**（可编辑）
tracker_update_task 工具允许更新已存在任务的属性，如状态、描述等，是增强的任务跟踪系统组件。
<!-- /kg:uuid=f78e39af-80a2-55f3-9521-c4951d8d1f50 -->

<!-- kg:uuid=b89e5902-1690-507b-8c48-fdf5de11e7a8 tag=entity shared=false readonly-meta -->
## Tracker Visualize 工具
- **归属**：任务跟踪 / 任务管理

**摘要**（可编辑）
Gemini CLI 的任务跟踪工具，用于可视化任务依赖关系。

**详述**（可编辑）
tracker_visualize 工具提供任务和依赖关系的图形化展示，帮助用户直观理解任务流和依赖结构。
<!-- /kg:uuid=b89e5902-1690-507b-8c48-fdf5de11e7a8 -->

<!-- kg:uuid=d7cfe44d-9485-5106-babc-8a856870c6f0 tag=entity shared=false readonly-meta -->
## Update Topic 工具
- **归属**：配置与上下文 / 助手工具集

**摘要**（可编辑）
Gemini CLI 独有的工具，更新当前会话的主题或策略意图元数据。

**详述**（可编辑）
update_topic 工具允许 Gemini CLI 动态更新当前对话的主题或 strategic-intent 元数据，以反映会话焦点或目标的变化。
<!-- /kg:uuid=d7cfe44d-9485-5106-babc-8a856870c6f0 -->

<!-- kg:uuid=b06f24cf-0ff3-59a6-adca-702abacb0d30 tag=entity shared=false readonly-meta -->
## ~/.agents/skills/ 技能目录
- **归属**：配置与上下文 / 环境配置

**摘要**（可编辑）
跨运行时别名技能目录，与 Gemini CLI、Codex 和 Copilot CLI 共享。

**详述**（可编辑）
`~/.agents/skills/` 是一个用户级技能目录，作为 `~/.gemini/skills/` 的跨运行时别名，与 Gemini CLI、Codex 和 Copilot CLI 共享使用。当 `~/.agents/skills/` 和 `~/.gemini/skills/` 在同一作用域同时存在时，该目录具有更高的优先级，优先被加载。
<!-- /kg:uuid=b06f24cf-0ff3-59a6-adca-702abacb0d30 -->

<!-- kg:uuid=c0237a02-abdd-5b49-ada0-e4817a9ba49e tag=entity shared=false readonly-meta -->
## ~/.gemini/skills/ 技能目录
- **归属**：配置与上下文 / 环境配置

**摘要**（可编辑）
Gemini CLI 的用户级技能目录。

**详述**（可编辑）
用户级技能存放于 `~/.gemini/skills/` 目录中。每个技能是一个独立的子目录，其中必须包含一个 `SKILL.md` 文件，该文件以 YAML 前置元数据提供 `name` 和 `description` 字段。该目录与 `~/.agents/skills/` 互为跨运行时别名，当两者在同一作用域内同时存在时，`~/.agents/skills/` 具有更高的优先级。
<!-- /kg:uuid=c0237a02-abdd-5b49-ada0-e4817a9ba49e -->

<!-- kg:uuid=5c73e6dc-f6d5-572e-982c-174e020e9cf3 shared=true mirror=true source=_shared/任务跟踪/node-b6d3b2fc.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/任务跟踪/node-b6d3b2fc.md` 维护，请勿在此编辑。
> **任务跟踪映射** — 将技能任务跟踪动作映射到 write_todos 工具。
<!-- /kg:uuid=5c73e6dc-f6d5-572e-982c-174e020e9cf3 -->

<!-- kg:uuid=888fce9a-00b5-5b0e-a95b-d1cdb11f4f3a tag=concept shared=false readonly-meta -->
## 子代理内联提示
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
当技能分派子代理时提供内联提示，可直接传递给 invoke_agent。

**详述**（可编辑）
如果技能未引用任何提示模板，而是直接在分派指令中提供了内联提示文本，那么在 Gemini CLI 中，可以直接将该内联文本作为 prompt 参数传递给 invoke_agent 工具，并指定 agent_name: "generalist"。这简化了无模板场景下的子代理调用流程。
<!-- /kg:uuid=888fce9a-00b5-5b0e-a95b-d1cdb11f4f3a -->

<!-- kg:uuid=4bc9b020-f88e-5fd8-902e-38c5fb637a28 shared=true mirror=true source=_shared/代理编排/node-441c4c1e.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/代理编排/node-441c4c1e.md` 维护，请勿在此编辑。
> **子代理分派映射** — 将技能动作“Dispatch a subagent”映射到 invoke_agent 工具。
<!-- /kg:uuid=4bc9b020-f88e-5fd8-902e-38c5fb637a28 -->

<!-- kg:uuid=8e8bde5e-f988-5eb1-81d5-a9a949386881 tag=concept shared=false readonly-meta -->
## 子代理提示模板（引用）
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
当技能分派子代理时引用提示模板文件，需填充模板后调用 invoke_agent。

**详述**（可编辑）
某些技能在分派子代理时会引用一个 *-prompt.md 模板文件（如 implementer-prompt.md、task-reviewer.md 等）。在 Gemini CLI 上，需要先依据上下文填充模板中的占位符，然后将完整提示作为 prompt 参数传递给 invoke_agent 工具，并指定 agent_name: "generalist" 来执行。例如，引用 superpowers:requesting-code-review 技能中的 ./code-reviewer.md 模板时，也需要填充后传递。
<!-- /kg:uuid=8e8bde5e-f988-5eb1-81d5-a9a949386881 -->

<!-- kg:uuid=8a5842a6-08bc-5df1-95fb-1beb6b10123d tag=concept shared=false readonly-meta -->
## 并行子代理分派
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
在同一响应中多次调用 invoke_agent 以并行运行子代理。

**详述**（可编辑）
当技能需要并行分发多个子代理时，Gemini CLI 支持在同一响应中发出多个 invoke_agent 调用，或在一次提示中使用多个 @generalist 调用。这些调用会并行执行独立的子代理任务，以提升效率。需要注意的是，必须保持具有依赖关系的任务的顺序性，不能为了简化历史而将必须顺序执行的子代理任务强制序列化。
<!-- /kg:uuid=8a5842a6-08bc-5df1-95fb-1beb6b10123d -->

<!-- kg:uuid=152a8bd1-eeb8-590c-84b1-4d303de1a402 tag=concept shared=false readonly-meta -->
## 技能目录优先级
- **归属**：配置与上下文 / 环境配置

**摘要**（可编辑）
当 ~/.gemini/skills/ 和 ~/.agents/skills/ 在同一作用域都存在时，~/.agents/skills/ 优先。

**详述**（可编辑）
用户级技能目录存在两个可能路径：`~/.gemini/skills/` 作为 Gemini CLI 专用目录，而 `~/.agents/skills/` 是跨运行时的别名目录，与 Codex 和 Copilot CLI 共享。当这两个目录在相同作用域内同时存在时，系统会优先采用 `~/.agents/skills/` 中的技能定义，以确保跨工具行为的一致性。
<!-- /kg:uuid=152a8bd1-eeb8-590c-84b1-4d303de1a402 -->

<!-- kg:uuid=8589bb69-e0a5-57a4-8c58-7c767cfb8fed tag=concept shared=false readonly-meta -->
## 提示模板占位符填充
- **归属**：代理编排 / 子代理执行

**摘要**（可编辑）
子代理提示模板中的占位符需在调用前填充实际值。

**详述**（可编辑）
技能提供的提示模板中包含占位符，例如 {WHAT_WAS_IMPLEMENTED} 或 [FULL TEXT of task]。在使用 invoke_agent 调用子代理之前，必须将所有占位符替换为具体的上下文值，以确保子代理获得完整且准确的任务描述。模板本身包含了代理的角色、评审标准和输出格式，子代理将严格遵循这些指令执行。
<!-- /kg:uuid=8589bb69-e0a5-57a4-8c58-7c767cfb8fed -->

