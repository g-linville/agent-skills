---
name: generate-tests
description: Generate unit tests for a given source file, covering happy paths, edge cases, and error handling.
compatibility: Go, Python, TypeScript, JavaScript
metadata:
  createdAt: "2026-02-15T14:00:00Z"
  author: test-user
allowed-tools: "Read Write Bash"
---

## Inputs

- **file** (required): Path to the source file to generate tests for.
- **framework** (optional): Test framework to use. Default: auto-detect from project.

## Steps

### 1. Read Source
Read and analyze {{input.file}} to understand its public API, dependencies, and edge cases.

---

### 2. Identify Test Cases
List test cases covering:
- Happy path for each public function
- Edge cases (empty input, boundary values, nil/null)
- Error handling paths

---

### 3. Write Tests
Generate test code using {{input.framework}} conventions. Place the test file adjacent to the source.

## Output

Test file written. {{Write Tests}}
