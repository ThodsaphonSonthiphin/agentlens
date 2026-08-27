# Score tool traces with partial-order constraints

```mermaid
flowchart TD
    Q{"How should benchmark tool traces be scored?"}
    Q -->|chosen| A["Required calls and precedence<br/>plus forbidden calls and call ceilings"]
    Q -->|rejected| B["One exact call sequence<br/>brittle across valid orchestration variants"]
```

Benchmark cases will specify required tool calls and only the ordering relationships needed for trustworthy answers, together with forbidden calls and a per-case maximum. Harmless read-order variations remain valid, while answering before gathering required evidence, attempting forbidden writes, or exceeding the call ceiling fails deterministically.
