# Efficient Fine-Tuning of LLaMA 3.2-1B for Sentiment Analysis

---

## Overview

This repository presents an efficient fine-tuning framework for adapting the **LLaMA 3.2-1B** model to multiple sentiment analysis tasks across diverse domains and languages. The project leverages **parameter-efficient fine-tuning** techniques to achieve strong downstream performance while maintaining low computational and memory overhead.

The model is adapted to the following sentiment analysis tasks:

- Multilingual sentiment classification  
- Financial sentiment analysis on Twitter data  
- Movie review sentiment analysis  

To ensure scalability and efficiency, we employ **LoRA-based fine-tuning** using `peft` along with **low-bit quantization** using `bitsandbytes`.

---

## Key Techniques

- **Low-Rank Adaptation (LoRA):** Fine-tuning only a small subset of parameters while freezing the base model.
- **Quantization:** 8-bit / 4-bit quantization to reduce memory footprint and speed up training.
- **Task-Specific Adaptation:** Fine-tuning the model for individual downstream sentiment tasks.

---

## Datasets

The model is trained and evaluated on the following datasets:

- **Multilingual Sentiment Dataset:** `tyqiangz/multilingual-sentiments`
- **Financial Twitter Sentiment:** Zero-shot Twitter financial sentiment dataset
- **Movie Reviews:** Stanford NLP IMDB sentiment dataset

---

## Training Strategy

- The multilingual and financial Twitter sentiment tasks are fine-tuned using **LoRA**.
- The IMDB sentiment task is fine-tuned directly for domain adaptation.
- Quantization is applied using the `bitsandbytes` library for memory-efficient training.

---

## Model Architecture

- **Base Model:** LLaMA 3.2-1B  
- **Fine-Tuning Method:** LoRA  
- **Quantization:** 8-bit / 4-bit (bitsandbytes)

---

## Use Cases

- Multilingual opinion mining  
- Financial market sentiment analysis  
- Review-based recommendation systems  
- Low-resource or edge-device NLP deployments  

---

## Future Work

- Multi-task joint training across sentiment datasets
- Evaluation on low-resource languages
- Adapter fusion and prompt-based fine-tuning
- Deployment on edge devices

---

## Acknowledgements

This project builds upon open-source contributions from the HuggingFace ecosystem and the research community on parameter-efficient fine-tuning.

---


