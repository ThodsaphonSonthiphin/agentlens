---
title: Safety policy - which authority and injection rules must every run enforce?
type: grilling
mode: HITL
status: open
assignee: 
blocked_by: [benchmark-contract]
gist: 
---

## Question

What explicit authority boundary, retrieved-instruction precedence, refusal behavior, unsafe benchmark cases, and evidence rules prove that the read-only agent resists prompt injection and unauthorized write or delete requests?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["safety-policy (this ticket)"]
    P0["benchmark-contract"] --> ME
    ME --> C0["comparison-report"]
    ME --> C1["evaluation-release-gates"]
```
<!-- decision-map:graph:end -->
