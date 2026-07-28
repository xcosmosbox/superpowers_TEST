<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=b06f24cf-0ff3-59a6-adca-702abacb0d30 tag=entity shared=false readonly-meta -->
## Agents 技能目录
- **归属**：技能系统 / 技能定义与加载

**摘要**（可编辑）
跨运行时技能别名目录。

**详述**（可编辑）
~/.agents/skills/ 是一个被多个运行时代理（如 Gemini CLI、Codex、Copilot CLI）共享使用的技能目录，它作为 ~/.gemini/skills/ 的别名而存在。当两个目录同时存在时，.agents/skills/ 具有更高的优先级，使得共享技能可以覆盖特定运行时的技能配置。
<!-- /kg:uuid=b06f24cf-0ff3-59a6-adca-702abacb0d30 -->

<!-- kg:uuid=b0f8a44a-778e-53c4-a322-bbf1a33e2105 tag=concept shared=false readonly-meta -->
## GEMINI.md 分层加载
- **归属**：技能系统 / 技能定义与加载

**摘要**（可编辑）
按全局、项目、子目录顺序分层加载指令文件的机制。

**详述**（可编辑）
GEMINI.md 分层加载机制允许指令文件从全局到局部逐层细化配置。全局文件位于 ~/.gemini/GEMINI.md，项目级文件在工作空间目录及其祖先目录中定义，子目录文件在工具访问相应目录时被加载。所有层级的指令会合并生效，从而提供灵活的配置粒度。
<!-- /kg:uuid=b0f8a44a-778e-53c4-a322-bbf1a33e2105 -->

<!-- kg:uuid=000814c4-947a-5129-8be2-12169895f61e tag=entity shared=false readonly-meta -->
## GEMINI.md 指令文件
- **归属**：技能系统 / 技能定义与加载

**摘要**（可编辑）
Gemini CLI 的指令文件。

**详述**（可编辑）
GEMINI.md 是 Gemini CLI 环境中使用的指令文件，在技能文档中常被称为“your instructions file”。Gemini CLI 通过加载 GEMINI.md 来获取用户的指令和配置，从而定制化自身的行为和响应。
<!-- /kg:uuid=000814c4-947a-5129-8be2-12169895f61e -->

<!-- kg:uuid=c0237a02-abdd-5b49-ada0-e4817a9ba49e tag=entity shared=false readonly-meta -->
## Gemini 用户技能目录
- **归属**：技能系统 / 技能定义与加载

**摘要**（可编辑）
用户级技能存放目录。

**详述**（可编辑）
~/.gemini/skills/ 是 Gemini CLI 的用户级技能文件系统路径，用于存放个人自定义技能。每个技能以子目录形式存放在该目录下，并且子目录内必须包含一个 SKILL.md 文件来定义该技能。
<!-- /kg:uuid=c0237a02-abdd-5b49-ada0-e4817a9ba49e -->

<!-- kg:uuid=20d777b3-f2ed-5adc-b09d-b63d083f85dd tag=entity shared=false readonly-meta -->
## MCP资源列表工具
- **归属**：平台集成 / MCP资源

**摘要**（可编辑）
列出可用MCP资源的工具。

**详述**（可编辑）
list_mcp_resources 工具从已配置的 MCP 服务中获取所有可用的资源列表。
<!-- /kg:uuid=20d777b3-f2ed-5adc-b09d-b63d083f85dd -->

<!-- kg:uuid=ead6b584-30ff-5acc-bfb4-f43e833bc898 tag=entity shared=false readonly-meta -->
## MCP资源读取工具
- **归属**：平台集成 / MCP资源

**摘要**（可编辑）
读取指定MCP资源的工具。

**详述**（可编辑）
read_mcp_resource 工具允许访问 MCP（Model Context Protocol）服务器提供的资源，并读取其内容。
<!-- /kg:uuid=ead6b584-30ff-5acc-bfb4-f43e833bc898 -->

<!-- kg:uuid=08dc076b-04b0-5867-9599-575f7111d1cc tag=entity shared=false readonly-meta -->
## Shell命令执行工具
- **归属**：开发环境工具 / Shell与命令执行

**摘要**（可编辑）
执行Shell命令的工具。

**详述**（可编辑）
run_shell_command 工具允许 Gemini CLI 执行任意的 Shell 命令，它对应于技能中定义的“Run a shell command”动作。通过该工具，可以调用系统命令来完成各类操作。
<!-- /kg:uuid=08dc076b-04b0-5867-9599-575f7111d1cc -->

<!-- kg:uuid=c3b573cd-8ecc-5881-8b18-607025494467 tag=entity shared=false readonly-meta -->
## URL获取工具
- **归属**：开发环境工具 / 网络访问

**摘要**（可编辑）
获取指定URL内容的工具。

**详述**（可编辑）
URL获取工具通过web_fetch功能向指定的URL发起获取请求并返回内容，实现“Fetch a URL”动作。它适用于访问网页、API等网络资源。
<!-- /kg:uuid=c3b573cd-8ecc-5881-8b18-607025494467 -->

<!-- kg:uuid=bc174deb-3de7-5154-84c7-450cc04e45b7 tag=entity shared=false readonly-meta -->
## write_todos 工具
- **归属**：任务管理 / 任务跟踪

**摘要**（可编辑）
Gemini CLI 中用于任务状态管理的工具。

**详述**（可编辑）
write_todos 是 Gemini CLI 提供的任务跟踪工具，专门用于管理待办事项的状态。支持的状态包括：pending（待处理）、in_progress（进行中）、completed（已完成）、cancelled（已取消）和 blocked（受阻）。在技能中，它对应“创建待办事项”和“标记完成”等任务跟踪操作，帮助保持任务列表的实时更新。
<!-- /kg:uuid=bc174deb-3de7-5154-84c7-450cc04e45b7 -->

<!-- kg:uuid=5390fc73-6479-5e6c-8bdc-ed0185551bd3 tag=entity shared=false readonly-meta -->
## 丰富任务跟踪器
- **归属**：任务管理 / 任务跟踪

**摘要**（可编辑）
一组提供创建、更新、获取、列出、依赖管理和可视化任务的功能的工具集。

**详述**（可编辑）
丰富任务跟踪器是一组功能完备的工具集，用于在 Gemini CLI 中进行全面的任务管理。具体包括：tracker_create_task 用于创建新任务；tracker_update_task 用于更新现有任务的信息（如状态或描述）；tracker_get_task 通过标识符查询特定任务的详细信息；tracker_list_tasks 用于获取任务列表，可能支持过滤和排序；tracker_add_dependency 用于在两个任务之间建立依赖关系，确保一个任务在另一个完成之前无法开始；tracker_visualize 以图形或文本图表形式展示任务及其依赖关系，辅助理解项目进度。这些工具共同提供了从创建到可视化的端到端任务跟踪能力。
<!-- /kg:uuid=5390fc73-6479-5e6c-8bdc-ed0185551bd3 -->

<!-- kg:uuid=8fe9c7e5-fb54-5df7-a056-bffea1e64588 tag=entity shared=false readonly-meta -->
## 会话主题更新工具
- **归属**：会话管理 / 会话状态

**摘要**（可编辑）
更新会话主题或战略意图元数据的工具。

**详述**（可编辑）
update_topic 工具用于修改当前对话的主题标签或战略意图元数据，帮助管理上下文感知。
<!-- /kg:uuid=8fe9c7e5-fb54-5df7-a056-bffea1e64588 -->

<!-- kg:uuid=f818edc4-46ad-5a21-9509-b9c2d4fa224f tag=entity shared=false readonly-meta -->
## 内容搜索工具
- **归属**：开发环境工具 / 文件系统操作

**摘要**（可编辑）
用于在文件内容中搜索模式匹配的工具。

**详述**（可编辑）
内容搜索工具用于在文件内容中搜索模式匹配。它通过 grep_search 工具提供基于 grep 的文本搜索功能，用于在文件中查找匹配的内容，实现了技能所请求的“Search file contents”动作。
<!-- /kg:uuid=f818edc4-46ad-5a21-9509-b9c2d4fa224f -->

<!-- kg:uuid=ec880575-37bf-5a06-b4d5-aeb1dcdd8c16 tag=entity shared=false readonly-meta -->
## 内部文档查找工具
- **归属**：会话管理 / 会话状态

**摘要**（可编辑）
查找捆绑文档的工具。

**详述**（可编辑）
get_internal_docs 工具用于访问 Gemini CLI 内置的帮助和参考文档，为使用者提供即时的内部文档查询能力。
<!-- /kg:uuid=ec880575-37bf-5a06-b4d5-aeb1dcdd8c16 -->

<!-- kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c shared=true mirror=true source=_shared/子代理管理/sub-agent-dispatch-tool.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/子代理管理/sub-agent-dispatch-tool.md` 维护，请勿在此编辑。
> **子代理分派工具** — 在不同平台中用于创建和分派子代理的工具集合。
<!-- /kg:uuid=dbbf80e6-85e1-5cce-b109-8a64e59f569c -->

<!-- kg:uuid=027fd4a0-fd47-562c-83bc-bd49cd79072e tag=entity shared=false readonly-meta -->
## 子代理完成信号工具
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
子代理向父代理发送完成信号并返回结果的工具。

**详述**（可编辑）
`complete_task` 是专供 Gemini 子代理使用的工具。当子代理完成分配的任务后，它调用此工具将结果返回给其父代理。
<!-- /kg:uuid=027fd4a0-fd47-562c-83bc-bd49cd79072e -->

<!-- kg:uuid=bf1d1eff-65b3-5381-b4e2-ef2231e65da5 tag=concept shared=false readonly-meta -->
## 子代理提示模板填充
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
将占位符替换为实际内容后传递给子代理的方法。

**详述**（可编辑）
许多技能包含提示模板文件（如 `implementer-prompt.md`），其中含有占位符（如 `{WHAT_WAS_IMPLEMENTED}` 或 `[FULL TEXT of task]`）。在调用子代理之前，必须使用实际值填充所有占位符，将完整的提示作为 `prompt` 参数传递给 `invoke_agent`。模板中已定义了子代理的角色、审查标准和输出格式，子代理会严格遵循这些指令执行任务。
<!-- /kg:uuid=bf1d1eff-65b3-5381-b4e2-ef2231e65da5 -->

<!-- kg:uuid=c22b1363-3750-560f-b58f-1e0b5ba2e243 tag=concept shared=false readonly-meta -->
## 子代理调度机制
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
通过 invoke_agent 或 @generalist 语法调度子代理的机制。

**详述**（可编辑）
在 Gemini CLI 中，当技能需要分派子代理时，通过 `invoke_agent` 工具调用实现，需传入 `agent_name`（如 `"generalist"`、`"cli_help"`、`"codebase_investigator"`、`"browser_agent"` 等）和构造好的提示。此外，Gemini CLI 还支持聊天快捷语法：在输入中直接使用 `@generalist <prompt>` 即可等效调度子代理。该机制涵盖了通用子代理和各种内置专用子代理的调度。
<!-- /kg:uuid=c22b1363-3750-560f-b58f-1e0b5ba2e243 -->

<!-- kg:uuid=d8c5758e-a69a-518a-a0cc-af864554632c tag=concept shared=false readonly-meta -->
## 并行子代理分派
- **归属**：子代理管理 / 代理调度与生命周期

**摘要**（可编辑）
在一次响应中并行调用多个子代理的能力。

**详述**（可编辑）
Gemini CLI 支持并行分派子代理：可以在同一个响应中发出多个 `invoke_agent` 调用，或者在单个提示中包含多个 `@generalist` 指令，从而同时运行独立的子代理任务。需要注意的是，有依赖关系的任务仍需按顺序执行，不应为了简化历史而将独立的子代理任务串行化。
<!-- /kg:uuid=d8c5758e-a69a-518a-a0cc-af864554632c -->

<!-- kg:uuid=9ba0cbd8-bbed-5712-a021-88535fd398a1 shared=true mirror=true source=_shared/技能系统/skill-action-mapping-rules.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/技能系统/skill-action-mapping-rules.md` 维护，请勿在此编辑。
> **技能动作映射规则** — 定义技能描述的动作如何解析为具体平台工具调用的规则。
<!-- /kg:uuid=9ba0cbd8-bbed-5712-a021-88535fd398a1 -->

<!-- kg:uuid=c2a9f170-4490-511e-a67f-a9af0416b8fd tag=entity shared=false readonly-meta -->
## 技能定义文件
- **归属**：技能系统 / 技能定义与加载

**摘要**（可编辑）
定义技能的 Markdown 文件，包含名称和描述。

**详述**（可编辑）
SKILL.md 是每个技能目录下的定义文件，它以 Markdown 格式编写，包含技能的元数据（name 和 description 前置属性）以及技能的具体内容。Gemini CLI 通过读取该文件来了解和使用技能，是技能被发现和执行的基础。
<!-- /kg:uuid=c2a9f170-4490-511e-a67f-a9af0416b8fd -->

<!-- kg:uuid=12455841-badc-5aac-bf57-295cb67c331b tag=concept shared=false readonly-meta -->
## 技能目录优先级规则
- **归属**：技能系统 / 技能定义与加载

**摘要**（可编辑）
.agents/skills/ 优先级高于 ~/.gemini/skills/ 的规则。

**详述**（可编辑）
Gemini CLI 默认使用 ~/.gemini/skills/ 作为用户级技能目录，但同时支持 ~/.agents/skills/ 作为跨运行时的别名目录。如果这两个目录在相同范围内同时存在，Gemini CLI 会优先使用 .agents/skills/，这意味着该目录中的共享技能可以覆盖特定于 Gemini CLI 的技能。
<!-- /kg:uuid=12455841-badc-5aac-bf57-295cb67c331b -->

<!-- kg:uuid=71194d8d-6243-589f-a207-41fea35e8940 tag=entity shared=false readonly-meta -->
## 技能调用工具
- **归属**：技能系统 / 技能定义与加载

**摘要**（可编辑）
用于调用另一个技能的工具。

**详述**（可编辑）
activate_skill 工具允许 Gemini CLI 加载并执行其他技能，对应技能中“Invoke a skill”动作。通过该工具，可以实现技能的模块化复用，从而在不同的上下文中灵活调用已有的技能功能。
<!-- /kg:uuid=71194d8d-6243-589f-a207-41fea35e8940 -->

<!-- kg:uuid=4dc2a7ab-e752-545f-84f1-f8e866ee2870 tag=entity shared=false readonly-meta -->
## 文件写入工具
- **归属**：开发环境工具 / 文件系统操作

**摘要**（可编辑）
用于创建新文件的工具。

**详述**（可编辑）
文件写入工具用于在 Gemini CLI 环境中创建新文件。它通过 write_file 工具实现：当技能需要“Create a new file”时，Gemini CLI 会调用此工具来实现文件创建。
<!-- /kg:uuid=4dc2a7ab-e752-545f-84f1-f8e866ee2870 -->

<!-- kg:uuid=22d90530-2c15-5153-8e8b-076ba1a79de2 tag=entity shared=false readonly-meta -->
## 文件查找工具
- **归属**：开发环境工具 / 文件系统操作

**摘要**（可编辑）
通过文件名模式查找文件的工具。

**详述**（可编辑）
文件查找工具通过文件名模式查找文件。它使用 glob 工具，根据提供的 glob 模式在文件系统中匹配文件名，实现“Find files by name”动作，常用于根据命名规则定位文件。
<!-- /kg:uuid=22d90530-2c15-5153-8e8b-076ba1a79de2 -->

<!-- kg:uuid=4ceba803-a7d2-51dd-9823-fbaf106e8b91 tag=entity shared=false readonly-meta -->
## 文件编辑工具
- **归属**：开发环境工具 / 文件系统操作

**摘要**（可编辑）
用于编辑已有文件的工具。

**详述**（可编辑）
文件编辑工具用于编辑已有文件。它通过 replace 工具实现：replace 是 Gemini CLI 的文件编辑工具，通过替换文件中的指定内容来实现编辑功能，对应技能请求的“Edit a file”动作。
<!-- /kg:uuid=4ceba803-a7d2-51dd-9823-fbaf106e8b91 -->

<!-- kg:uuid=f6b0feb6-df5c-5847-ae15-3df702c3984a tag=entity shared=false readonly-meta -->
## 文件读取工具
- **归属**：开发环境工具 / 文件系统操作

**摘要**（可编辑）
用于读取文件内容的工具，支持单个或多个文件。

**详述**（可编辑）
文件读取工具用于读取文件内容。它包含两个子工具：read_file 和 read_many_files。read_file 是 Gemini CLI 的基础文件读取工具，当技能发起“Read a file”动作请求时，Gemini CLI 将其解析为对该工具的调用，实现读取指定文件内容的功能。read_many_files 是批量文件读取工具，允许在一次调用中读取多个文件，对应技能请求的“Read multiple files at once”动作。
<!-- /kg:uuid=f6b0feb6-df5c-5847-ae15-3df702c3984a -->

<!-- kg:uuid=b88bc5e8-aada-5467-b9e9-5dd68de4894f tag=entity shared=false readonly-meta -->
## 用户提问工具
- **归属**：会话管理 / 会话状态

**摘要**（可编辑）
向用户提出结构化问题的工具。

**详述**（可编辑）
ask_user 工具允许 Gemini CLI 在交互过程中向用户提问，问题可以是文本输入、单选、多选等结构化形式，以便获取用户的直接输入。
<!-- /kg:uuid=b88bc5e8-aada-5467-b9e9-5dd68de4894f -->

<!-- kg:uuid=148e2610-a688-5ae5-9942-b1a417b8d197 tag=entity shared=false readonly-meta -->
## 目录列表工具
- **归属**：开发环境工具 / 文件系统操作

**摘要**（可编辑）
列出目录下文件和子目录的工具。

**详述**（可编辑）
目录列表工具用于列出目录下的文件和子目录。它通过 list_directory 工具获取指定目录下的文件和子目录列表，对应技能中的“List files and subdirectories”动作，提供目录遍历功能。
<!-- /kg:uuid=148e2610-a688-5ae5-9942-b1a417b8d197 -->

<!-- kg:uuid=4beeb4f1-a1d4-500e-9466-06c52c627a5f tag=entity shared=false readonly-meta -->
## 网页搜索工具
- **归属**：开发环境工具 / 网络访问

**摘要**（可编辑）
使用Google搜索网页的工具。

**详述**（可编辑）
网页搜索工具使用google_web_search工具通过Google搜索引擎查询网络内容，对应技能请求的“Search the web”动作。它返回搜索结果信息。
<!-- /kg:uuid=4beeb4f1-a1d4-500e-9466-06c52c627a5f -->

<!-- kg:uuid=219c7dcf-12ed-58f9-a823-7bddea3aaf55 tag=entity shared=false readonly-meta -->
## 规划模式管理
- **归属**：任务管理 / 规划模式

**摘要**（可编辑）
进入和退出只读规划模式的工具。

**详述**（可编辑）
规划模式管理提供进入和退出只读规划模式的工具。enter_plan_mode 工具将系统切换到只读的规划模式，在该模式下可以进行分析和规划，但不会执行修改操作。exit_plan_mode 工具使系统退出规划模式，恢复到可以正常执行操作的常规模式。
<!-- /kg:uuid=219c7dcf-12ed-58f9-a823-7bddea3aaf55 -->

<!-- kg:uuid=612010d1-3b18-546d-aa27-65ddcd3b1335 tag=entity shared=false readonly-meta -->
## 记忆保存工具
- **归属**：会话管理 / 会话状态

**摘要**（可编辑）
在会话间持久化事实的工具（遗留）。

**详述**（可编辑）
save_memory 是 Gemini CLI 的遗留工具，用于在用户会话之间保存事实信息，以供后续会话引用。该工具仅在配置 experimental.memoryV2 为 false 时有效。
<!-- /kg:uuid=612010d1-3b18-546d-aa27-65ddcd3b1335 -->

<!-- kg:uuid=e3988be1-41ac-5960-a2bc-b1c860076bb3 shared=true mirror=true source=_shared/子代理管理/predefined-sub-agent-types.md -->
> 🔒 **[共享镜像 · 只读]** 本内容由 `_shared/子代理管理/predefined-sub-agent-types.md` 维护，请勿在此编辑。
> **预定义子代理类型** — 平台内置或特定用途的子代理类型定义。
<!-- /kg:uuid=e3988be1-41ac-5960-a2bc-b1c860076bb3 -->

