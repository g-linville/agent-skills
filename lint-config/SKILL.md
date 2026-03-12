---
name: lint-config
description: Analyze and fix linter configuration files for common issues and best practices.
metadata:
  createdAt: "2026-03-10T16:00:00Z"
  author: test-user
  branch-only: "true"
---

## Inputs

- **config_file** (optional): Path to the linter config. Default: auto-detect.

## Steps

### 1. Detect Config
Find the linter configuration file (eslint, golangci-lint, pylint, etc.) in the project.

---

### 2. Analyze
Check for:
- Conflicting rules
- Deprecated options
- Missing recommended rules for the project type

---

### 3. Fix
Apply recommended fixes and output a summary of changes.

## Output

{{Fix}}
