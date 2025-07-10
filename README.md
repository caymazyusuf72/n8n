# (G) - Email Classification Workflow for n8n

![n8n](https://raw.githubusercontent.com/n8n-io/n8n/master/docs/images/n8n-logo.png)

## Overview

This workflow automates email classification triggered by a webhook, integrating seamlessly with Gmail. It processes incoming emails, categorizes them based on content or metadata, and triggers subsequent actions accordingly.

---

## Workflow Statistics

| Attribute      | Value     |
|----------------|-----------|
| Status         | Active    |
| Trigger        | Webhook   |
| Complexity     | Medium    |
| Nodes          | 15        |
| Integrations   | Gmail     |

---

## Setup Guide

### Prerequisites

- Active n8n instance
- Google OAuth credentials with Gmail API access configured in n8n
- Basic understanding of webhooks and email classification logic

### Steps

1. **Import Workflow:**

   - Download the workflow JSON file
   - In n8n Editor UI, go to Menu (☰) → Import Workflow → Select the JSON file

2. **Configure Webhook:**

   - Open the Webhook Trigger node
   - Copy and deploy the webhook URL to receive triggers

3. **Set Gmail Credentials:**

   - Ensure Gmail OAuth credentials are linked properly in n8n
   - Verify Gmail API permissions to read and process emails

4. **Customize Classification Logic:**

   - Review and adjust code or decision nodes for email categorization according to your rules

5. **Activate Workflow:**

   - Turn on the workflow in n8n
   - Test by sending emails to trigger classification

---

## Workflow Diagram

```mermaid
graph TD
    A[Webhook Trigger] --> B[Gmail Node: Fetch Emails]
    B --> C[Code/Function Node: Classification Logic]
    C --> D[Filter Nodes / Actions based on Category]
    D --> E[Further Processing / Notifications]
