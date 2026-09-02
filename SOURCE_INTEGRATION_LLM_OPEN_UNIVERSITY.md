# Integration of LLM Open University Roadmap

Source inspiration:
`youssefHosni/LLM-Open-University-From-Begineer-to-Advanced`

The source repository is used as a **curriculum-gap checklist and resource map**. This certification does not reproduce its README text.
Concepts are rewritten, updated, and converted into networking-specific lessons/labs.

## Mapping

| Source roadmap topic | Certification treatment |
|---|---|
| Transformer / tokenization / decoding | Existing Notebooks 03–05 |
| Dataset creation / instruction data | Existing Notebook 10 + Lab 4 |
| Fine-tuning | Existing Notebooks 12–14 + Practical Exam 1 |
| LLM evaluation | Existing Notebook 15 + release gates |
| Quantization: GGUF, AWQ, PTQ, GPTQ, QAT | **New Notebook 29** |
| RLHF / alignment | Existing Notebooks 16–18 |
| Vision-language / multimodal RAG | **New Notebook 30** |
| Prompt engineering | Existing Notebook 06 |
| Vector DB / RAG | Existing 07–08 |
| Advanced RAG: hybrid, self-query, parent doc, HyDE, fusion/compression | **New Notebook 28** |
| Agents / multi-agent / agent evaluation | Existing 20–22 + Practical Exam 2 |
| Inference optimization | Existing 25 + Notebook 29 |
| LLMOps / automated testing | **New Notebook 31** |
| LLM security / red teaming | **New Notebook 32** |
| Local/demo/server/edge deployment | **New Notebook 33** |
| Local runtimes: GPT4All, LM Studio, Ollama, llama.cpp | **New Notebook 33** |
| MCP | Existing Notebook 22 |
| Portfolio projects | Replaced by certification labs + AI NOC capstone |
| Staying current with research | Covered operationally through dependency/research update process |

## What we deliberately did not copy

- Long resource lists are not part of the graded core.
- Product-specific claims that may age quickly are framed as examples, not certification facts.
- Generic chatbot examples are converted to network-engineering cases.
- Older terminology/implementation guidance is subordinate to current official documentation.

## Pedagogical upgrade

The source roadmap frequently answers **"what should I study?"**

This certification adds:
- **what must I be able to build?**
- **how do I prove it works?**
- **what fails?**
- **what should not be an LLM?**
- **what prevents an unsafe production action?**
