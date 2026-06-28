# AgileBuilder Skills

本仓库收录与AgileBuilder产品相关的 AI Agent Skills，用于增强 AI 在 AgileBuilder 生态下的项目创建、模板交付与项目改造能力。

## 使用方式

将本仓库中的 `skills/` 目录配置到支持 Skills 的 AI Agent 工具中。每个子目录都是一个独立 Skill，入口文件统一为 `SKILL.md`。

## 前置条件

- 使用 `agilebuilder-template-delivery` 前，需要先在当前 Agent 环境中启用 AgileBuilder MCP。
- Agent 应能读取 AgileBuilder MCP 暴露的 `agilebuilder://usage/agent-policy`、`agilebuilder://usage/guide`、`agilebuilder://docs/catalog` 等资源。
- 如果 AgileBuilder MCP 不可用，相关 Skill 应明确告知用户原因，再按本地仓库约束继续处理可完成的部分。

## 包含的 Skills

| Skill | 说明 | 典型触发语 |
|---|---|---|
| [`agilebuilder-template-delivery`](skills/agilebuilder-template-delivery) | 优先使用 AgileBuilder MCP 模板创建项目，并在编码前读取 AgileBuilder 文档约束 | "帮我创建一个 Spring Boot 项目"、"按 AgileBuilder 模板初始化仓库" |
| [`project-skeletonization`](skills/project-skeletonization) | 将完整业务项目改造为可复用的基础项目骨架，保留通用能力、删除业务功能 | "把这个项目改成 skeleton"、"去掉业务功能保留基础框架" |

## 发布前检查

见 [RELEASE_CHECKLIST.md](RELEASE_CHECKLIST.md)。

## License

MIT. See [LICENSE](LICENSE).
