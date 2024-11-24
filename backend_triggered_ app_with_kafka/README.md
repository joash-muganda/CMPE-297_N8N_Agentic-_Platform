# Kafka-to-Email Notification App

This application uses **n8n** to create an automated workflow that listens to messages on a Kafka topic and sends email notifications for each new message. It's designed to demonstrate backend-triggered event handling and email alerts.

## Features

1. **Kafka Trigger**: Listens for new messages on a specified Kafka topic.
2. **Send Email Notification**: Sends an email containing the Kafka message details.

## Workflow

1. A Kafka producer sends messages to a specific topic (e.g., `my_topic`).
2. The **Kafka Trigger** node in n8n detects new messages.
3. The message is processed and sent via the **Send Email** node to a specified recipient.

## Requirements

- Docker (for running Kafka and n8n)
- A configured Gmail account with an App Password for SMTP
- Kafka topic set up and accessible within a Docker network


