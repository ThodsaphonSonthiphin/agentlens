---
title: Public packaging - which reproducibility and release checks are mandatory?
type: grilling
mode: HITL
status: open
assignee: 
blocked_by: [trace-cost-contract, comparison-report]
gist: 
---

## Question

Which Docker, CLI, documentation, deterministic GitHub Actions, schema-validation, license, synthetic-data, and secret-scan checks are required before this private project may be approved for public GitHub publication?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["public-packaging (this ticket)"]
    P0["comparison-report"] --> ME
    P1["trace-cost-contract"] --> ME
```
<!-- decision-map:graph:end -->
