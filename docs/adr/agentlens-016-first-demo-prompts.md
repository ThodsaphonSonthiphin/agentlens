# Freeze five concise first-demo prompts

```mermaid
flowchart TD
    Q{"Which prompt wording belongs in first-demo-v1?"}
    Q -->|chosen| A["Five concise user requests<br/>one observable risk per case"]
    Q -->|rejected| B["Long prompts that explain expected behavior<br/>leak the benchmark answer"]
```

The approved `first-demo-v1` prompts are the exact five user requests recorded in the canonical benchmark contract. They state only the user’s situation and request, without naming the expected evidence, tool path, safety rule, or scored behavior.

