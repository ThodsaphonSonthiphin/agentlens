# Freeze benchmark suites as immutable hash-addressed versions

```mermaid
flowchart TD
    Q{"How should first-demo inputs change after evaluation begins?"}
    Q -->|chosen| A["Hash immutable first-demo-v1<br/>changes create a new suite version"]
    Q -->|rejected| B["Edit fixtures in place<br/>silently invalidates comparisons"]
```

The five prompts, corpus files, evidence IDs, assertion predicates and critical tags, tool constraints, call ceilings, and fake-provider script will be frozen as `first-demo-v1` before either skill version runs. The manifest and corpus files carry SHA-256 hashes, expected answers remain hidden from the agent, every result records the suite ID and hash, and any later correction—including wording—creates a new suite version rather than altering v1.
