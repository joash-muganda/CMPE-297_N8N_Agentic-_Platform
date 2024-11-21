# Slack to Airtable Ticketing Automation

This repository contains a workflow that automates the creation of support tickets from Slack messages containing specific keywords or emojis (e.g., `:ticket:`). The workflow uses AI to generate actionable ticket details and logs them into Airtable for efficient tracking and resolution.

---

## Features

1. **Query Slack for Messages**  
   - The workflow searches a designated Slack channel for messages containing the `:ticket:` emoji using a Slack API query.
   - Retrieves the most recent messages based on the configured schedule trigger.

2. **Generate Ticket Details Using AI**  
   - Extracted message content is sent to OpenAI's ChatGPT model to:
     - Generate a concise ticket title.
     - Summarize the user issue.
     - Suggest actionable solutions.
     - Assign a priority level (low, medium, high, urgent).

3. **Log Tickets into Airtable**  
   - The workflow sends structured ticket data to Airtable, creating a new record for each ticket.
   - Airtable serves as a centralized database for managing and tracking support tickets.

4. **Optional Slack Updates**  
   - Optionally, the workflow can post ticket status updates back to Slack.

---

## Setup Instructions

### Prerequisites
- **Slack Integration**: A Slack workspace and a designated channel for ticket messages.
- **OpenAI API**: Access to the OpenAI ChatGPT model.
- **Airtable**: A table set up with fields to store ticket details (e.g., title, summary, priority, ideas).

### Steps

1. **Slack Node Configuration**
   - Set the Slack channel to monitor.
   - Use a search query such as `in:#channel-name ":ticket:"` to filter messages.

2. **AI Node Setup**
   - Configure the OpenAI node to process message content.
   - Use the provided text prompt to generate ticket details.

3. **Airtable Node Setup**
   - Link Airtable and ensure fields for ticket details (title, summary, priority, suggestions) match the workflow structure.

4. **Testing**
   - Post sample messages in Slack with the `:ticket:` emoji.
   - Verify tickets are correctly logged in Airtable.

---

## Example Workflow

1. **Step 1: Query Slack for Messages**  
   Slack API retrieves messages from the specified channel.

2. **Step 2: Generate Ticket Details Using AI**  
   OpenAI processes the message text to create structured ticket information.

3. **Step 3: Log Ticket in Airtable**  
   Airtable stores the ticket information in a structured format.

4. **Optional Step 4: Post Updates to Slack**  
   Update Slack with ticket status or ID.

---

## Video Demo

Watch the [video demonstration here](https://drive.google.com/file/d/1j83Io5EER9D5gGeWnUnTy02lkIdnTTJ_/view?usp=sharing).

---

This repository simplifies support ticket management by seamlessly integrating Slack, OpenAI, and Airtable, boosting team efficiency and reducing response times.
