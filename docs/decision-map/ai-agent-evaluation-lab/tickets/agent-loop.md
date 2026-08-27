---
title: Agent loop - what is the smallest observable orchestration loop for the benchmark?
type: prototype
mode: HITL
status: closed
assignee: agent-loop-1238
blocked_by: [benchmark-contract, provider-boundary]
gist: Use a framework-free application-owned Python runner for prompt assembly, bounded read-only tools, retries, schema validation, failures, usage, and correlated traces.
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

## Comment

## Prototype artifact

[Runnable agent-loop prototype](../../../../prototypes/agent_loop.py)

Verified in the working tree based on `main` (`3bd7fa9`):

- `python prototypes/agent_loop.py --scenario success` completed with three read-only calls, one retry, schema-valid output, and a 14-event correlated trace.
- `python prototypes/agent_loop.py --scenario invalid-output` failed deterministically with `invalid_output`.
- `python -m py_compile prototypes/agent_loop.py` passed.

<!-- decision-map:resolution:start -->
## Resolution

Use a framework-free application-owned Python runner for prompt assembly, bounded read-only tools, retries, schema validation, failures, usage, and correlated traces.

Detail: docs/adr/agentlens-017-application-owned-agent-loop.md

```mermaid
sequenceDiagram
    participant R as Benchmark runner
    participant P as Model provider
    participant T as Read-only tools
    R->>P: normalized messages, tools, output schema
    P-->>R: retryable failure or tool calls
    R->>T: validated bounded call
    T-->>R: correlated evidence result
    R->>P: messages plus tool result
    P-->>R: final structured output
    R->>R: validate, accumulate usage, finish trace
```

Confirming exchange: the user approved the runnable prototype with: “ok”.

<!-- decision-map:resolution:end -->
