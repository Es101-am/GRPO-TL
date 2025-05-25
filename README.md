# GRPO-TL

# 🧠 GRPO-TL: Reasoning-Focused Fine-Tuning of TinyLlama with GRPO

This project demonstrates how to fine-tune the [TinyLlama](https://huggingface.co/TinyLlama) model using **GRPO (Generalized Reinforcement Pretraining Objective)** to enhance **step-by-step reasoning** skills, especially for grade-school math problems.

---

## 📌 Highlights

- ✅ **Model**: TinyLlama 1.1B (or any causal LM)
- 📚 **Dataset**: [GSM8K](https://huggingface.co/datasets/gsm8k) — natural language math problems
- 🎯 **Objective**: Improve reasoning via <think>...</think> and <answer>...</answer> structure
- 🧪 **Reward Function**: Custom scoring based on use of reasoning keywords, tags, and correctness

---

## 🗂️ Project Structure

| File | Description |
|------|-------------|
| `GRPO.ipynb` | Main notebook for formatting data, training with GRPO, and testing TinyLlama |
| `gsm8k_200_formatted.json` | Preprocessed dataset (first 200 samples) with reasoning prompts |
| `reward_function.py` *(optional)* | Custom reward calculation for GRPO (embedded in notebook) |

---

## 🚀 How It Works

### 🧾 Prompt Format

```text
User: [GSM8K question] Please show your reasoning inside <think> </think> tags and your final answer inside <answer> </answer> tags.
Assistant: Let me solve this step by step.
<think> ...reasoning steps... </think>
<answer> final result </answer>
