<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=2b329f45-0fae-5627-81ee-b20ac9c7d113 tag=entity shared=true readonly-meta -->
## CLI配置与技能目录
- **归属**：多智能体开发与任务编排 / CLI环境与配置

**摘要**（可编辑）
包括Antigravity CLI工具、GEMINI.md指令文件以及Gemini和跨运行时技能目录。

**详述**（可编辑）
CLI环境下的核心配置与技能组织机制包括三部分：Antigravity CLI工具（简称为 agy），它是一个命令行工具，能够接收技能语言定义的动作描述（例如派遣子代理、创建待办事项等），并将这些描述解析为对应的底层工具调用，从而执行实际操作。Gemini CLI 使用名为 GEMINI.md 的指令文件，该文件按层级加载，以提供灵活的项目与用户配置：全局文件位于 ~/.gemini/GEMINI.md，项目级文件则位于工作空间目录及其所有祖先目录中，且当工具访问特定子目录中的文件时，还会额外加载该子目录下的 GEMINI.md。技能目录方面，存在两种路径：用户级技能存放在 ~/.gemini/skills/ 目录下，每个技能由一个独立的子目录构成，其中必须包含一个 SKILL.md 文件，该文件需具备 name 和 description 等前置元数据；同时，~/.agents/skills/ 作为一个跨运行时别名，与 Codex 和 Copilot CLI 共享，当 ~/.gemini/skills/ 与 ~/.agents/skills/ 同时存在时，系统会优先使用 .agents/skills/ 下的技能定义。
<!-- /kg:uuid=2b329f45-0fae-5627-81ee-b20ac9c7d113 -->

