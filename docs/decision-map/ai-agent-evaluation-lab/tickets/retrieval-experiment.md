---
title: Retrieval experiment - how should keyword and semantic retrieval be compared?
type: prototype
mode: HITL
status: open
assignee: 
blocked_by: [benchmark-contract]
gist: 
---

## Question

Which corpus, chunking rule, keyword baseline, embedding path, local vector store, top-k policy, and retrieval metrics make the keyword-versus-semantic comparison fair and explainable?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["retrieval-experiment (this ticket)"]
    P0["benchmark-contract"] --> ME
    ME --> C0["comparison-report"]
    ME --> C1["evaluation-release-gates"]
```
<!-- decision-map:graph:end -->
