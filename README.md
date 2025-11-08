# n8n-Automations

A collection of automation workflows built using [n8n](https://n8n.io), hosted in Docker.  
These workflows help automate social media, content creation, and productivity tasks with minimal setup.  
It includes ready-to-use automations for **Instagram** and **LinkedIn**.

---

## Overview

This repository provides a set of pre-built workflows that you can import directly into your own n8n instance.  
Each workflow is modular, easy to modify, and designed for creators and developers looking to streamline their daily tasks.

### Available Workflows

- **Instagram Idea Generator**  
  Automatically creates engaging Instagram post ideas — including hooks, captions, and CTAs — and saves them to Google Sheets.

- **LinkedIn Automation**  
  Helps automate LinkedIn tasks like generating post drafts or logging your content pipeline directly into Google Sheets.

---

## Run n8n in Docker

You can easily run n8n locally using Docker.

```bash
# Pull the latest n8n image
docker pull n8nio/n8n

# Run n8n container
docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n

Start n8n using Docker

Follow the commands above to run n8n locally.

Import a workflow into n8n

In the n8n dashboard, go to:

Workflows → Import → Upload JSON


Then select a workflow file from this repository (for example, the Instagram or LinkedIn automation).

Configure credentials

Inside n8n, add your required credentials:

Google Sheets OAuth2 credentials (for Sheets-based workflows)

LinkedIn OAuth credentials (for LinkedIn workflows)

Any other API keys as needed

Update placeholders

Before activating the workflows, replace placeholder values such as:

Google Sheet IDs

Webhook URLs

Session keys or other custom variables

Activate and test

Once everything is configured:

Activate the workflow inside n8n

Trigger it manually or via webhook

Verify that it logs data correctly (e.g., posts in Google Sheets)

Requirements

Docker installed

n8n running locally or on a server

Google Sheets credentials (for Sheets-based workflows)

LinkedIn developer credentials (for LinkedIn automation)

Author

Rajat Surana
LinkedIn

GitHub
