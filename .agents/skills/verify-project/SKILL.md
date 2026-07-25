---
name: verify-project
description: Review the Claude and Codex configuration examples for syntax, broken paths, and exposed secrets.
---

# Verify project

## Procedure

1. Inventory instruction and configuration files.
2. Validate JSON and TOML syntax.
3. Confirm that paths mentioned in documentation exist.
4. Search for values that resemble API keys, tokens, or passwords.
5. Report findings in priority order with a recommended fix.

## Safety

- A review request does not authorize file changes.
- Redact any value that appears to be a real credential.

