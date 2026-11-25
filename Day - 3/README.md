# Day 3 – LangChain, Automated Testing & AI Agents 🌸

## 📌 Task Overview

Enhanced the Bloom & Bliss Flower Shop AI Assistant using Google Gemini and LangChain. The main focus was building conversational chains, automated response testing, temperature comparison, and introducing AI agents.

## 🛠️ Technologies Used

- Python
- Google Colab
- Gemini API – `gemini-3.1-flash-lite`
- LangChain
- CSV

## ⚙️ Implementation

### 1. Gemini API Integration

Replaced the Groq API with Google Gemini API and configured the model using `ChatGoogleGenerativeAI`.

### 2. LangChain Pipeline

Implemented a conversational chain using:

- `ChatPromptTemplate` – Structured prompt creation.
- `MessagesPlaceholder` – Maintains conversation context.
- `StrOutputParser` – Extracts responses as plain text.

**Pipeline:** Prompt → LLM → Output Parser → Response

### 3. Automated Testing

Created a `tests.csv` file containing 18 customer questions with expected keywords or values.

Implemented `run_tests()` to evaluate assistant responses, display PASS or FAIL, and calculate the pass rate.

The dataset includes 15 expected passing cases and 3 intentionally failing cases to verify the testing mechanism.

### 4. Temperature Comparison

Tested the assistant with different temperature settings.

| Temperature | Total Tests | Passed | Failed | Pass Rate |
|---|---:|---:|---:|---:|
| 1.0 | 18 | 15 | 3 | 83% |
| 0.3 | 18 | 15 | 3 | 83% |

Both temperature settings achieved the same reported pass rate, although their response styles differed.

### 5. Error Handling

Implemented retry logic and delays between API requests to handle temporary `503 UNAVAILABLE` server errors.

### 6. AI Agent Creation

Created a basic AI agent using LangChain's `create_agent()` function with the Gemini model and Flower Shop system prompt.

**Sample Query:** Can I buy two Sunflower Bouquets with a budget of Rs. 1000?

**Expected Result:**

- Total cost: Rs. 898
- Remaining balance: Rs. 102

The agent is currently configured without external tools.

## 🤖 Agent or Not

### Plain Code – Bouquet Price Calculation

Calculating the total price of bouquets requires a simple mathematical formula without using an LLM.

**Example:** Three Red Roses Bouquets = 399 × 3 = Rs. 1197.

### One LLM Call – Bouquet Recommendation

Recommending suitable flowers based on customer preferences, occasion, and budget requires a single LLM call.

**Example:** Recommend a wedding bouquet within Rs. 800.

### Agent – Customer Order Management

Managing a complete customer order requires multiple operations, such as checking flower availability, calculating prices, verifying delivery availability, and confirming the order.

An AI agent with external tools would be suitable for this task. This is a proposed future functionality.

## 📚 Learning Outcomes

- Building conversational chains using LangChain.
- Automated testing and response evaluation.
- Comparing different temperature settings.
- Handling API server errors.
- Understanding the difference between plain code, LLM calls and AI agents.

## 🚀 Conclusion

Successfully implemented a Gemini-powered conversational assistant with automated testing, temperature comparison, and basic agent functionality using LangChain.
