# Allow one recovery call within each benchmark case

```mermaid
flowchart TD
    Q{"How tightly should first-demo tool calls be bounded?"}
    Q -->|chosen| A["Minimum evidence path plus one call<br/>ceilings 4, 5, 4, 5, 4"]
    Q -->|rejected| B["Minimum calls only<br/>rejects one reasonable recovery step"]
```

The maximum tool-call counts for Grant 1, Grant 2, Packing 1, Packing 2, and Menu 1 are respectively 4, 5, 4, 5, and 4. Each ceiling permits one recovery search or reread beyond the minimum evidence path; any forbidden write remains an immediate assertion failure regardless of the remaining call budget.
