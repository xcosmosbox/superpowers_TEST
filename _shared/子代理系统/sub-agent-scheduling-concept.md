<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=e05b5202-a73d-56fe-83bd-8e053c2fe242 tag=concept shared=true readonly-meta -->
## 子代理调度概念
- **归属**：子代理系统 / 子代理调度

**摘要**（可编辑）
涵盖子代理调度工具、并行调度、提示模板填充和通用快捷方式的核心概念。

**详述**（可编辑）
子代理调度工具是用于调度子代理执行任务的工具，涵盖多种实现和变体，以支持不同的子代理调度场景。在 Gemini CLI 中，并行子代理调度指在同一响应中同时调度多个独立的子代理任务，可以通过在一条响应中发出多个 invoke_agent 调用，或在提示中多次使用 @generalist 语法来实现。相互存在依赖关系的子代理任务必须保持顺序执行；但不应为了简化对话历史而将原本相互独立的子代理任务强行串行化，从而浪费并行执行的优势。提示模板填充是指在调度子代理前，将提示模板中的占位符替换为具体内容。技能中的子代理调度动作可能引用外部提示模板文件（例如 superpowers:subagent-driven-development 的 ./implementer-prompt.md），或直接提供内联提示。在 Gemini CLI 中调用 invoke_agent 之前，必须将模板中的所有占位符（如 {WHAT_WAS_IMPLEMENTED} 或 [FULL TEXT of task]）替换为具体内容，然后将填充完整的提示传递给子代理。提示模板通常定义了代理的角色定位、评审标准及期望的输出格式，确保子代理按规范执行任务。此外，在 Gemini CLI 中，可以通过 @generalist <prompt> 语法快捷调度通用子代理，等价于调用 invoke_agent 工具并指定 agent_name: 'generalist'。Gemini CLI 还内置了其他代理名称，如 cli_help（用于 CLI 帮助）、codebase_investigator（用于代码库调查），以及启用浏览器工具时提供的 browser_agent。
<!-- /kg:uuid=e05b5202-a73d-56fe-83bd-8e053c2fe242 -->

