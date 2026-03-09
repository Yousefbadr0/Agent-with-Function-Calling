# Simple AI Agent with Tool Calling

This project implements a **simple AI agent from scratch** using a **Large Language Model (LLM) as a router** that decides which tool should handle the user's request.

The agent analyzes a user prompt, returns a structured JSON specifying the required tool and its arguments, then executes the tool and returns the result.

## Architecture

The agent follows a simple workflow:

User Prompt → LLM Router → JSON Tool Selection → Tool Execution → Response

The LLM acts as a **router** that extracts the intent and parameters from the user's query.

Example JSON output from the model:

```json
{
  "tool": "currency",
  "arguments": {
    "amount": 50,
    "from_currency": "USD",
    "to_currency": "EGP"
  }
}
