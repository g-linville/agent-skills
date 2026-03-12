---
name: summarize-issue
description: Summarize a GitHub issue with context, impact assessment, and suggested next steps.
license: Apache-2.0
metadata:
  createdAt: "2026-02-10T08:30:00Z"
  author: test-user
---

## Inputs

- **issue_url** (required): URL of the GitHub issue to summarize.

## Steps

### 1. Fetch Issue
Retrieve the issue details from {{input.issue_url}}.

---

### 2. Analyze Context
Analyze the issue description, comments, and linked PRs to understand the full context.

---

### 3. Summarize
Produce a concise summary including:
- **Problem:** What is the issue about?
- **Impact:** Who is affected and how severely?
- **Next Steps:** Recommended actions to resolve.

## Output

{{Summarize}}
