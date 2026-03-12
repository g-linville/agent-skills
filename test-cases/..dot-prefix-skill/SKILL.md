---
name: dot-prefix-skill
description: Skill in a directory whose name starts with ".." to test path traversal edge cases.
---

This skill directory name starts with ".." which could be confused with directory traversal.
The scanner should either reject it or handle it safely without escaping the repo root.
