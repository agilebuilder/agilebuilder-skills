# agilebuilder-template-delivery

[Chinese](README.zh-CN.md)

Use AgileBuilder MCP first for template-based project creation and document-first implementation.

## Use Cases

- Create a new project, application prototype, repository, or scaffold.
- Write, refactor, debug, or extend code in a workspace connected to AgileBuilder.
- Make the agent read AgileBuilder policies, guides, and project document constraints before implementation.

## Triggers

In AI tools that support skills, trigger this skill with natural language such as:

- "Create a Spring Boot project."
- "Initialize a React repository from an AgileBuilder template."
- "Refactor the user module in this repository, and read the AgileBuilder documents first."

Some platforms may also support explicit triggers:

- `$agilebuilder-template-delivery`
- `/agilebuilder-template-delivery`

## Capabilities

1. **Project creation**: call AgileBuilder `listTemplates` first and create projects from templates instead of hand-written scaffolding.
2. **Document-first coding**: read AgileBuilder Agent Policy, Usage Guide, and Document Catalog before coding, refactoring, or debugging.
3. **Constraint reconciliation**: reconcile user requests with AgileBuilder document constraints and surface conflicts explicitly.

## Examples

### Create a new project

```text
User: Create a full-stack admin project.

Agent:
1. Read agilebuilder://usage/agent-policy.
2. Call listTemplates to discover candidate templates.
3. Review candidate template details and ask for confirmation when ambiguous.
4. Create the project from the selected template at an absolute target path.
```

### Modify an existing project

```text
User: Change the login API to JWT plus Redis sessions.

Agent:
1. Read agent-policy, guide, and catalog.
2. Find project documents related to authentication and the technology stack.
3. Implement the change according to the documented constraints.
```

## Prerequisites

- AgileBuilder MCP server is configured and available.
- If project-level documents are needed, the current workspace should be connected to an AgileBuilder space. If no project documents exist, the agent still reads AgileBuilder system policy and guide.

## Notes

- If no template can satisfy the requested stack, the agent explains why before using manual scaffolding.
- If the user request conflicts with AgileBuilder documents, the agent lists the conflict explicitly and lets the user decide.
