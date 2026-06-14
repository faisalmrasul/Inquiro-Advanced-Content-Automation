# Inquiro Advanced Content Automation

An advanced AI-powered content automation workflow built with **n8n**. This workflow acts as an intelligent agent system that processes user requests for summarization, content creation, improvement, research, analysis, and general assistance. It uses Groq's LLM (Llama 3.3 70B), routes requests intelligently, and delivers polished responses via email.

## Features

- **Webhook Trigger**: Accepts POST requests with user messages and optional content.
- **Agentic Planning**: Analyzes request complexity and plans execution.
- **Intelligent Routing**: Uses LLM to determine the best specialized agent.
- **Specialized Agents**:
  - Summarization Agent
  - Content Creation Agent
  - Content Improvement Agent
  - Research Agent
  - Analytics Agent
  - General Assistant Agent
- **Rich Email Delivery**: HTML-formatted emails with agent metadata.
- **Error Handling & Fallbacks**: Robust parsing and clarification flows.
- **Groq Integration**: Fast, cost-effective LLM inference.

## Tech Stack

- [n8n](https://n8n.io/) - Workflow automation
- Groq API (Llama 3.3 70B)
- Gmail (for email delivery)
- JavaScript Code Nodes for logic

## Quick Start

1. **Import Workflow**
   - Copy the `workflow.json` content.
   - In n8n, go to **Workflows** > **Import from File/Clipboard**.
   - Paste and save.

2. **Configure Credentials**
   - **Groq API**: Add your Groq API key.
   - **Gmail**: Set up OAuth2 credentials.
   - Update email defaults if needed.

3. **Deploy Webhook**
   - Activate the workflow.
   - Use the webhook URL for integrations (e.g., from web forms, Zapier, or custom apps).

4. **Test**
   - Send a POST request to the webhook with payload:
     ```json
     {
       "userMessage": "Summarize this article about AI",
       "article": "...your text here...",
       "email": "your@email.com"
     }