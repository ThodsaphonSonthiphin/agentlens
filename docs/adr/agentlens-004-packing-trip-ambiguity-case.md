# Require clarification for an ambiguous trip name

```mermaid
flowchart TD
    Q{"How should Packing Case 1 handle two Summit trips?"}
    Q -->|chosen| A["Name both matches and ask which trip<br/>without recommending items yet"]
    Q -->|rejected| B["Choose the top search result<br/>confident but unsupported"]
```

Packing Case 1 will ask what Alex should pack for “the Summit trip” while the frozen corpus contains both an Alpine Summit trek and a Summit client conference. A passing response must cite both matching trip records, ask one focused clarification, recommend no items before clarification, and follow `search → read both trip summaries → ask for clarification`.
