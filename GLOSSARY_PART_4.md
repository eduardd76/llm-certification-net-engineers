# Network LLM Engineering Glossary — Part 4

Terms Retriever through Zero-Shot Prompting.

## Retriever

**Definition:** The component that selects documents/chunks relevant to a query.

**Networking context:** The R in a RAG pipeline.

## Reward

**Definition:** A numeric signal that says how desirable an outcome is.

**Networking context:** 1.0 when a subnet JSON answer is exactly correct.

## Reward Model

**Definition:** A learned model that scores outputs according to preferences.

**Networking context:** Score which troubleshooting answer follows operational best practices.

## RLAIF

**Definition:** Reinforcement Learning from AI Feedback.

**Networking context:** An AI judge helps create preference/reward signals.

## RLHF

**Definition:** Reinforcement Learning from Human Feedback: a family of methods using human preferences/rewards to optimize model behavior.

**Networking context:** Classic pipeline: preferences -> reward model -> RL policy optimization.

## RLOO

**Definition:** REINFORCE Leave-One-Out, an online RL method using leave-one-out baselines to reduce variance.

**Networking context:** A post-training RL alternative available in modern tooling.

## RLVR

**Definition:** Reinforcement Learning with Verifiable Rewards.

**Networking context:** Subnet math or config-schema tasks can have deterministic reward functions.

## Rollback

**Definition:** Restoring a known-good prior state after a failed change.

**Networking context:** Mandatory control for autonomous remediation.

## Rollout

**Definition:** A generated trajectory/completion sampled from a policy during RL.

**Networking context:** Generate several candidate subnet answers for reward scoring.

## RoPE

**Definition:** Rotary Position Embedding, a common positional technique in modern LLMs.

**Networking context:** A model architecture detail affecting long-context behavior.

## Safety Evaluation

**Definition:** Tests whether the system avoids harmful/unauthorized behavior.

**Networking context:** Does it refuse to invent evidence or bypass approval?

## Sandbox

**Definition:** An isolated environment for executing risky or untrusted operations.

**Networking context:** Validate generated scripts away from production.

## Schema Validation

**Definition:** Checking structured model output against a formal schema.

**Networking context:** Reject malformed remediation JSON.

## Search / Tree Search

**Definition:** Exploring multiple candidate reasoning/action paths before selecting an answer.

**Networking context:** Can be paired with verifiers for complex network planning.

## Seed

**Definition:** A value controlling pseudo-random processes for repeatability.

**Networking context:** Use the same split/order when comparing experiments.

## Self-Attention

**Definition:** Attention where queries, keys, and values come from the same sequence.

**Networking context:** Core operation in decoder-only LLMs.

## Self-Consistency

**Definition:** Generate multiple solutions and choose/aggregate consistent results.

**Networking context:** Useful only if combined with strong verification; repetition is not proof.

## Self-Querying Retrieval

**Definition:** Turning a natural-language request into semantic search plus structured metadata filters.

**Networking context:** Filter incidents by vendor, date, device class, and topic.

## Self-Supervised Learning

**Definition:** Learning targets derived from the data itself rather than human labels.

**Networking context:** LLM pretraining predicts missing/next tokens from raw text.

## Semantic Search

**Definition:** Search based on meaning rather than exact keyword matching.

**Networking context:** 'BGP peer won't establish' can retrieve docs about TCP/179 and neighbor state.

## Sequence Length

**Definition:** Number of tokens processed in one example/context.

**Networking context:** Long CLI outputs consume context and GPU memory.

## Serving

**Definition:** Exposing a model for inference through an application/API.

**Networking context:** Run a local OpenAI-compatible endpoint.

## Short-Term Memory

**Definition:** Temporary state for the current interaction/task.

**Networking context:** Current hypotheses and tool results.

## Small Language Model (SLM)

**Definition:** A smaller language model optimized for lower cost, latency, or local deployment.

**Networking context:** A 0.5B–8B model may be enough for a narrow on-prem NOC task.

## Softmax

**Definition:** A function that converts a vector of logits into a probability distribution.

**Networking context:** Used to obtain next-token probabilities.

## Source of Truth (SoT)

**Definition:** Authoritative system holding operational facts.

**Networking context:** NetBox/Nautobot can ground device and topology facts.

## Sparse Model

**Definition:** A model where only part of the parameters/operations are active for a given input.

**Networking context:** Many MoE models are sparse.

## Sparse Retrieval

**Definition:** Retrieval using sparse term features such as BM25.

**Networking context:** Strong for exact terms like error codes, interface names, and RFC numbers.

## Speculative Decoding

**Definition:** A serving technique where a smaller draft model proposes tokens that a larger model verifies.

**Networking context:** Can reduce latency.

## Speech-to-Text (ASR)

**Definition:** Automatic speech recognition.

**Networking context:** Convert a spoken outage bridge into text.

## State

**Definition:** Structured information representing where an agentic workflow currently is.

**Networking context:** Incident ID, evidence, hypotheses, completed checks.

## Stream Processing

**Definition:** Continuous processing of event streams.

**Networking context:** Compute anomaly features from telemetry in near-real time.

## Structured Output

**Definition:** Model output constrained to a schema such as JSON.

**Networking context:** Return diagnosis, evidence, next_checks, confidence.

## Student Model

**Definition:** The smaller model being trained to imitate the teacher.

**Networking context:** Deploy locally for low latency.

## Supervised Fine-Tuning (SFT)

**Definition:** Fine-tuning on prompt/target examples using supervised next-token loss.

**Networking context:** Train on expert troubleshooting answers.

## Supervised Learning

**Definition:** Learning from examples that include desired outputs or labels.

**Networking context:** Train a ticket classifier from labeled incidents.

## Support Vector Machine (SVM)

**Definition:** A supervised method that finds a separating boundary with maximum margin in feature space.

**Networking context:** Can classify small structured datasets without an LLM.

## Symbolic AI

**Definition:** AI based on explicit symbols, rules, logic, and search rather than learned neural representations.

**Networking context:** Routing policy validators and logic engines can complement LLMs.

## Synthetic Data

**Definition:** Training/evaluation data generated programmatically or by models.

**Networking context:** Generate topology variations, then validate them deterministically.

## System Prompt

**Definition:** High-priority conversational instructions defining assistant behavior.

**Networking context:** Set network safety and output-format rules.

## Teacher Model

**Definition:** The stronger model supplying targets/signals for distillation.

**Networking context:** A frontier model can label sanitized network cases.

## Telemetry

**Definition:** Machine-generated measurements/state from infrastructure.

**Networking context:** Interface counters, BGP state, latency, logs.

## Temperature

**Definition:** A decoding parameter that changes the sharpness/randomness of token sampling.

**Networking context:** Use low temperature for deterministic troubleshooting.

## Tensor

**Definition:** A multidimensional array used to store model data and activations.

**Networking context:** Token embeddings are represented as tensors.

## Tensor Parallelism

**Definition:** Splitting tensor operations/model dimensions across devices.

**Networking context:** Common for large-model inference/training.

## Termination Condition

**Definition:** Rule that stops an agent loop.

**Networking context:** Stop after evidence is sufficient, max steps reached, or human approval required.

## Test Split

**Definition:** Held-out data reserved for final evaluation.

**Networking context:** Avoid optimizing repeatedly against it.

## Test-Time Compute

**Definition:** Extra inference computation used to improve answers, such as longer reasoning/search or multiple candidates.

**Networking context:** Generate several diagnoses and verify them.

## Text-to-Speech (TTS)

**Definition:** Generating spoken audio from text.

**Networking context:** Voice assistant for field engineers.

## Throughput

**Definition:** Amount of work processed per unit time.

**Networking context:** Tokens/sec or requests/sec.

## Time to First Token (TTFT)

**Definition:** Delay before the first generated token is returned.

**Networking context:** A key perceived-latency metric.

## Time-Series Model

**Definition:** A model designed for ordered measurements over time.

**Networking context:** Forecast utilization or detect temporal anomalies in telemetry.

## Timeout

**Definition:** Maximum allowed duration for a tool/agent operation.

**Networking context:** Prevents a stuck telemetry query from blocking the workflow.

## Token

**Definition:** A unit of text processed by a language model; it may be a word, subword, symbol, or byte sequence.

**Networking context:** `Ethernet1/49` may split into multiple tokens.

## Token Throughput

**Definition:** Number of input/output tokens processed per second.

**Networking context:** Used to compare inference serving systems.

## Tokenizer

**Definition:** Software that converts text into token IDs and back.

**Networking context:** Different model families can tokenize CLI syntax differently.

## Tool Calling

**Definition:** A model producing a structured request to invoke an external function/tool.

**Networking context:** Call `get_bgp_neighbors(router)` instead of guessing state.

## Tool Schema

**Definition:** A machine-readable definition of a tool name, arguments, and types.

**Networking context:** `get_interface_counters(device, interface)`.

## Tool-Use Dataset

**Definition:** Training examples that include tool calls and tool results.

**Networking context:** Teach a model when and how to query `get_bgp_neighbors`.

## Top-k Sampling

**Definition:** Sampling only from the k highest-probability next tokens.

**Networking context:** A decoding control, not a training method.

## Top-p / Nucleus Sampling

**Definition:** Sampling from the smallest token set whose cumulative probability reaches p.

**Networking context:** Useful for creative generation; less desirable for deterministic ops.

## Trace

**Definition:** A record of steps/events through an AI workflow.

**Networking context:** See which telemetry call supported a diagnosis.

## Train Split

**Definition:** Examples used to update weights.

**Networking context:** Must not contain held-out test prompts.

## Training

**Definition:** The process of updating model parameters to reduce an objective/loss.

**Networking context:** Train on network incident examples.

## Trajectory

**Definition:** A sequence of states, actions/tool calls, observations, and outputs in an agent/RL task.

**Networking context:** A complete troubleshooting run can be a trajectory.

## Transfer Learning

**Definition:** Reusing knowledge from a pretrained model for a different downstream task.

**Networking context:** Fine-tuning a general LLM for networking is transfer learning.

## Transformer

**Definition:** A neural architecture built around attention and feed-forward blocks.

**Networking context:** The dominant architecture behind current LLMs.

## Uncertainty

**Definition:** Lack of certainty in predictions, evidence, model knowledge, or environment state.

**Networking context:** Should drive escalation and additional evidence collection.

## Underfitting

**Definition:** Model/training capacity is insufficient to fit the desired patterns.

**Networking context:** Both training and eval performance remain weak.

## Unsupervised Learning

**Definition:** Learning structure from data without explicit target labels.

**Networking context:** Cluster telemetry patterns without predefined incident classes.

## Validation Split

**Definition:** Examples used during model development/hyperparameter selection.

**Networking context:** Used to compare experiments.

## Vector

**Definition:** An ordered list of numbers.

**Networking context:** An embedding may be a 768-dimensional vector.

## Vector Database

**Definition:** A system optimized to store embeddings and retrieve nearest neighbors.

**Networking context:** Retrieve relevant runbooks from a network knowledge base.

## Vector Store

**Definition:** Storage/index used for vector similarity retrieval; may be a vector DB or library index.

**Networking context:** FAISS index of runbook embeddings.

## Verifier

**Definition:** A deterministic or model-based component that checks candidate outputs/actions.

**Networking context:** Validate syntax, policy, reachability, or subnet math.

## Vision-Language Model (VLM)

**Definition:** A multimodal model combining vision and language understanding/generation.

**Networking context:** Analyze topology diagrams or screenshots.

## vLLM

**Definition:** An LLM inference/serving engine focused on high-throughput generation and efficient memory use.

**Networking context:** Serve a local network model behind an API.

## Vocabulary

**Definition:** The set of token IDs the tokenizer/model can represent directly.

**Networking context:** A model's output softmax spans its vocabulary.

## Weight

**Definition:** A parameter used in a neural computation, often stored in matrices.

**Networking context:** Fine-tuning changes some or all model weights.

## World Model

**Definition:** A learned model intended to predict aspects of an environment's dynamics/state transitions.

**Networking context:** Could approximate network behavior, but high-stakes changes still need authoritative verification.

## Zero-Shot Prompting

**Definition:** Asking a model to perform a task without examples in the prompt.

**Networking context:** 'Classify this incident into WAN/LAN/DNS/Security.'
