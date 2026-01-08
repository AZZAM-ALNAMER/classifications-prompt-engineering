# Prompt-Based Customer Message Classification

This project implements a prompt-based customer message classification system using the instruction-tuned **FLAN-T5-Base** model. Instead of training or fine-tuning a traditional classifier, the system relies entirely on **prompt engineering and few-shot in-context learning** to classify customer support messages.

Each input message is classified into:
- **Sentiment**: Positive, Negative, or Neutral
- **Issue Category**: Product Defect, Shipping Delay Inquiry, Feature Request, Positive Feedback, Negative Feedback, or Other

The model produces outputs in a strict, structured format:

Sentiment | Category

---

## 🧠 Project Motivation

Customer support systems receive large volumes of unstructured text every day. Automatically identifying both the **sentiment** and **issue type** of a message can help improve ticket routing, prioritization, and response time.

Traditional machine learning approaches require labeled datasets and model training. This project demonstrates that **instruction-tuned large language models** can perform structured classification tasks **without any fine-tuning**, making the approach suitable for:
- Rapid prototyping
- Low-resource environments
- Exploratory NLP tasks

---

## 🎯 Objectives

- Apply a pretrained instruction-tuned transformer model for text classification
- Design a structured prompt that enforces a fixed output format
- Perform sentiment and category classification without model fine-tuning
- Evaluate model behavior using single-message and batch testing
- Analyze strengths and limitations of prompt-based classification

---

## 🤖 Model & Tools

### Model
- **FLAN-T5-Base** (`google/flan-t5-base`)
- Instruction-tuned sequence-to-sequence transformer
- Strong zero-shot and few-shot generalization capabilities

### Libraries
- `transformers`
- `torch`
- `sentencepiece`
- `accelerate` (optional)

The project was developed in **Python** using **Google Colab** and runs on **CPU or GPU**.

---

## 🏷️ Classification Labels

### Sentiment Labels
- Positive
- Negative
- Neutral

### Issue Categories
- Product Defect
- Shipping Delay Inquiry
- Feature Request
- Positive Feedback
- Negative Feedback
- Other

All labels are explicitly defined inside the prompt to constrain the model’s output space.

---

## ✍️ Prompt Engineering Approach

The system relies entirely on prompt engineering. The prompt includes:

## 🎥 Project Demo

A full walkthrough and explanation of the project is available here:  
  [YouTube Demo Video](https://youtu.be/GD4ZJGH4Wio)

1. A clear task instruction
2. Explicit definitions of allowed sentiment and category labels
3. Multiple labeled examples (few-shot prompting)
4. A strict output format:

