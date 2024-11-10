# n8n Assignment: Building Three Unique Apps

This repository contains three unique applications built using the n8n platform as part of an assignment. Each app leverages different functionalities of n8n to showcase its capabilities in automation, backend processing, and human-in-the-loop workflows.

## Overview

This project includes:
1. **Customer Support Chat Frontend** - A chat-based support interface for customer queries.
2. **Backend Triggered Application** - An app that triggers backend events, like handling Kafka messages or email processing.
3. **Human-in-the-Loop Agent** - A workflow that invokes a human agent if the AI needs assistance with a query.

### Prerequisites
- [n8n](https://n8n.io/) installed (self-hosted on your local machine using either npm or Docker).
- Free quota on n8n's platform (to avoid limits on API calls).
- Access to workflows in the n8n library for template usage.

## Application Details

### 1. Customer Support Chat Frontend
**Description**: A chat frontend designed to handle customer support queries. If the AI cannot resolve an issue, it escalates to a human agent.

- **Technologies**: Uses n8n and may integrate with a chatbot (e.g., GPT or Dialogflow).
- **Workflow**: The workflow processes incoming messages, generates responses, and escalates unresolved issues to a human.
- **Template**: Based on n8n's customer support and chatbot templates.

**Setup**:
1. Import a suitable chat template from the [n8n workflows library](https://n8n.io/workflows/).
2. Integrate the chatbot API if using one (optional).
3. Configure escalation parameters to notify a human agent if the AI is uncertain.

### 2. Backend Triggered Application
**Description**: This app processes backend events such as Kafka messages or incoming emails, allowing automated responses or data processing actions.

- **Technologies**: n8n with email or Kafka triggers.
- **Workflow**: Triggers on backend events (like Kafka messages or new emails), performs processing (e.g., stores data, triggers actions), and forwards it as needed.

**Setup**:
1. Import an email automation or Kafka workflow template from the [n8n workflows library](https://n8n.io/workflows/).
2. Set up triggers based on the desired backend process.
3. Configure any necessary API keys or integration details.

### 3. Human-in-the-Loop Agent
**Description**: An app that involves a human agent if the AI does not confidently respond to a query. Useful in situations where human intervention is required.

- **Technologies**: n8n with human agent integration.
- **Workflow**: If the AI cannot answer, it triggers a notification to a human agent for intervention.

**Setup**:
1. Use [this workflow template](https://n8n.io/workflows/2095-ask-a-human-for-help-when-the-ai-doesnt-know-the-answer) to create the human-in-the-loop configuration.
2. Customize the threshold for AI confidence and set the notification parameters.

## Installation

To run this project locally:

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/n8n-assignment
