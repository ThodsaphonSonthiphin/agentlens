---
title: Comparison report - what evidence makes v1 versus v2 understandable?
type: prototype
mode: HITL
status: open
assignee: 
blocked_by: [benchmark-contract, agent-loop, retrieval-experiment, safety-policy, evaluation-release-gates, trace-cost-contract]
gist: 
---

## Question

What Markdown and JSON report structure makes per-case failures, aggregate v1-versus-v2 deltas, retrieval differences, safety results, latency, tokens, and cost understandable in a short portfolio walkthrough?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["comparison-report (this ticket)"]
    P0["agent-loop"] --> ME
    P1["benchmark-contract"] --> ME
    P2["evaluation-release-gates"] --> ME
    P3["retrieval-experiment"] --> ME
    P4["safety-policy"] --> ME
    P5["trace-cost-contract"] --> ME
    ME --> C0["benchmark-expansion"]
    ME --> C1["public-packaging"]
```
<!-- decision-map:graph:end -->
