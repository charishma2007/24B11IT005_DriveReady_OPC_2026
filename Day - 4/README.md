# Day 4 – AI Agent with Tool Calling and Google Sheets Integration

## Task Overview

Developed an AI agent using LangChain and Groq that 
performs business operations through custom tools 
and stores customer orders in Google Sheets.

## Tasks Implemented

- Configured Groq LLM using LangChain.
- Connected Google Sheets using Gspread.
- Implemented structured data validation using Pydantic.
- Created custom tools using the @tool decorator.
- Built an AI agent using create_agent().
- Maintained conversation history for contextual responses.
- Implemented exception handling.

## Tools Implemented

| Tool | Description |
|------|-------------|
| get_price() | Calculates the total order price. |
| is_open() | Retrieves business operating hours. |
| log_order() | Validates and saves confirmed orders in Google Sheets. |

## Technologies Used

- Python
- LangChain
- Groq API
- Pydantic
- Gspread
- Google Colab

## Learning Outcomes

- Understanding tool calling in Agentic AI.
- Creating and integrating custom tools.
- Connecting AI agents with external applications.
- Validating structured data using Pydantic.
- Managing conversation memory.
- Automating order management using Google Sheets.

## Result

Implemented an AI agent capable of selecting appropriate 
tools, responding to customer queries, and storing 
confirmed orders in Google Sheets.
