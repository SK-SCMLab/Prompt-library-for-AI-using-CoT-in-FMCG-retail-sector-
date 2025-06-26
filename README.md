# 🎅 Prompt library for AI using CoT in FMCG retail sector
This repository gives a detailed example of prompt engineering using Chain of Thought (CoT) prompting for four common FMCG Retail challenges.

---

## 🙋 Basic Prompting techniques

### Zero-shot prompting
This technique where a user presents a task to an LLM (Large Language Model) without giving the model further examples. Here, the user expects the model to perform the task without a prior understanding, or shot, of the task. Modern LLMs demonstrate remarkable zero-shot performance
- The larger the LLM, the more likely zero-shot prompt will yield effective results
- Instruction tuning can improve zero-shot learning. You can adopt Reinforcement Learning from Human Feedback (RLHF) to scale instruction tuning, aligning modern LLMs to better fit human preferences

### Chain of Thought (CoT) prompting
It breaks down complex reasoning tasks through intermediary reasoning steps. You can use both zero-shot and few-shot prompting techniques with CoT prompts. These are specific to a problem type. You can use the phrase "Think step by step" to invoke CoT reasoning from your ML model
