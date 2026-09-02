# Final Capstone — Build an AI NOC Mini-Platform

## Objective

Build a small but complete AI NOC system that demonstrates professional Network LLM Engineering.

The capstone is not judged on how many agents or models you use.
It is judged on **architecture quality, evidence discipline, measurable performance, and safety**.

## Mandatory capabilities

### 1. Incident intake
Accept a structured incident with:
- incident ID,
- user-reported symptom,
- affected site/device/service,
- timestamp,
- known change context.

### 2. Knowledge retrieval
Use RAG over at least:
- protocol/RFC knowledge,
- one runbook,
- one historical incident.

### 3. Live evidence/tool layer
Implement read-only tools for at least three of:
- topology / source of truth,
- interface state,
- BGP/OSPF state,
- VNI/VRF state,
- route lookup,
- telemetry counters.

### 4. Reasoning/orchestration
Maintain structured state:
- observations,
- hypotheses,
- checks completed,
- evidence collected,
- confidence,
- next action.

### 5. Assurance
At least two of:
- schema validator,
- deterministic route/subnet verifier,
- policy engine,
- digital-twin reachability test,
- config parser/linter.

### 6. Human approval
No state-changing production action may execute without explicit approval.

### 7. Evaluation
Compare at least:
- base + prompt,
- base + RAG,
- adapted model,
- adapted model + RAG/tools/validators.

### 8. Observability
Produce a trace containing:
- model/version,
- retrieval sources,
- tool calls,
- validator results,
- decision,
- approval state,
- latency.

## Required incident set

Your capstone must successfully handle at least six incident families:

1. OSPF adjacency
2. BGP route/session
3. EVPN/VXLAN
4. VLAN/STP
5. MTU/tunnel
6. DNS or IPv6

At least one case must contain **insufficient evidence** and the system must say so.

At least one case must contain **indirect prompt injection** in retrieved content.

## Final presentation

15–20 minutes:
- 3 min problem and architecture
- 5 min live walkthrough
- 5 min evaluation results
- 3 min failures/limitations
- 2 min roadmap

## Submission artifacts

- architecture diagram
- code/notebooks
- dataset card
- model/adaptation card
- evaluation report
- threat model
- trace sample
- release gate
- retrospective: what should not be an LLM
