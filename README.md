# 🎅 Prompt library for AI using CoT in FMCG retail sector
This repository gives a detailed example of prompt engineering using Chain of Thought (CoT) prompting for four common FMCG Retail challenges.

---

## 🙋 Basic Prompting techniques

### Zero-shot prompting
This technique where a user presents a task to an LLM (Large Language Model) without giving the model further examples. Here, the user expects the model to perform the task without a prior understanding, or shot, of the task. Modern LLMs demonstrate remarkable zero-shot performance
- The larger the LLM, the more likely zero-shot prompt will yield effective results
- Instruction tuning can improve zero-shot learning. You can adopt Reinforcement Learning from Human Feedback (RLHF) to scale instruction tuning, aligning modern LLMs to better fit human preferences

### Few-shot prompting
This technique where user gives the model contextual information about the required tasks. In this technique, you provide examples of both the task and output you want. Providing this context, or a few shots, in the prompt conditions the model to follow the task guidance closely
- The labels in a few-shot prompt do not need to be correct to improve model performance. Usually, applying random labels outperforms using no labels at all. However, the label space and distribution of the input text specified by the demonstrations are important. The use of term label in this context refers to the output of the prompt examples. The sentiment expressed by the statement in a "prompt example" is an example of a label
- If you have access to a large set of examples, use techniques to obey the token limits of your model and dynamically populate prompt templates. You can use an example selector that is based on semantic similarity to help

### Chain of Thought (CoT) prompting
It breaks down complex reasoning tasks through intermediary reasoning steps. You can use both zero-shot and few-shot prompting techniques with CoT prompts. These are specific to a problem type. You can use the phrase "Think step by step" to invoke CoT reasoning from your ML model

---

## 🦸 Prompt 1: Stock outs of high movement SKUs

### Introduction
Reason through root causes and purpose actionable recommendations

### Context
FMCG retailers struggle with recurring stock-outs for fast-moving products
- SKU Sales history: [Sales data]
- Inventory status: [Inventory data]
- Lead times & Reorder points: [Reorder data]

### Think aloud (chain of thought)
1. Identify SKUs with recurring stockouts
2. Assess root causes (demand fluctuations, lead times, order quantity, forecasting errors)
3. Suggest actionable recommendations for SKU replenishment, safety stock policies, and supplier collaboration

### Final output
- List of recurring stock-out SKUs
- Root cause of each SKU
- Specific actionable recommendations

---

## 🧑‍🚒 Excess & Obsolete inventory

### Introduction
Think clearly about surplus stock and suggest ways to reduce waste

### Context
Excess or obsolete inventory is tying up working capital and causing write-offs
- SKU Movement & Ageing: [Movement data]
- Sell-through rate: [sell through data]
- Expiry date: [expiry dates]

### Think aloud (chain of thought)
1. Identify SKUs with low turnover or nearing expiry
2. Assess the root causes (over-ordering, forecasting error, slow sales)
3. Suggest targeted clearance strategies (promotions, discounts, bundles)
4. Propose long-term measures (forecasting adjustments, reivew of MOQ, vendor agreements)

### Final output
- List of slow-moving and obsolete SKUs
- Clearance and long-term prevention recommendations

---

## 🏃 Price optimization against competition

### Introduction
Compare pricing and suggest competitive pricing strategies

### Context
Customers are shifting to competitors due to pricing discrepancies across key SKUs
- SKU Prices across competitors: [competitor data]
- Sales and profit margins: [sales profit data]
- Customer segments and price sensitivity: [customer data]

### Think aloud (chain of thought)
1. Identify SKUs with significant pricing gaps vs competitors
2. Evaluate the impact of pricing differences on sales and margins
3. Identify SKUs where price adjustments can increase sales without compromising margins
4. Suggest competitive pricing strategies for key SKUs

### Final output
- SKU-wise pricing discrepancy and impact
- SKU-wise pricing recommendations
- Strategies for aligning pricing with customer expectations

---

## 👓 Late deliveries from distributors

### Introduction
Pinpoint delays and purpose actionable improvements

### Context
Frequent delays from distributors affect product availability and customer satisfaction
- Distributor Delivery times: [delivery data]
- SKU Service level agreements: [SLA data]
- Frequency and patterns of late deliveries: [late delivery data]

### Think aloud (chain of thought)
1. Identify SKUs with recurring delays and compare actual vs SLA times
2. Analyze root causes (distributor constraints, order quantity, transportation)
3. Recommend actionable improvements (alternate distributors, lead-time adjustments, buffer stock policies)
4. Suggest metrics and reporting measures for ongoing performance monitoring

### Final output
- SKU-wise delay and root cause summary
- Recommend corrective and preventive measures
- Suggested metrics for performance monitoring

---

## 👒 Requirements
- Essentials of Prompt engineering
- Supply Chain concepts

---
*"A well-crafted prompt is like a key that unlocks the true potential of AI"*
