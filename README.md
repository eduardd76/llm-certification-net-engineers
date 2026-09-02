# Network LLM Engineering — Full Course

A practical, networking-first course covering the complete path from AI terminology and transformer fundamentals
to fine-tuning, RAG, DPO/GRPO/RLVR, agents, MCP/A2A, digital-twin verification, serving, observability, and production AI NOC design.

## Scope

- 29 Jupyter notebooks
- 317 glossary terms with networking examples
- Networking SFT data (where copied from the original course)
- Preference dataset for safe troubleshooting behavior
- Verifiable subnet tasks for RLVR
- Mini retrieval corpus plus live RFC-download labs
- Capstone integrating RAG + tools + model + validators

## Course sequence

### Orientation
- `00_start_here.ipynb`

### Part I — Foundations
- `01_ai_ml_dl_genai_llm.ipynb`
- `02_neural_networks_gradients.ipynb`
- `03_transformer_attention.ipynb`
- `04_tokens_context_logits_decoding.ipynb`
- `05_model_lifecycle_and_model_types.ipynb`

### Part II — Knowledge and Context
- `06_prompt_engineering_and_structured_outputs.ipynb`
- `07_embeddings_and_vector_search.ipynb`
- `08_rag_for_network_engineers.ipynb`
- `09_graphrag_and_network_knowledge_graphs.ipynb`

### Part III — Adaptation
- `10_network_llm_data_engineering.ipynb`
- `11_pretraining_and_continued_pretraining.ipynb`
- `12_sft_supervised_finetuning.ipynb`
- `13_lora_peft.ipynb`
- `14_qlora_and_quantization.ipynb`
- `15_evaluation_for_network_llms.ipynb`

### Part IV — Post-Training
- `16_preferences_reward_models_rlhf.ipynb`
- `17_dpo_network_preferences.ipynb`
- `18_grpo_and_rlvr_network_tasks.ipynb`
- `19_distillation_and_synthetic_data.ipynb`

### Part V — Agentic Systems
- `20_tool_calling_and_function_calling.ipynb`
- `21_agents_planning_memory_orchestration.ipynb`
- `22_mcp_and_a2a.ipynb`

### Part VI — Production Network AI
- `23_network_ai_noc_reference_architecture.ipynb`
- `24_digital_twin_and_verification.ipynb`
- `25_serving_vllm_latency_and_cost.ipynb`
- `26_observability_security_governance.ipynb`

### Capstone and reference
- `27_capstone_network_llm_engineering_system.ipynb`
- `99_glossary_explorer.ipynb`

## Recommended study path

**Beginner:** 00–12, 15, 20, 23, 27  
**LLM engineer:** all notebooks  
**Network AI architect:** all notebooks, with special focus on 08–09, 15, 20–27

## Hardware

Most concept/RAG notebooks run on CPU. Model-generation labs are smoother with a GPU.
LoRA/DPO/GRPO training cells are explicitly marked as GPU labs and use small models/short runs by default.

## Core architecture principle

> Fine-tuning changes model behavior. RAG/tools provide current facts. Deterministic systems verify what can be verified.

For Network AI, reliability comes from the composition of these mechanisms rather than from model size alone.

## Version baseline checked on 2026-08-23

- Transformers 5.14.1
- TRL 1.10.0
- PEFT 0.20.0
- Datasets 5.0.1
- Accelerate 1.14.0
- Sentence Transformers 5.7.0

See the official library documentation before upgrading the pinned environment because post-training APIs evolve quickly.


## Professional Certification Track

This package now includes a full **Network LLM Engineer Professional Certification** track in `certification/`.

The track is designed for **54–58 hours** and includes:
- six module quizzes,
- architecture assignments,
- troubleshooting challenge bank,
- two practical exams,
- final AI NOC capstone,
- instructor guide,
- grading rubrics,
- student certification checklist.

Start with `CERTIFICATION_BLUEPRINT.md`.

## Advanced RAG / Quantization / LLMOps / Security expansion

Additional networking-focused notebooks:
- `28_advanced_rag_patterns.ipynb`
- `29_quantization_deep_dive.ipynb`
- `30_multimodal_network_ai.ipynb`
- `31_llmops_ci_release.ipynb`
- `32_llm_security_red_teaming.ipynb`
- `33_local_server_edge_deployment.ipynb`

See `SOURCE_INTEGRATION_LLM_OPEN_UNIVERSITY.md` for the curriculum mapping.
