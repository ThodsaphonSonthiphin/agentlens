---
title: Trace and cost contract - what must be recorded, redacted, and budgeted?
type: grilling
mode: HITL
status: open
assignee: 
blocked_by: [provider-boundary, agent-loop]
gist: 
---

## Question

Which trace fields, correlation rules, token and cost calculations, redaction policy, failure records, and THB 300 budget guard provide useful observability without exposing prompts, secrets, or provider-specific details?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["trace-cost-contract (this ticket)"]
    P0["agent-loop"] --> ME
    P1["provider-boundary"] --> ME
    ME --> C0["comparison-report"]
    ME --> C1["public-packaging"]
```
<!-- decision-map:graph:end -->
