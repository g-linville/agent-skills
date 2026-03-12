---
name: deploy-checker
description: Verify a deployment is healthy by checking endpoints, logs, and metrics.
metadata:
  createdAt: "2026-03-01T10:00:00Z"
  author: test-user
---

## Inputs

- **environment** (required): Target environment — `staging` or `production`.
- **service** (required): Name of the service to check.

## Steps

### 1. Check Health Endpoint
Hit the health endpoint for {{input.service}} in {{input.environment}} and verify a 200 response.

---

### 2. Check Recent Logs
Scan the last 5 minutes of logs for errors or panics related to {{input.service}}.

---

### 3. Verify Metrics
Check key metrics (error rate, latency p99, CPU) are within normal thresholds.

**On error:** Report Failure

---

### 4. Report Success
Deployment of {{input.service}} to {{input.environment}} looks healthy.

**Condition:** {{Check Health Endpoint}} contains 200

---

### 5. Report Failure
Deployment issues detected. Manual investigation recommended.

**Condition:** {{Check Health Endpoint}} not contains 200

## Output

{{Report Success}}
{{Report Failure}}
