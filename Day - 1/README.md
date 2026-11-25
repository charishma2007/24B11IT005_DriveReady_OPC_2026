# Day 1 – Agentic AI: Flower Shop AI Assistant 🌸

## 📌 Task Overview

The Day 1 task focuses on developing a domain-specific AI assistant using Large Language Models (LLMs), Prompt Engineering, and Prompt Guard.

I developed an AI-powered customer assistant for **Bloom & Bliss Flower Shop** that answers customer queries, recommends bouquets, provides pricing details, and follows predefined business rules.

## 🎯 Objectives

- Understand Large Language Models and their integration.
- Connect an LLM using the Groq API.
- Design structured system prompts using Role, Facts, Rules, and Format.
- Generate accurate and domain-specific responses.
- Explore prompt injection detection using Prompt Guard.

## 🛠️ Technologies Used

- Python
- Google Colab
- LangChain
- Groq API
- GPT-OSS-120B
- Llama Prompt Guard 2

## 🌷 Features

- Flower and bouquet recommendations.
- Product information and pricing.
- Budget-based suggestions.
- Occasion-based recommendations.
- Customized bouquet suggestions.
- Flower care and maintenance tips.
- Restricted responses to flower-related queries.

## ⚙️ Implementation

### Step 1: Install Required Libraries

Installed the `langchain_groq` library to integrate the Groq LLM with Python.

### Step 2: Configure API Key

Stored the API key securely in Google Colab Secrets and retrieved it using `userdata`.

### Step 3: Initialize the LLM

Configured the ChatGroq model with:

- Model: `openai/gpt-oss-120b`
- Temperature: `0`

### Step 4: Design the System Prompt

Created a structured system prompt containing four components:

| Component | Description |
|---|---|
| Role | Defines the AI as a flower shop assistant. |
| Facts | Contains flower varieties, prices, shop timings and services. |
| Rules | Controls the assistant's behaviour and prevents incorrect information. |
| Format | Defines the response style, tone and length. |

### Step 5: Generate AI Responses

Created an `ask()` function that accepts customer queries, combines them with the system prompt, and generates responses using the LLM.

### Step 6: Test the AI Assistant

Tested the assistant with the following query:

**Input:** Which flowers are famous in your shop?

**Output:**

- Red Roses Bouquet – Rs. 399
- Pink Roses Bouquet – Rs. 499
- Sunflower Bouquet – Rs. 449
- Mixed Flowers Bouquet – Rs. 649
- Lily Bouquet – Rs. 799
- Orchid Bouquet – Rs. 999

The assistant also provided customized bouquet suggestions.

### Step 7: Prompt Guard

Used the `meta-llama/llama-prompt-guard-2-22m` model to test the detection of potentially malicious prompt injection attempts.

The test returned a score of approximately `0.9989`.

## 🔄 Workflow

Customer Query → System Prompt → Groq LLM → AI Response

Prompt injection detection was tested separately using Prompt Guard.

## 📚 Learning Outcomes

- LLM integration using Groq and LangChain.
- Secure API key management.
- Structured prompt engineering.
- Domain-specific AI assistant development.
- Controlling AI-generated responses.
- Introduction to prompt injection detection.

## 🚀 Conclusion

Successfully developed a domain-specific AI assistant for Bloom & Bliss Flower Shop using Groq LLM and structured prompt engineering. The task provided practical experience in building AI assistants and understanding AI safety through Prompt Guard.
