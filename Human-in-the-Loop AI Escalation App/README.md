# Human-in-the-Loop AI Escalation App

## Overview
This workflow integrates AI and human agents to handle user queries efficiently. It processes queries using AI and escalates them to a human agent when the AI cannot provide a confident or sufficient response.

## Features
- **Webhook Integration**: Accepts external user queries via an HTTP POST request.
- **AI Processing**: Sends queries to OpenAI's GPT-4 model for intelligent responses.
- **Condition Evaluation**: Uses an If Node to determine if the AI's response is sufficient or requires human intervention.
- **Slack Notification**: Escalates unresolved queries to a specified Slack channel by updating the channel topic with the query details.

## Workflow Summary
1. **Trigger**: 
   - Queries are accepted via a Webhook or Chat Message trigger.
2. **AI Response**:
   - The query is sent to OpenAI's GPT-4 API for processing.
3. **Condition Check**:
   - The AI response is evaluated for completeness or confidence.
4. **Human Escalation**:
   - If the AI cannot respond confidently, the workflow updates the Slack channel topic to notify a human agent.

## Technologies Used
- **n8n**: Workflow automation.
- **OpenAI GPT-4**: AI-powered query processing.
- **Slack**: Communication and escalation.

## How to Use
1. Deploy the workflow in an n8n instance.
2. Configure the Webhook URL to accept external queries.
3. Set up OpenAI and Slack credentials in n8n.
4. Test the workflow by submitting a query to the Webhook.

## Purpose
The Human-in-the-Loop AI Escalation App ensures efficient handling of queries by combining AI automation with human expertise, guaranteeing no query goes unresolved.

