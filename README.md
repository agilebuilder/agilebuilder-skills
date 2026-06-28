# AgileBuilder Skills

[Chinese](README.zh-CN.md)

This repository contains AI Agent Skills for the AgileBuilder ecosystem. These skills help agents create projects from templates, follow AgileBuilder delivery constraints, and transform existing business projects into reusable starter skeletons.

## Usage

Configure the repository's `skills/` directory in an AI Agent tool that supports Skills. Each subdirectory is an independent skill, and each skill uses `SKILL.md` as its entry file.

## Prerequisites

- `agilebuilder-template-delivery` requires AgileBuilder MCP to be enabled in the active agent environment.
- The agent should be able to read AgileBuilder MCP resources such as `agilebuilder://usage/agent-policy`, `agilebuilder://usage/guide`, and `agilebuilder://docs/catalog`.
- If AgileBuilder MCP is unavailable, the relevant skill should clearly tell the user why, then continue only with the parts that can be completed under local repository constraints.

## Included Skills

| Skill | Description | Typical Triggers |
|---|---|---|
| [`agilebuilder-template-delivery`](skills/agilebuilder-template-delivery) | Prefer AgileBuilder MCP templates for project creation, and read AgileBuilder document constraints before coding. | "Create a Spring Boot project", "Initialize a repository from an AgileBuilder template" |
| [`project-skeletonization`](skills/project-skeletonization) | Convert a full business project into a reusable starter skeleton while keeping common capabilities and removing business features. | "Turn this project into a skeleton", "Remove business features and keep the base framework" |

## Contributing

This repository is English-first. `SKILL.md` files are written in English, `README.md` is the primary English documentation, and `README.zh-CN.md` is the Chinese documentation. Update both README files when skill behavior or user-facing guidance changes. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Release Checklist

See [RELEASE_CHECKLIST.md](RELEASE_CHECKLIST.md).

## License

MIT. See [LICENSE](LICENSE).
