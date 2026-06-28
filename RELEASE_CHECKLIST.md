# Release Checklist

Before publishing this skill package:

- Confirm every skill directory contains `SKILL.md` and `README.md`.
- Check Markdown links on a case-sensitive filesystem or CI runner.
- Verify AgileBuilder MCP installation and resource access instructions are current.
- Ensure no private project documents, credentials, tokens, or generated workspaces are committed.
- Run `git status --short` and publish only from a clean working tree.
- Tag the release with a semantic version such as `v0.1.0`.

