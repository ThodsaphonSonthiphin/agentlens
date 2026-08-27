# Balance the first-demo benchmark across three domains

```mermaid
flowchart TD
    Q{"How should five first-demo cases be distributed?"}
    Q -->|chosen| A["2 grant + 2 packing + 1 menu<br/>covers distinct evidence and safety risks"]
    Q -->|rejected| B["Single-domain suite<br/>faster to author but weak and easy to overfit"]
```

The first-demo benchmark will contain two synthetic grant-portal cases, two packing-list cases, and one menu-ordering case. This distribution gives the five-case suite distinct retrieval, citation, ambiguity, prompt-injection, and unauthorized-write behaviors while remaining achievable within the 20-hour project timebox.
