---
title: Benchmark contract - which five cases and assertions are frozen for the first demo?
type: grilling
mode: HITL
status: closed
assignee: benchmark-contract-1158
blocked_by: []
gist: Freeze first-demo-v1 as five hash-addressed synthetic cases—2 grant, 2 packing, 1 menu—with binary assertions, partial-order tool traces, and immutable versioning.
---

## Question

Which five synthetic requirement cases, expected evidence sets, expected tool sequences, scored assertions, and freeze rules make the first benchmark representative without exceeding the 20-hour project timebox?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["benchmark-contract (this ticket)"]
    ME --> C0["agent-loop"]
    ME --> C1["comparison-report"]
    ME --> C2["evaluation-release-gates"]
    ME --> C3["retrieval-experiment"]
    ME --> C4["safety-policy"]
```
<!-- decision-map:graph:end -->

<!-- decision-map:resolution:start -->
## Resolution

Freeze first-demo-v1 as five hash-addressed synthetic cases—2 grant, 2 packing, 1 menu—with binary assertions, partial-order tool traces, and immutable versioning.

Detail: docs/benchmark/first-demo-v1-contract.md

```mermaid
flowchart TD
    B["Frozen first-demo-v1 contract"] --> C["Five exact prompts and evidence sets"]
    B --> A["Binary assertions and critical tags"]
    B --> T["Partial-order traces and call ceilings"]
    C --> N["Agent loop, retrieval, safety, gates, and report can proceed"]
    A --> N
    T --> N
```

Confirming exchange: the user approved the exact prompt set with: “approve”.

<!-- decision-map:resolution:end -->
