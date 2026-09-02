# Network LLM Engineering Glossary — Part 2

Terms DPO through Long-Term Memory.

## DPO

**Definition:** Direct Preference Optimization, which trains directly from chosen/rejected pairs without an explicit reward-model-plus-RL loop.

**Networking context:** Prefer safe troubleshooting responses.

## Embedding

**Definition:** A dense numeric vector representing a token, sentence, document, or other object.

**Networking context:** Embed an incident query and RFC chunks for semantic retrieval.

## Embedding Model

**Definition:** A model designed to produce vector representations useful for similarity/search.

**Networking context:** Used in RAG before the generative LLM is called.

## Encoder

**Definition:** Transformer component that builds contextual representations of an input sequence.

**Networking context:** BERT-style models are encoder-centric.

## Encoder-Decoder Model

**Definition:** A model with separate input encoder and output decoder.

**Networking context:** T5 is a classic example.

## Environment

**Definition:** In RL/agents, the external system that receives actions and returns observations/rewards.

**Networking context:** A network digital twin can act as a training/evaluation environment.

## Epoch

**Definition:** One full pass through the training dataset.

**Networking context:** Three epochs means each training example is seen roughly three times.

## Evaluation Harness

**Definition:** Reusable code that runs a model on test cases and computes/stores results.

**Networking context:** Required before each adapter release.

## Event-Driven Architecture

**Definition:** Systems reacting to events/messages rather than only user requests.

**Networking context:** Kafka event triggers AI triage when an interface flaps.

## Exact Match

**Definition:** Metric requiring generated output to match the reference exactly.

**Networking context:** Useful for canonical structured answers, too strict for explanations.

## Experiment Tracking

**Definition:** Recording parameters, metrics, artifacts, and versions for training runs.

**Networking context:** Compare rank 8 vs 16 adapters reproducibly.

## Expert System

**Definition:** A rule/knowledge-based system designed to mimic specialist decisions in a narrow domain.

**Networking context:** Traditional network troubleshooting decision trees are expert systems.

## F1 Score

**Definition:** Harmonic mean of precision and recall.

**Networking context:** Balances false positives and false negatives.

## Faithfulness

**Definition:** Whether an answer is supported by supplied evidence/context.

**Networking context:** Do claims match retrieved telemetry/runbooks?

## Feature

**Definition:** An input variable or learned representation used by a model.

**Networking context:** Classic ML might use packet-loss percentage as a feature.

## Feed-Forward Network (FFN/MLP)

**Definition:** Per-token neural layers inside a transformer block after attention.

**Networking context:** A large share of model parameters often lives here.

## Few-Shot Prompting

**Definition:** Including a small number of examples in the prompt.

**Networking context:** Show two incident-summary examples before asking for a third.

## Fine-Tuning

**Definition:** Updating pretrained model parameters for a narrower task/domain/behavior.

**Networking context:** Teach a model a troubleshooting format.

## Fine-Tuning Corpus

**Definition:** The collection of examples actually used to update a model during adaptation.

**Networking context:** Keep it versioned, reviewed, and separate from the golden test set.

## Fine-Tuning Job

**Definition:** A managed or local process that trains an adapted model from a dataset/config.

**Networking context:** Track dataset hash, base model, hyperparameters, and output adapter.

## Fine-Tuning vs RAG

**Definition:** A design distinction: fine-tuning changes behavior/weights; RAG changes supplied context/facts.

**Networking context:** Stable troubleshooting style vs today's BGP table.

## FlashAttention

**Definition:** Optimized exact attention implementations designed to reduce memory traffic and improve speed.

**Networking context:** Useful for longer sequences and training efficiency.

## Foundation Model

**Definition:** A large broadly trained model that can be adapted to many downstream tasks.

**Networking context:** A general LLM can later be adapted to networking.

## FP16

**Definition:** 16-bit floating point.

**Networking context:** Lower memory, limited numerical range.

## FP32

**Definition:** 32-bit floating point.

**Networking context:** High precision, high memory.

## FSDP

**Definition:** Fully Sharded Data Parallel, which shards parameters/gradients/optimizer state across workers.

**Networking context:** Used to train larger models efficiently.

## Full Fine-Tuning

**Definition:** Updating all or most model weights.

**Networking context:** Memory-intensive compared with PEFT.

## Function Calling

**Definition:** A common term for structured tool invocation by a model.

**Networking context:** Tool schema defines arguments and expected result shape.

## Generalization

**Definition:** Performance on unseen examples drawn from the intended task distribution.

**Networking context:** Can the model diagnose a new topology, not memorize examples?

## Generative Adversarial Network (GAN)

**Definition:** A generative framework with a generator and discriminator trained adversarially.

**Networking context:** Important AI terminology, though not a primary architecture for text LLMs.

## Generative AI

**Definition:** Models that generate new content such as text, code, images, audio, or structured data.

**Networking context:** Generate a change plan, incident summary, or configuration explanation.

## GGUF

**Definition:** A model file format/ecosystem widely used with llama.cpp-compatible runtimes and quantized model distributions.

**Networking context:** Run quantized local models on engineer laptops.

## Golden Dataset

**Definition:** A small, carefully curated set of trusted evaluation examples.

**Networking context:** Expert-reviewed incidents used for release gates.

## GPTQ

**Definition:** A post-training weight quantization family using calibration/optimization to reduce quantization error.

**Networking context:** Compress a GPU-served open model after training.

## Gradient

**Definition:** The direction and magnitude of change in loss with respect to parameters.

**Networking context:** Backpropagation computes gradients for weight updates.

## Gradient Accumulation

**Definition:** Summing gradients across several mini-batches before one optimizer step.

**Networking context:** Simulates a larger effective batch on a smaller GPU.

## Gradient Boosting

**Definition:** An ensemble technique that sequentially builds weak learners to correct previous errors.

**Networking context:** Often strong on structured operational/tabular datasets.

## Gradient Checkpointing

**Definition:** Recomputing activations during backward pass instead of storing all of them.

**Networking context:** Trades compute for lower training memory.

## Gradient Descent

**Definition:** A family of optimization methods that move parameters in a direction that reduces loss.

**Networking context:** The conceptual basis of neural-network training.

## GraphRAG

**Definition:** RAG approaches that use graph structure, graph-derived context, or graph search in retrieval/generation.

**Networking context:** Retrieve topology paths and dependencies before diagnosing an outage.

## Greedy Decoding

**Definition:** Always choosing the highest-probability next token.

**Networking context:** Deterministic but not always globally optimal.

## Grounding

**Definition:** Constraining or supporting a model answer with external evidence.

**Networking context:** Ground an outage diagnosis in telemetry and topology.

## GRPO

**Definition:** Group Relative Policy Optimization, an RL method comparing rewards among multiple completions sampled for a prompt.

**Networking context:** Useful when multiple candidate network answers can be verifiably scored.

## Guardrail

**Definition:** A control limiting unsafe or invalid model behavior.

**Networking context:** Block commands that exceed allowed change scope.

## Hallucination

**Definition:** A generated claim that is unsupported, fabricated, or incorrect.

**Networking context:** Inventing a nonexistent BGP neighbor state.

## Handoff

**Definition:** Transfer of a task/control/context from one agent or component to another.

**Networking context:** NOC agent hands a suspected firewall issue to a security agent.

## Human Evaluation

**Definition:** People judge outputs against a rubric.

**Networking context:** Essential for nuanced network troubleshooting quality.

## Human-in-the-Loop (HITL)

**Definition:** A workflow requiring human review/approval at selected points.

**Networking context:** Engineer approves a production network change.

## Hybrid Retrieval

**Definition:** Combining sparse and dense retrieval.

**Networking context:** Useful for networking because exact CLI terms and semantic meaning both matter.

## HyDE

**Definition:** Hypothetical Document Embeddings: retrieval using an embedding of a generated hypothetical answer/document.

**Networking context:** Expand a vague incident query before finding real troubleshooting documents.

## Hyperparameter

**Definition:** A training setting chosen by the practitioner rather than learned directly.

**Networking context:** Learning rate, LoRA rank, batch size, epochs.

## IA3

**Definition:** A PEFT method that learns small scaling vectors applied to model activations.

**Networking context:** Very parameter-efficient alternative to LoRA for some tasks.

## Idempotency

**Definition:** Property where repeating an operation produces no additional unintended effect.

**Networking context:** Important for network automation retries.

## In-Context Learning (ICL)

**Definition:** A model performing a task from instructions/examples placed in the prompt, without updating weights.

**Networking context:** Show two incident examples in the prompt and ask for a third.

## Indirect Prompt Injection

**Definition:** Prompt injection entering through retrieved/tool-provided content rather than the user's direct prompt.

**Networking context:** A malicious wiki page manipulates the agent.

## Inference

**Definition:** Running a trained model to produce predictions or generations without updating its weights.

**Networking context:** Ask the network assistant a question in production.

## Inference Endpoint

**Definition:** A network service exposing model inference.

**Networking context:** The application calls a REST API instead of loading weights directly.

## Inference Scaling

**Definition:** Increasing computation at inference time to improve solution quality.

**Networking context:** Generate/search/verify multiple candidates for a difficult topology problem.

## Inference-Time RAG

**Definition:** Retrieval performed for each request without changing model weights.

**Networking context:** Ideal for current topology and runbooks.

## Instruction Tuning

**Definition:** Post-training on instruction/response examples so a model follows user requests better.

**Networking context:** SFT is commonly used to instruction-tune an LLM.

## Instruction-Tuned Model

**Definition:** A model post-trained to follow human instructions/dialogue.

**Networking context:** Usually the practical starting point for a network assistant.

## INT4 / 4-bit

**Definition:** Four-bit weight representation used for aggressive compression.

**Networking context:** Common in QLoRA-style training/inference.

## INT8

**Definition:** 8-bit integer representation used by some quantization methods.

**Networking context:** Reduces memory compared with FP16/BF16.

## k-Nearest Neighbors (k-NN)

**Definition:** A method that predicts from the labels/values of nearby examples in feature space.

**Networking context:** A conceptual cousin of nearest-neighbor vector retrieval.

## KL Divergence

**Definition:** A measure of difference between probability distributions.

**Networking context:** Used to discourage a policy from drifting too far from a reference model.

## Knowledge Distillation

**Definition:** Training a student to imitate teacher outputs/distributions or behavior.

**Networking context:** Compress a larger network model into an 8B model.

## Knowledge Graph

**Definition:** A graph of entities and typed relationships representing domain knowledge.

**Networking context:** Router -> peers_with -> Router; Interface -> member_of -> VRF.

## KTO

**Definition:** Kahneman-Tversky Optimization, a preference-alignment method that can learn from desirable/undesirable examples without requiring paired preferences in the same way as DPO.

**Networking context:** An alternative post-training method supported by modern TRL.

## KV Cache

**Definition:** Cached attention key/value tensors for previous tokens during autoregressive generation.

**Networking context:** Speeds generation but consumes memory.

## Label

**Definition:** The target answer/class associated with a supervised example.

**Networking context:** Ticket class = WAN, LAN, Security, DNS, etc.

## Large Language Model (LLM)

**Definition:** A neural language model with many parameters trained to predict or model token sequences at large scale.

**Networking context:** Used to explain CLI output or reason over troubleshooting evidence.

## Latency

**Definition:** Time required to produce a result.

**Networking context:** Critical for interactive NOC workflows.

## Latent Space

**Definition:** An internal representation space in which models encode abstract factors/features.

**Networking context:** Embeddings and hidden states live in learned representation spaces.

## Latent Variable

**Definition:** An unobserved variable inferred by a model to explain observed data.

**Networking context:** Used broadly in probabilistic/generative modeling.

## Layer

**Definition:** A stage/block of neural computation.

**Networking context:** A transformer contains many repeated blocks.

## Layer Normalization

**Definition:** Normalization used inside transformer architectures.

**Networking context:** Helps stabilize activations.

## Learning Rate

**Definition:** A hyperparameter controlling update size.

**Networking context:** Too high can destabilize fine-tuning; too low can learn slowly.

## Least Privilege

**Definition:** Giving a model/agent only the permissions required for its task.

**Networking context:** Read-only telemetry tool for diagnosis.

## LLM-as-a-Judge

**Definition:** Using another LLM to score outputs against criteria.

**Networking context:** Scalable but can inherit judge bias and needs validation.

## LLMOps

**Definition:** Operational practices for versioning, evaluating, deploying, observing and governing LLM applications and model artifacts.

**Networking context:** CI tests prompt/RAG/model/tool changes before AI NOC release.

## Logit

**Definition:** An unnormalized score produced by the model for a possible next token.

**Networking context:** Softmax converts logits into probabilities.

## Logits Distillation

**Definition:** Training a student to match teacher probability distributions/logits.

**Networking context:** Richer signal than only copying final text when logits are available.

## Long-Term Memory

**Definition:** Persistent state across tasks/sessions.

**Networking context:** Past incident outcomes stored in a database.
