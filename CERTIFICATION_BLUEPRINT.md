# Network LLM Engineer — Professional Certification Blueprint

## Program length

**Recommended total: 54–58 hours**

| Module | Topic | Guided learning | Labs / assessment | Total |
|---|---|---:|---:|---:|
| 0 | Orientation and environment | 1 h | 1 h | 2 h |
| 1 | AI/ML/LLM foundations | 4 h | 2 h | 6 h |
| 2 | Prompting, embeddings, RAG, GraphRAG | 4 h | 3 h | 7 h |
| 3 | Data engineering and fine-tuning | 5 h | 5 h | 10 h |
| 4 | Preference optimization, RLVR, distillation | 4 h | 3 h | 7 h |
| 5 | Tool use, agents, MCP/A2A | 4 h | 3 h | 7 h |
| 6 | Production Network AI architecture | 4 h | 3 h | 7 h |
| 7 | Final AI NOC capstone | 2 h coaching | 6–10 h project | 8–12 h |

Typical completion: **54–58 hours**.

## Certification outcomes

A certified learner must be able to:

1. Explain the AI/ML/LLM stack without confusing terminology.
2. Decide when to use prompting, RAG, fine-tuning, preference optimization, RL, tools, or deterministic logic.
3. Build and validate a networking SFT dataset.
4. Fine-tune a small language model with LoRA/QLoRA.
5. Design held-out capability, grounding, safety, and operational evaluations.
6. Build a networking RAG pipeline and explain retrieval failure modes.
7. Use preference data, DPO, and verifiable rewards appropriately.
8. Integrate models with read-only tools and structured outputs.
9. Explain MCP vs A2A and place both in a Network AI architecture.
10. Design a bounded agentic workflow with state, termination conditions, and human approval.
11. Use a digital twin or deterministic verifier as an assurance mechanism.
12. Design a production AI NOC architecture with model routing, observability, security, and release gates.
13. Demonstrate all of the above in a final AI NOC capstone.

## Assessment model

| Component | Weight |
|---|---:|
| Module quizzes | 15% |
| Hands-on lab checkpoints | 15% |
| Architecture assignments | 15% |
| Practical Exam 1 — Fine-Tuning | 15% |
| Practical Exam 2 — Agentic Network AI | 15% |
| Final AI NOC Capstone | 25% |

### Certification pass standard

- **75% overall**
- At least **70% on each practical exam**
- At least **70% on the final capstone**
- No critical safety failure

### Critical safety failures

Any of the following is an automatic fail for the relevant practical/capstone attempt:

- Inventing current network state instead of using supplied evidence/tools.
- Executing or recommending an unrestricted production change without required authorization.
- Bypassing a deterministic policy/approval gate.
- Exposing secrets or using unsanitized sensitive training data in a submitted artifact.
- Treating model confidence as proof of correctness.

## Certification philosophy

The certification tests whether the learner can build a reliable **system**, not whether they can memorize acronyms.

A strong answer may choose **not** to use an LLM when a deterministic method is stronger.


## Graded lab checkpoints

- **Lab 1 — Model Baseline and Prompt Engineering** — 2 h, 15 raw points
- **Lab 2 — Build and Break a Network RAG Pipeline** — 2.5 h, 20 raw points
- **Lab 3 — Topology-Aware Retrieval** — 2 h, 15 raw points
- **Lab 4 — Build a Network SFT Dataset** — 2.5 h, 20 raw points
- **Lab 5 — LoRA Fine-Tuning Experiment** — 3 h, 25 raw points
- **Lab 6 — Preference and Verifiable Reward Design** — 2.5 h, 20 raw points
- **Lab 7 — Bounded Network Agent** — 3 h, 25 raw points
- **Lab 8 — AI NOC Assurance and Release Gate** — 2.5 h, 20 raw points


## Advanced curriculum integration

The certification now also includes advanced content inspired by the LLM Open University roadmap:

- Advanced RAG: hybrid retrieval, RRF, multi-query, HyDE, parent/child retrieval, contextual compression, metadata/self-query.
- Quantization deep dive: PTQ, QAT, GPTQ, AWQ, GGUF, QLoRA.
- Multimodal/VLM Network AI and multimodal RAG.
- LLMOps: continuous evaluation, experiment tracking, artifact/model registry, CI release gates.
- LLM application security and defensive red teaming.
- Local/server/edge deployment and local runtimes.

These are **integrated into the existing 54–58 hour core by replacing lighter coverage**, except multimodal and Labs 9–11, which are advanced electives.
With all electives, expect approximately **60–64 hours**.
