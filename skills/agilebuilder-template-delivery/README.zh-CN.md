# agilebuilder-template-delivery

[English](README.md)

优先使用 AgileBuilder MCP 进行模板化项目创建和文档优先的代码实现。

## 适用场景

- 需要新建项目、应用原型、代码仓库或脚手架；
- 在已接入 AgileBuilder 的工作空间中编写、重构、调试或扩展代码；
- 希望 AI 在动手前先读取 AgileBuilder 的策略、指南和项目文档约束。

## 触发方式

在支持 skills 的 AI 工具中，可用自然语言触发：

- “帮我创建一个 Spring Boot 项目”
- “按 AgileBuilder 模板初始化一个 React 仓库”
- “在这个仓库里重构用户模块，先读一下 AgileBuilder 的文档”

部分平台也支持显式触发：

- `$agilebuilder-template-delivery`
- `/agilebuilder-template-delivery`

## 主要能力

1. **项目创建**：优先调用 AgileBuilder `listTemplates`，从模板创建项目，而非手工脚手架；
2. **文档优先编码**：在编码、重构、调试前读取 AgileBuilder Agent Policy、Usage Guide 和 Document Catalog；
3. **约束对齐**：将用户请求与 AgileBuilder 文档约束进行 reconcile，冲突时显式提示用户。

## 使用示例

### 示例 1：创建新项目

```text
用户：帮我创建一个前后端分离的管理后台项目。

AI：
1. 读取 agilebuilder://usage/agent-policy
2. 调用 listTemplates 查找候选模板
3. 在存在歧义时查看候选模板详情并让用户确认
4. 使用选中的模板创建项目到指定绝对路径
```

### 示例 2：在现有项目中修改代码

```text
用户：把登录接口改成 JWT + Redis 会话。

AI：
1. 读取 agent-policy、guide 和 catalog
2. 查找与认证、技术栈相关的项目文档
3. 按文档约束实现修改
```

## 前置条件

- AgileBuilder MCP server 已配置并可用；
- 如需读取项目级文档，当前工作空间应接入 AgileBuilder 空间；如果没有项目文档，仍会读取 AgileBuilder 系统策略和指南。

## 注意事项

- 如果模板无法满足用户指定的技术栈，AI 会说明原因后再进行手工脚手架；
- 当用户请求与 AgileBuilder 文档冲突时，AI 会显式列出冲突，由用户决策。
