---
title: Benchmark expansion - how should five cases grow into the full fifteen-case portfolio benchmark?
type: grilling
mode: HITL
status: open
assignee: 
blocked_by: [evaluation-release-gates, comparison-report]
gist: 
---

## Question

After the five-case demo is stable, how should the benchmark expand to fifteen cases across the grant portal, packing list, and menu-ordering fixtures while preserving frozen expectations and avoiding test cases selected to flatter v2?

<!-- decision-map:graph:start -->
```mermaid
graph TD
    ME["benchmark-expansion (this ticket)"]
    P0["comparison-report"] --> ME
    P1["evaluation-release-gates"] --> ME
```
<!-- decision-map:graph:end -->
