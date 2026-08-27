---
title: Agent loop - what is the smallest observable orchestration loop for the benchmark?
type: prototype
mode: HITL
status: open
assignee: 
blocked_by: [benchmark-contract, provider-boundary]
gist: 
---

## Question

What minimal custom Python orchestration loop demonstrates prompt assembly, bounded read-only tools, retrieval, retries, structured-output validation, failure handling, and trace propagation while remaining understandable without an agent framework?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["agent-loop (this ticket)"]
    P0["benchmark-contract"] --> ME
    P1["provider-boundary"] --> ME
    ME --> C0["comparison-report"]
    ME --> C1["evaluation-release-gates"]
    ME --> C2["trace-cost-contract"]
```
<!-- decision-map:graph:end -->
