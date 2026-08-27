# AgentLens

AgentLens is an evaluation context for comparing AI-agent behavior using frozen synthetic evidence and reproducible scoring.

## Language

**First-demo benchmark**:
The frozen five-case suite used to demonstrate representative retrieval, citation, ambiguity, and safety behavior before the benchmark expands.
_Avoid_: Sample prompts, smoke tests

**Benchmark case**:
A frozen synthetic user request paired with its evidence set, expected tool sequence, and deterministic assertions.
_Avoid_: Test prompt, example question

**Frozen suite**:
An immutable, hash-addressed version of benchmark prompts, evidence, assertions, and tool constraints used for comparable evaluation runs.
_Avoid_: Current test data, latest fixtures

**Agent loop**:
The bounded sequence that turns a Benchmark case into provider requests, read-only evidence operations, a validated answer, and one correlated trace.
_Avoid_: Agent framework, autonomous workflow

