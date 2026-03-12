---
name: code-review
description: Review code changes for quality, security, performance, and best practices (feature-branch version).
license: MIT
compatibility: Works with any Git repository.
metadata:
  createdAt: "2026-02-01T12:00:00Z"
  author: test-user
allowed-tools: "Bash(git:*) Read Grep Glob"
---

## Inputs

- **target** (optional): Files or directory to review. Default: `.`
- **focus** (optional): Area of focus — one of `security`, `performance`, `readability`, or `all`. Default: `all`

## Steps

### 1. Find Changes
Identify all modified files in {{input.target}} using `git diff --name-only`.

---

### 2. Analyze Code
Review each changed file for:
- Security vulnerabilities (injection, auth issues)
- Performance concerns (N+1 queries, unnecessary allocations)
- Readability (naming, complexity, documentation)

Focus on: {{input.focus}}

---

### 3. Generate Report
Produce a structured report with findings categorized by severity (critical, warning, info).

## Output

{{Generate Report}}
