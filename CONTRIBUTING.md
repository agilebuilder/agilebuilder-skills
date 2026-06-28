# Contributing

This repository is maintained as an English-first public skill collection.

## Documentation Rules

- `SKILL.md` must be written in English.
- `README.md` is the primary English documentation.
- `README.zh-CN.md` is the Chinese documentation.
- When adding or updating a skill, update both `README.md` and `README.zh-CN.md` when user-facing behavior, prerequisites, examples, or safety notes change.
- Keep the English and Chinese README files equivalent in meaning. The English version is the source of truth when wording differs.
- Use UTF-8 for all Markdown files.

## Skill Rules

- Keep each skill in its own directory under `skills/`.
- Each skill must include a `SKILL.md` entry file.
- Public skills should avoid private team names, internal endpoints, private credentials, and organization-specific assumptions unless clearly documented as examples.
- Do not commit local credentials, tokens, generated runtime configuration, or environment-specific files.

## Release Scope

This repository is intended for public distribution on GitHub and ClawHub.
Private or team-only skills should stay outside this repository or be excluded from the public release process.
