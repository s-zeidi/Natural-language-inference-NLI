# Natural Language Inference in Biomedical Domain: Enhancing Entailment Classification

## Overview
This repository contains the code, experiments, and fine-tuned models from my Master's thesis on **entailment classification in biomedical domain tasks**.  
We investigate multiple **large language models (LLMs)** under different prompting strategies, followed by fine-tuning, to improve performance on biomedical NLI tasks.

## Dataset
Our experiments use the **NLI4CT dataset** from *SemEval-2024 Task 2*, which consists of clinical trial reports paired with hypotheses and labeled as either **entailment** or **contradiction**.  
The dataset was pre-processed to extract relevant trial sections and formatted for zero-shot, few-shot, and fine-tuning scenarios.

## Models
The following LLMs were evaluated:
- **LLaMA 2**
- **Qwen 2**
- **Mistral**
- **DeepSeek R1 Distill Qwen**

We also experimented with **DeepSeek R1** for **augmenting structured reasoning outputs** to enrich our training dataset. However, the reasoning column produced by DeepSeek R1 was not of sufficient quality for direct use. We are continuing this work by testing other models such as **GPT** and **Gemini** for generating higher-quality reasoning chains.

## Experimental Settings
We explored:
- **Zero-shot prompting**
- **Two-shot prompting**
- **Chain-of-Thought (CoT) reasoning**
- **CoT + Two-shot prompting**
- **Fine-tuning with LoRA**
- **Data augmentation with structured reasoning outputs**

## Results
The performance of each model was compared across all prompting strategies, with final fine-tuned models yielding the best F1-scores.

For now, Qwen 2 7B was the best within these experiments.
The final model is now publicly available on my Hugging Face page.
https://huggingface.co/sepzyd/Qwen2-biomed-nli-EEC
