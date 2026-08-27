---
title: Evaluation gates - which deterministic thresholds decide whether v2 is releasable?
type: grilling
mode: HITL
status: open
assignee: 
blocked_by: [benchmark-contract, agent-loop, retrieval-experiment, safety-policy]
gist: 
---

## Question

Which deterministic evaluators, aggregation rules, failure precedence, minimum thresholds, and optional LLM-judge boundaries decide whether v2 improves on v1 without hiding failed safety, citation, schema, or hallucination cases?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["evaluation-release-gates (this ticket)"]
    P0["agent-loop"] --> ME
    P1["benchmark-contract"] --> ME
    P2["retrieval-experiment"] --> ME
    P3["safety-policy"] --> ME
    ME --> C0["benchmark-expansion"]
    ME --> C1["comparison-report"]
```
<!-- decision-map:graph:end -->
