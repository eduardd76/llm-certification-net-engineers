# Network LLM Engineering Glossary — Part 1

Terms A2A through DoRA.

## A2A

**Definition:** Agent2Agent Protocol, an open standard for interoperable communication between agentic applications.

**Networking context:** A NOC agent can delegate to a security agent without sharing internal implementation.

## Ablation

**Definition:** An experiment removing/changing one component to measure its contribution.

**Networking context:** Compare RAG with and without reranking.

## Accuracy

**Definition:** Fraction of predictions judged correct.

**Networking context:** Good for classification and deterministic tasks.

## Activation

**Definition:** The intermediate value produced by a neural network layer.

**Networking context:** Activations consume memory during training.

## Active Learning

**Definition:** Selecting the most informative uncertain examples for human labeling.

**Networking context:** Send ambiguous incidents to experts for labels.

## Adapter

**Definition:** A small trainable module attached to a frozen model.

**Networking context:** Store separate NOC and SOC adapters.

## Adapter Merging

**Definition:** Combining one or more LoRA/adapters with a base or each other under supported methods.

**Networking context:** Potentially consolidate specialist adapters after evaluation.

## Advantage

**Definition:** In RL, a signal estimating how much better an action/output was than a baseline.

**Networking context:** GRPO derives relative advantages from group rewards.

## Agent

**Definition:** A system in which a model participates in a loop that can choose actions/tools, observe results, and continue toward a goal.

**Networking context:** A NOC agent queries topology, telemetry, and runbooks before proposing remediation.

## Agent Loop

**Definition:** Repeated cycle of observe -> decide -> act/tool -> observe until done or stopped.

**Networking context:** Read ticket, query telemetry, test hypothesis, summarize.

## Agentic Workflow

**Definition:** A workflow with iterative model decisions, tool use, state, and control logic.

**Networking context:** Diagnose -> collect evidence -> verify -> propose change.

## Alignment

**Definition:** Shaping model behavior toward intended goals, preferences, and constraints.

**Networking context:** Align a NOC assistant with safe operating procedures.

## Alignment Tax

**Definition:** Potential loss in some capabilities/performance as a model is optimized for preferred behavior or constraints.

**Networking context:** Over-alignment to terse NOC format can hurt open-ended explanation quality.

## Anomaly Detection

**Definition:** Methods that identify observations that deviate from an expected baseline.

**Networking context:** Detect unusual interface error rates or traffic patterns.

## API

**Definition:** Application Programming Interface.

**Networking context:** Expose `POST /v1/chat/completions` to internal tools.

## Artificial Intelligence (AI)

**Definition:** The broad field of building systems that perform tasks associated with intelligence, such as perception, prediction, planning, language, and decision support.

**Networking context:** AI is the umbrella; an AI NOC can include anomaly detectors, LLMs, optimization, and rules.

## Attention

**Definition:** A mechanism that lets token representations weight information from other token positions.

**Networking context:** A question token can attend to relevant earlier CLI lines.

## Attention Head

**Definition:** One parallel attention subspace within multi-head attention.

**Networking context:** Different heads can learn different relationships.

## Autoencoder

**Definition:** A model trained to reconstruct its input through a compressed representation.

**Networking context:** Can learn compact telemetry representations and support anomaly detection.

## Autonomy Level

**Definition:** The degree to which a system can act without human approval.

**Networking context:** Read-only diagnosis vs supervised remediation vs autonomous changes.

## Autoregressive

**Definition:** Generating/predicting one token conditioned on previous tokens.

**Networking context:** LLM text generation is typically autoregressive.

## AWQ

**Definition:** Activation-aware Weight Quantization, which uses activation behavior to preserve important weights/channels during low-bit quantization.

**Networking context:** Quantize a Network LLM using representative CLI/incident calibration data.

## Backpropagation

**Definition:** Algorithm for computing gradients through a neural network using the chain rule.

**Networking context:** Makes transformer training possible.

## Base Model

**Definition:** A pretrained model before instruction/chat alignment.

**Networking context:** Often better suited as a starting point for some continued-pretraining tasks.

## Baseline

**Definition:** A reference system measured before introducing a new technique.

**Networking context:** Prompt-only base model before fine-tuning.

## Batch

**Definition:** A group of examples processed together in one training step.

**Networking context:** GPU memory limits how many sequences fit in a batch.

## Batching

**Definition:** Processing multiple inference requests together for hardware efficiency.

**Networking context:** Serving engines dynamically batch network-assistant requests.

## Bayesian Inference

**Definition:** Updating probability beliefs as evidence is observed.

**Networking context:** A disciplined analogy for revising outage hypotheses after each test.

## Beam Search

**Definition:** Maintaining multiple high-scoring sequence candidates during decoding.

**Networking context:** More common in some sequence tasks than chat LLM usage.

## Benchmark

**Definition:** A standardized collection of tasks and metrics for comparing models.

**Networking context:** A networking benchmark might include routing, configs, and incident reasoning.

## BF16

**Definition:** bfloat16: 16-bit floating point with FP32-like exponent range.

**Networking context:** Often preferred on supported modern GPUs.

## Bias

**Definition:** A learned additive parameter in many neural layers; not the same as social/model bias.

**Networking context:** A linear layer may use weight*x + bias.

## Calibration

**Definition:** How well confidence values correspond to actual correctness likelihood.

**Networking context:** A '90% confident' system should be right about 90% in that band.

## Canary Deployment

**Definition:** Rolling a change to a small subset before broad rollout.

**Networking context:** Test an AI-proposed config on one site first.

## Capability Evaluation

**Definition:** Tests whether the model can perform desired tasks.

**Networking context:** Can it identify an MTU hypothesis?

## Catastrophic Forgetting

**Definition:** Loss of previously learned abilities after narrow training.

**Networking context:** An over-tuned network adapter becomes worse at general language.

## Causal Mask

**Definition:** A mask preventing a decoder token from attending to future tokens.

**Networking context:** Required for autoregressive next-token training.

## Chain-of-Thought (CoT)

**Definition:** A term for intermediate reasoning steps used or elicited during problem solving; internal reasoning need not be exposed to users.

**Networking context:** Prefer concise evidence and decision summaries rather than requiring hidden reasoning transcripts.

## Checkpoint

**Definition:** Saved model/training state.

**Networking context:** Resume training or retain the best adapter.

## Chosen / Rejected

**Definition:** The preferred and dispreferred answers in pairwise preference data.

**Networking context:** Used directly by DPO-style training.

## Chunk

**Definition:** A portion of a source document used as a retrieval unit.

**Networking context:** An RFC section or troubleshooting procedure subsection.

## Chunking

**Definition:** The process of splitting documents into retrieval-sized pieces.

**Networking context:** Bad chunking can separate a command from its explanation.

## Circuit Breaker

**Definition:** A reliability control that stops repeated calls to a failing dependency.

**Networking context:** Disable an unhealthy device API temporarily.

## Classification

**Definition:** A supervised-learning task that assigns one of several categories to an input.

**Networking context:** Classify an incident as LAN, WAN, DNS, security, or application.

## Closed Model

**Definition:** A model accessed as a service without distributing its weights.

**Networking context:** May offer higher capability but less deployment control.

## Clustering

**Definition:** An unsupervised method that groups similar examples without predefined labels.

**Networking context:** Group recurring incident patterns or telemetry behavior.

## Concept Drift

**Definition:** Change in the relationship between inputs and correct outputs.

**Networking context:** Operational policy for what counts as an incident changes.

## Confidence Threshold

**Definition:** A cutoff used to route low-confidence cases to more review or stronger models.

**Networking context:** Low confidence -> human escalation.

## Context Window

**Definition:** Maximum token span a model can attend to for a request.

**Networking context:** A 32K-token context may hold topology, logs, and a question.

## Contextual Compression

**Definition:** Reducing retrieved context to passages relevant to the query before generation.

**Networking context:** Remove irrelevant runbook paragraphs before passing context to the LLM.

## Continued Pretraining

**Definition:** Additional language-model pretraining on a new/domain corpus.

**Networking context:** Adapt a base model to networking text.

## Continuous Batching

**Definition:** Dynamically adding/removing requests from an inference batch as they progress.

**Networking context:** A major LLM serving optimization.

## Contrastive Learning

**Definition:** Learning representations by pulling matching pairs closer and pushing mismatched pairs apart.

**Networking context:** Align network diagram images with descriptive text in multimodal models.

## Convolutional Neural Network (CNN)

**Definition:** A neural architecture using convolutional filters, historically dominant in image and spatial tasks.

**Networking context:** May process visual network diagrams or spectrogram-like telemetry representations.

## Cosine Similarity

**Definition:** A similarity measure based on the angle between vectors.

**Networking context:** Commonly used to rank query/document embeddings.

## Coverage

**Definition:** How much of the required answer/evidence is captured.

**Networking context:** Did the diagnosis include return-path verification?

## Cross-Entropy

**Definition:** A loss comparing predicted probability distributions with target outcomes.

**Networking context:** Standard next-token training loss.

## Curriculum Learning

**Definition:** Training examples ordered or staged from easier to harder tasks.

**Networking context:** Subnet basics before complex EVPN troubleshooting.

## Data Contamination

**Definition:** Unintended overlap between training data and benchmark/test material.

**Networking context:** Can make evaluation results look stronger than true generalization.

## Data Curation

**Definition:** Selecting, cleaning, balancing, labeling, and reviewing data for a model task.

**Networking context:** Often more important than simply increasing training volume.

## Data Distillation

**Definition:** Using a stronger teacher or process to produce training targets for a smaller student.

**Networking context:** Teacher generates expert incident analyses for a local SLM.

## Data Drift

**Definition:** Change in the input-data distribution over time.

**Networking context:** Incidents shift from MPLS to SD-WAN after a migration.

## Data Flywheel

**Definition:** A feedback loop where production interactions produce reviewed data that improves future systems.

**Networking context:** Engineer corrections become candidate SFT/eval examples.

## Data Leakage

**Definition:** Information from validation/test unintentionally entering training or prompts.

**Networking context:** Paraphrases of test incidents in train can inflate scores.

## Data Lineage

**Definition:** Traceability from a dataset/model output back to source data and transformations.

**Networking context:** Know which incident/RFC created each training example.

## Data Parallelism

**Definition:** Replicating a model across devices and splitting batches.

**Networking context:** Each GPU processes different examples.

## Dataset

**Definition:** A structured collection of examples used for training, validation, or testing.

**Networking context:** Prompt/answer pairs about OSPF, BGP, and EVPN.

## Decision Tree

**Definition:** A model that makes predictions by following learned feature-based decision branches.

**Networking context:** Classify incidents from measurable telemetry features.

## Decoder

**Definition:** Autoregressive transformer component that generates tokens.

**Networking context:** GPT/Qwen/Llama-style LLMs are decoder-only.

## Decoder-Only Model

**Definition:** An autoregressive transformer that predicts subsequent tokens from preceding tokens.

**Networking context:** Most chat LLMs use this design.

## Deduplication

**Definition:** Removing duplicate or near-duplicate examples/documents.

**Networking context:** Prevents memorization and train/test leakage.

## Deep Learning (DL)

**Definition:** Machine learning based on multi-layer neural networks that learn hierarchical representations.

**Networking context:** Transformers are deep neural networks used by modern LLMs.

## DeepSpeed

**Definition:** A library/runtime providing memory and distributed-training optimizations such as ZeRO.

**Networking context:** Often used for multi-GPU LLM training.

## Dense Model

**Definition:** A model where essentially all core model parameters are used for each token.

**Networking context:** Classic Llama/Qwen dense variants.

## Dense Retrieval

**Definition:** Retrieval using neural embeddings.

**Networking context:** Strong for semantic paraphrases.

## Determinism

**Definition:** Degree to which repeated runs produce the same result.

**Networking context:** Low-temperature generation helps but GPU kernels may still vary.

## Deterministic Evaluation

**Definition:** Evaluation using exact algorithms/rules with no model judgment.

**Networking context:** Subnet math, schema validation, topology reachability, syntax checks.

## Diffusion Model

**Definition:** A generative model that learns to reverse a gradual noising process.

**Networking context:** Dominant in many image-generation systems; separate from LLM autoregressive generation.

## Digital Twin

**Definition:** A model/simulation of a real system used for analysis or validation.

**Networking context:** Test a network change against a lab twin before production.

## Dimensionality Reduction

**Definition:** Methods that reduce the number of features while trying to preserve useful structure.

**Networking context:** Project embeddings or telemetry to 2D/3D for inspection.

## Distributed Training

**Definition:** Training across multiple accelerators or machines.

**Networking context:** Needed for models that do not fit on one GPU.

## Domain-Adaptive Pretraining (DAPT)

**Definition:** Continued pretraining focused on a domain corpus.

**Networking context:** RFCs, network design docs, sanitized internal runbooks.

## DoRA

**Definition:** Weight-Decomposed Low-Rank Adaptation, a LoRA-related method that separates weight magnitude and direction.

**Networking context:** An advanced adapter option; evaluate rather than assuming it beats standard LoRA.
