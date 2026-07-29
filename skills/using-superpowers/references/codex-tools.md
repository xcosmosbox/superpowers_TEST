<!-- 本文档由领域知识层结构化生成。仅「摘要/详述」可编辑；其余为系统维护，请勿修改。 -->

<!-- kg:uuid=7c69f017-552a-5625-a62b-71131f53050f tag=concept shared=false readonly-meta -->
## Codex应用完成工作流
- **归属**：技能系统 / 技能工作流

**摘要**（可编辑）
沙箱环境下引导用户通过原生控件完成推送等工作流。

**详述**（可编辑）
Codex应用完成工作流是指在沙箱环境（例如处于分离头状态或外部管理工作树）阻止分支或推送操作时，代理会将所有工作提交并通知用户通过应用的原生控件完成后续流程。用户有两个选择：一是“创建分支”，即创建一个新分支（用户命名），然后借助应用UI提交、推送并创建PR；二是“转移到本地”，将当前工作转移到本地检出以便本地处理。在整个过程中，代理仍然能够运行测试、暂存文件，并输出建议的分支名称、提交消息和PR描述，供用户复制使用。
<!-- /kg:uuid=7c69f017-552a-5625-a62b-71131f53050f -->

<!-- kg:uuid=58145a4f-928b-5328-8140-25a215dd7682 tag=entity shared=false readonly-meta -->
## 多代理配置
- **归属**：子代理系统 / 子代理调度

**摘要**（可编辑）
启用多代理支持的配置项。

**详述**（可编辑）
在 Codex 配置文件 (~/.codex/config.toml) 中，通过设置 [features] 下的 multi_agent = true 来启用多代理支持。启用后，spawn_agent、wait_agent、close_agent 等工具可用于 dispatching-parallel-agents 和 subagent-driven-development 等技能。
<!-- /kg:uuid=58145a4f-928b-5328-8140-25a215dd7682 -->

<!-- kg:uuid=dc70fe9e-464e-50f5-9ca5-ab0f9e6a61db tag=concept shared=false readonly-meta -->
## 子代理调度规则
- **归属**：子代理系统 / 子代理调度

**摘要**（可编辑）
管理子代理审查与生命周期的一般规则。

**详述**（可编辑）
子代理调度规则用于管理子代理审查与实现生命周期。在 subagent-driven-development 方法中，审查子代理完成审查并返回结果后应立即关闭。
<!-- /kg:uuid=dc70fe9e-464e-50f5-9ca5-ab0f9e6a61db -->

