# project-skeletonization

[Chinese](README.zh-CN.md)

Convert a complete business project into a reusable base skeleton, starter, or template.

## Use Cases

- Turn a legacy business project into a general-purpose base framework.
- Keep common capabilities such as authentication, routing, layout, and deployment while removing specific business features.
- Require the agent to confirm keep/remove boundaries with the user before destructive changes.

## Triggers

In AI tools that support skills, trigger this skill with natural language such as:

- "Turn this project into a skeleton."
- "Remove business features and keep the base framework."
- "Convert this Spring Boot project into a starter."

Some platforms may also support explicit triggers:

- `$project-skeletonization`
- `/project-skeletonization`

## Capabilities

1. **Project inventory**: inspect frontend, backend, database, deployment, tests, and documents.
2. **Module classification**: classify modules as keep, remove, or needs confirmation.
3. **Collaborative transformation**: output a plan and wait for user confirmation before destructive changes.
4. **Placeholder verification**: add a minimal placeholder page, API, or command so the skeleton can start, build, and prove the integration path works.

## Example

```text
User: Convert this e-commerce admin project into a reusable base skeleton.

Agent:
1. Inspect the project structure: Vue frontend, Spring Boot backend, MySQL, and Docker.
2. List what to keep: login, route guards, unified response, exception handling, Docker deployment.
3. List what to remove: product management, order management, payment APIs, and other business modules.
4. List uncertain items: audit logs, file uploads, scheduled tasks.
5. Wait for user confirmation.
6. Apply the confirmed transformation and verify the result.
```

## Supported Stacks

Spring Boot / Java, Node.js / TypeScript, Python with Django / FastAPI / Flask, and Vue / React frontend projects.

## Notes

- The agent must receive written user confirmation for the keep/remove plan before transformation.
- Uncertain modules are not deleted without confirmation.
- After transformation, the agent runs build, test, startup, or equivalent verification and reports the result.
