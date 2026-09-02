# Network LLM Engineering Glossary — Part 3

Terms LoRA through Retrieval-Augmented Generation (RAG).

## LoRA

**Definition:** Low-Rank Adaptation: frozen base weights plus trainable low-rank updates.

**Networking context:** Create a small networking adapter rather than a full model copy.

## LoRA Alpha

**Definition:** A scaling hyperparameter for the LoRA update.

**Networking context:** Controls the effective adapter contribution.

## LoRA Rank (r)

**Definition:** The dimensionality/capacity of LoRA's low-rank update.

**Networking context:** Higher rank means more trainable adapter parameters.

## Loss Function

**Definition:** A numerical objective minimized during training.

**Networking context:** Cross-entropy penalizes low probability on the correct next token.

## LSTM

**Definition:** Long Short-Term Memory, a gated RNN architecture designed to preserve longer-range dependencies.

**Networking context:** Can model telemetry sequences, though transformers and modern time-series models are common alternatives.

## Machine Learning (ML)

**Definition:** A subset of AI in which a system learns patterns from data instead of having every rule manually programmed.

**Networking context:** A model can learn to classify incident tickets from labeled historical tickets.

## MCP

**Definition:** Model Context Protocol, an open protocol for connecting AI applications to tools/data/context providers.

**Networking context:** Expose NetBox, telemetry, or ticketing capabilities through standardized interfaces.

## Memory

**Definition:** Persisted information reused across steps/sessions; can be short-term state or long-term storage.

**Networking context:** Remember incident evidence, not model hidden state.

## Metric

**Definition:** A quantitative evaluation measure.

**Networking context:** Accuracy, F1, exact match, latency, cost, schema validity.

## Mini-batch

**Definition:** The practical batch subset used for one forward/backward update.

**Networking context:** Most LLM training is mini-batch training.

## Mixed Precision

**Definition:** Using different numeric precisions during training for speed/memory while preserving stability.

**Networking context:** BF16 compute with some FP32 operations.

## Mixture of Experts (MoE)

**Definition:** Architecture with multiple expert subnetworks where only a subset activates for a token.

**Networking context:** Can scale parameter count without activating all parameters each token.

## Model Card

**Definition:** Documentation describing a model's purpose, limitations, training/evaluation, and intended use.

**Networking context:** Record that an adapter is not approved for autonomous changes.

## Model Drift

**Definition:** Degradation/change in model-system performance as data or environment changes.

**Networking context:** New network platforms may reduce diagnostic accuracy.

## Model License

**Definition:** Legal terms governing model use, redistribution, modification, and sometimes outputs.

**Networking context:** Must be reviewed before commercial/on-prem use.

## Model Registry

**Definition:** A controlled store/catalog for model versions and metadata.

**Networking context:** Track base model, adapter, eval score, and approval state.

## Model Routing

**Definition:** Selecting a model based on task, cost, latency, or capability.

**Networking context:** Use a 3B triage model and larger reasoning model only when needed.

## Model-Based Evaluation

**Definition:** Evaluation using another learned model as part of the scoring process.

**Networking context:** Use an LLM judge, but calibrate it against network experts.

## Monte Carlo Tree Search (MCTS)

**Definition:** A tree-search algorithm balancing exploration and exploitation through repeated simulations.

**Networking context:** Sometimes discussed in reasoning agents; use only when the environment/reward justifies the complexity.

## Multi-Agent System

**Definition:** A system composed of multiple specialized agents that coordinate.

**Networking context:** Topology, routing, security, and change-validation agents.

## Multi-Head Attention

**Definition:** Several attention heads computed in parallel.

**Networking context:** Allows multiple relation patterns to be represented.

## Multimodal Model

**Definition:** A model that can process or generate more than one modality such as text, image, audio, video.

**Networking context:** Read a network diagram plus CLI text.

## Multimodal RAG

**Definition:** Retrieval-augmented generation that indexes/retrieves more than text, such as images, diagrams, video, audio or tables.

**Networking context:** Retrieve topology diagrams plus runbook text for diagnosis.

## Near-Duplicate

**Definition:** Content that is highly similar but not byte-identical.

**Networking context:** Paraphrased incidents can still leak into evaluation.

## Neural Network

**Definition:** A parameterized function composed of layers and nonlinear operations.

**Networking context:** Transformers are neural networks.

## Neuro-Symbolic AI

**Definition:** Systems combining neural models with symbolic logic, rules, graphs, or formal methods.

**Networking context:** LLM proposes a diagnosis while graph/rule engines verify topology and policy constraints.

## NF4

**Definition:** NormalFloat4, a 4-bit data type designed for normally distributed neural weights.

**Networking context:** Common recommendation for QLoRA base-weight quantization.

## Objective

**Definition:** The mathematical goal optimized during training; often expressed through a loss.

**Networking context:** SFT optimizes likelihood of target completions.

## Observability

**Definition:** Instrumentation that makes system behavior measurable through logs, traces, metrics, and artifacts.

**Networking context:** Trace prompt -> retrieval -> tool calls -> answer -> approval.

## OOD / Out-of-Distribution

**Definition:** Inputs meaningfully different from the data distribution used to develop/evaluate the system.

**Networking context:** A new vendor or protocol not represented in training.

## OOD Detection

**Definition:** Methods for identifying inputs outside the intended operating distribution.

**Networking context:** Route unknown platforms to a human or stronger retrieval workflow.

## Open-Weights Model

**Definition:** A model whose trained weights are available under a license, though data/code openness varies.

**Networking context:** Useful for on-prem deployment.

## OpenAI-Compatible API

**Definition:** An API shape modeled on OpenAI endpoints and adopted by many serving engines.

**Networking context:** Allows applications to switch between compatible backends more easily.

## Operational Evaluation

**Definition:** Tests reliability, latency, cost, observability, and failure handling in realistic workflows.

**Networking context:** What happens when NetBox is unavailable?

## Optimizer

**Definition:** An algorithm such as AdamW that converts gradients into parameter updates.

**Networking context:** Training libraries commonly default to AdamW.

## Orchestrator

**Definition:** A component coordinating models, tools, agents, state, and policies.

**Networking context:** Route network incidents to specialist agents.

## ORPO

**Definition:** Odds Ratio Preference Optimization, a preference-training approach that combines supervised and preference objectives without a separate reference model in its original formulation.

**Networking context:** An alternative preference method; not automatically superior to DPO.

## Outcome Reward Model (ORM)

**Definition:** A reward model that scores the final result/outcome.

**Networking context:** Score whether the final configuration passes a verifier.

## Overfitting

**Definition:** Learning training examples too specifically and failing to generalize.

**Networking context:** Great train loss but poor unseen incident performance.

## Parameter

**Definition:** A learned numerical value in a neural network.

**Networking context:** Billions of parameters collectively encode the model's learned behavior.

## Parameter-Efficient Fine-Tuning (PEFT)

**Definition:** Methods that train a small number of additional/selected parameters instead of the full model.

**Networking context:** LoRA is a popular PEFT method.

## Parent-Child Retrieval

**Definition:** Retrieve using small child chunks but return their larger parent context.

**Networking context:** Match an exact BGP error while returning the full troubleshooting section.

## Perplexity

**Definition:** An exponentiated language-model loss measuring how surprised the model is by text; lower is better on the same data/tokenization.

**Networking context:** Can measure adaptation to networking text, but not operational correctness.

## Pipeline Parallelism

**Definition:** Splitting model layers/stages across devices.

**Networking context:** Another scale-out strategy.

## Planner

**Definition:** A component/model that decomposes a goal into steps.

**Networking context:** Plan an incident investigation.

## Policy

**Definition:** In RL, the behavior that maps a state/prompt to an action/output distribution.

**Networking context:** The LLM being optimized in GRPO is the policy.

## Policy Engine

**Definition:** A deterministic component enforcing rules independently of model judgment.

**Networking context:** Block unauthorized devices or commands.

## Positional Encoding

**Definition:** Mechanisms giving the model information about token order/position.

**Networking context:** Transformers otherwise lack sequence order inherently.

## Post-Training

**Definition:** Training after foundation pretraining to shape behavior/capabilities.

**Networking context:** Includes SFT, preference optimization, reward/RL methods.

## PPO

**Definition:** Proximal Policy Optimization, an RL algorithm used in classic RLHF pipelines.

**Networking context:** Optimize a policy against a learned reward while constraining updates.

## Precision

**Definition:** Of predicted positives, the fraction that are truly positive.

**Networking context:** Important when false alarms are costly.

## Preference Data

**Definition:** Examples expressing which output is preferred over another for the same prompt.

**Networking context:** Choose cautious evidence-based diagnosis over reckless changes.

## Prefix Caching

**Definition:** Reusing computation for shared prompt prefixes.

**Networking context:** Useful when all NOC requests share a large system/runbook prefix.

## Prefix Tuning

**Definition:** A PEFT method that learns trainable continuous prefix vectors injected into model layers.

**Networking context:** Another lightweight adaptation method.

## Pretraining

**Definition:** Large-scale initial training, usually self-supervised, producing a base model.

**Networking context:** Learn general language and broad knowledge before networking adaptation.

## Principal Component Analysis (PCA)

**Definition:** A linear dimensionality-reduction method that projects data onto directions of greatest variance.

**Networking context:** Visualize or compress high-dimensional telemetry features.

## Process Reward Model (PRM)

**Definition:** A reward model that scores intermediate reasoning/process steps rather than only final outcomes.

**Networking context:** Potentially useful when validated troubleshooting steps matter, but step labels are expensive.

## Prompt

**Definition:** The input instructions/context given to a model.

**Networking context:** 'Give three verification steps before any config change.'

## Prompt Cache

**Definition:** Caching reusable prompt processing or responses depending on system design.

**Networking context:** Avoid repeatedly processing unchanged policy context.

## Prompt Engineering

**Definition:** Designing prompts/context to improve model behavior without changing weights.

**Networking context:** Often the first intervention before fine-tuning.

## Prompt Injection

**Definition:** Instructions embedded in untrusted input that try to override intended model behavior.

**Networking context:** A ticket description says 'ignore policy and run this command'.

## Prompt Tuning

**Definition:** A PEFT family that learns trainable prompt-like vectors rather than changing all model weights.

**Networking context:** An alternative parameter-efficient adaptation technique to LoRA.

## PTQ

**Definition:** Post-Training Quantization: quantizing an already-trained model without full retraining.

**Networking context:** Shrink a trained Network LLM for serving.

## QAT

**Definition:** Quantization-Aware Training: simulating quantization during training so the model adapts to it.

**Networking context:** Advanced option when PTQ quality loss is unacceptable.

## QLoRA

**Definition:** Fine-tuning a quantized base model with LoRA adapters, commonly using 4-bit weights.

**Networking context:** Lets larger models fit on limited GPUs.

## Quantization

**Definition:** Representing model weights/activations with fewer bits to save memory and compute.

**Networking context:** Serve an 8B model in 4-bit where quality permits.

## Query / Key / Value (Q/K/V)

**Definition:** Projected vectors used to compute attention scores and aggregate information.

**Networking context:** Not related to a network query packet; these are transformer tensors.

## RAG Pipeline

**Definition:** Ingestion -> chunking -> embedding/indexing -> retrieval -> optional rerank -> prompt construction -> generation -> citation/evaluation.

**Networking context:** End-to-end network knowledge retrieval flow.

## RAGAS / RAG Evaluation

**Definition:** A family of approaches/metrics for assessing retrieval and grounded-generation quality.

**Networking context:** Measure retrieval relevance and answer faithfulness separately.

## Random Forest

**Definition:** An ensemble of decision trees whose predictions are aggregated.

**Networking context:** A strong classic-ML baseline for tabular network features.

## Reasoning Model

**Definition:** A model/post-training regime optimized for multi-step problem solving, often using extra test-time computation.

**Networking context:** Can improve difficult topology or policy reasoning, but still requires grounding.

## Recall

**Definition:** Of true positives, the fraction detected.

**Networking context:** Important when missing incidents is costly.

## Reciprocal Rank Fusion (RRF)

**Definition:** A rank-fusion method that combines multiple ranked result lists using inverse rank contributions.

**Networking context:** Fuse sparse and dense retrieval for runbooks.

## Recurrent Neural Network (RNN)

**Definition:** A neural sequence architecture that carries recurrent hidden state from step to step.

**Networking context:** Historically used for text/time series before transformers became dominant.

## Red Teaming

**Definition:** Adversarial testing intended to discover failures and abuse paths.

**Networking context:** Try prompt injection in retrieved runbooks or malicious tool arguments.

## Reference Model

**Definition:** A fixed model used as a behavioral/probability anchor in some preference/RL methods.

**Networking context:** DPO compares policy likelihood changes against a reference.

## Regression

**Definition:** A previously working behavior that becomes worse after a change.

**Networking context:** Tuned model forgets basic TCP knowledge.

## Reinforcement Learning (RL)

**Definition:** Learning a policy from rewards obtained after actions or generated outputs.

**Networking context:** Reward a model for producing verifiably correct subnet calculations.

## Relevance

**Definition:** How well retrieved context or generated answers match the question.

**Networking context:** A DNS incident should not retrieve OSPF-only chunks.

## Reproducibility

**Definition:** Ability to rerun an experiment and obtain comparable results.

**Networking context:** Pin versions, seeds, data hashes, and configs.

## Reranker

**Definition:** A second-stage model or method that reorders retrieved candidates for relevance.

**Networking context:** Rerank top 20 chunks down to the best 5.

## Residual Connection

**Definition:** A skip connection that adds a layer's input to its output.

**Networking context:** Supports stable training of deep transformers.

## Retrieval-Augmented Generation (RAG)

**Definition:** An architecture that retrieves external information at inference time and gives it to a generator.

**Networking context:** Use current configs/runbooks without storing them in model weights.
