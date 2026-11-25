# Day 2 – Agentic AI: Conversational Flower Shop Assistant 🌸

## 📌 Task Overview

The Day 2 task focuses on enhancing the AI assistant developed on Day 1 by implementing conversation memory, Python functions, decorators, function logging, and API error handling.

I developed an interactive conversational chatbot for **Bloom & Bliss Flower Shop** that maintains conversation context and provides personalized customer assistance.

## 🎯 Objectives

- Understand multi-turn conversations using LLMs.
- Implement conversation history and memory.
- Implement Python functions and decorators.
- Calculate bouquet prices programmatically.
- Handle API errors and connection failures.
- Build an interactive customer support chatbot.

## 🛠️ Technologies Used

- Python
- Google Colab
- Groq API
- GPT-OSS-20B
- JSON
- Functools

## 🌷 Key Features

- Interactive customer conversations.
- Conversation memory and context management.
- Bouquet recommendations and pricing.
- Automatic price calculation using a Python function.
- Function execution logging.
- English and Telugu language support.
- API exception handling.
- Budget-based personalized recommendations.

## ⚙️ Implementation

### Step 1: Install Required Libraries

Installed the `groq` library to access the Large Language Model through the Groq API.

### Step 2: Configure API Key

Retrieved the API key securely from Google Colab Secrets using `userdata` and configured it as an environment variable.

### Step 3: Initialize the LLM

Configured the Groq client with:

- Model: `openai/gpt-oss-20b`
- Temperature: `0.3`

### Step 4: Define Menu and System Prompt

Created a bouquet menu using a Python dictionary.

| Bouquet | Price |
|---|---:|
| Red Roses Bouquet | Rs. 399 |
| Pink Roses Bouquet | Rs. 499 |
| Sunflower Bouquet | Rs. 449 |
| Mixed Flowers Bouquet | Rs. 649 |
| Lily Bouquet | Rs. 799 |
| Orchid Bouquet | Rs. 999 |

Designed a structured system prompt using Role, Facts, Rules, and Format to control chatbot behaviour.

### Step 5: Implement Function Logging

Created a `log_call()` decorator using `functools.wraps` to record function names, arguments, and returned results.

### Step 6: Implement Price Calculation

Created a `get_price()` function to calculate the total cost of bouquets based on quantity.

**Formula:**

Total Price = Bouquet Price × Quantity

**Example:**

- Bouquet: Red Roses
- Quantity: 3
- Unit Price: Rs. 399
- Total Price: Rs. 1197

### Step 7: Implement Conversation Memory

Created a conversation history list to store user messages and assistant responses.

The system prompt and the latest eight conversation messages are passed to the LLM to maintain context and limit the input size.

### Step 8: Implement Error Handling

Handled the following API exceptions:

| Exception | Purpose |
|---|---|
| RateLimitError | Handles API request limit errors. |
| APIConnectionError | Handles server connection failures. |

The chatbot displays user-friendly messages instead of terminating unexpectedly when these errors occur.

### Step 9: Build an Interactive Chat Loop

Implemented a continuous conversation using a `while` loop.

The chatbot accepts customer queries, generates responses, and continues the conversation until the user enters `bye`, `exit`, or `quit`.

## 🔄 Workflow

Customer Input → Conversation History → Groq LLM → AI Response → Update History → Continue Conversation

The price calculation and function logging are implemented and tested separately.

## 🧪 Sample Output

**Customer:** What is your shop menu?

**Assistant:** Displays available bouquets, prices, customization options, and shop timings.

**Customer:** What is your shop address?

**Assistant:** I'll check with the shop owner.

**Customer:** Exit

**Assistant:** Thank you for visiting Bloom & Bliss! Have a blooming day! 🌷

## 📊 Day 1 vs Day 2

| Day 1 | Day 2 |
|---|---|
| Basic AI assistant | Interactive conversational chatbot |
| Structured prompt engineering | Prompt engineering with memory |
| Independent queries | Multi-turn conversations |
| LangChain integration | Direct Groq API integration |
| Prompt Guard testing | API error handling |
| Basic response generation | Price calculation and function logging |

## 📚 Learning Outcomes

- Multi-turn conversation management.
- LLM conversation memory.
- Python decorators and function logging.
- Programmatic price calculation.
- API exception handling.
- Secure API key management.
- Interactive chatbot development.

## 🚀 Conclusion

Successfully enhanced the Bloom & Bliss Flower Shop AI Assistant by implementing conversation memory, function logging, price calculation, and API error handling. The Day 2 task provided practical experience in developing interactive and context-aware AI applications.
