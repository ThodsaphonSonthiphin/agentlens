# Keep the observable agent loop application-owned

```mermaid
flowchart TD
    Q{"Where should benchmark orchestration live?"}
    Q -->|chosen| A["Small application-owned Python runner<br/>every boundary remains observable"]
    Q -->|rejected| B["Agent framework<br/>adds opaque behavior before the benchmark is stable"]
    Q -->|rejected| C["Provider adapter executes tools<br/>breaks the normalized provider boundary"]
```

Use one framework-free Python runner that owns prompt assembly, bounded sequential read-only tool execution, one explicit retry policy, structured-output validation, terminal failure records, normalized usage accumulation, and run-ID propagation across the trace. Provider adapters only return normalized model turns, while tools remain application-owned; [the runnable prototype](../../prototypes/agent_loop.py) demonstrates both a recovered timeout and a deterministic invalid-output failure.

