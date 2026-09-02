# Instructor Guide

## Teaching model
Use a 20–30 minute concept block followed by a 30–60 minute lab block.
Do not lecture for multiple hours without a practical checkpoint.

## Recommended sequencing
- Foundations: terminology + toy code.
- Context: retrieval before fine-tuning.
- Adaptation: baseline -> data -> LoRA -> eval.
- Post-training: preferences and verifiable reward only after SFT.
- Agents: tools/state/termination before multi-agent.
- Production: digital twin, policy, observability, release gates.
- Capstone: architecture first, code second.

## Socratic questions
Ask repeatedly:
- What assumption are you making?
- Which fact is current and where does it come from?
- Why is this an LLM problem?
- What can be verified deterministically?
- What is the blast radius if the model is wrong?
- What happens when the tool is unavailable?
- What data could leak between train and test?
- Which metric would tell us this is actually better?

## Practical exam supervision
Learners may use official docs and their own course notes.
They may not use a prebuilt answer key or another student's submission.
The goal is professional problem solving, not memory testing.

## Grading
Use the master rubric plus exam-specific criteria.
A learner who chooses a simpler, safer architecture can outscore a learner with a complex multi-agent design.
