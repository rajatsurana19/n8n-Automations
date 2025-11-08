# n8n Automations

A collection of **n8n workflows** for automating social media content creation, hosted locally using **Docker**.

---

## 🚀 Overview

This repository contains powerful and time-saving **n8n workflows** designed to streamline your content creation process.  
Each workflow can be easily customized and runs locally via Docker, giving you full control over your data and automation.

---

## ✨ Workflows Included

### 1. LinkedIn Post Generation
- Automatically generates engaging posts for your LinkedIn profile.  
- Can be configured to pull content ideas or inspiration from various sources.  
- Saves drafted ideas or posts directly to Google Sheets.

### 2. Instagram Content Idea Generation
- Helps you brainstorm and generate content ideas for your Instagram feed.  
- Produces post hooks, captions, and strategies for consistent posting.  
- Stores all ideas neatly in Google Sheets for future use.

---

## 🛠️ Technology Stack

- **n8n** – Workflow automation tool that powers the logic and integrations.  
- **Docker** – Used for containerized local hosting and easy setup.  
- **Google Sheets API** – For saving generated post ideas and drafts.
- **Googel Docs API** - For saving Linkedin post ideas in drafts.

---

## ⚙️ Local Setup & Installation

Follow these steps to get started locally:

### 1. Clone the Repository

git clone https://github.com/rajatsurana19/n8n-Automations.git

### 2. Navigate to the Project Directory
cd n8n-Automations

### 3. Run n8n with Docker

# Pull the latest n8n image
docker pull n8nio/n8n

# Run n8n container locally
docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
Once started, open http://localhost:5678 in your browser to access the n8n dashboard.

### 4. Import Workflows
In your n8n dashboard, go to Workflows → Import → Upload JSON.

Select the .json workflow files included in this repository (e.g., LinkedIn or Instagram).

Click Import to add them to your workspace.

### 5. Configure Credentials
Inside n8n, set up the following:

Google Sheets OAuth2 credentials for saving generated content.
Google Docs OAuth2 credentials for saving gennerated content

Any other required API keys specific to your setup.

### 6. Update Placeholders
Before activating the workflows, replace:

Google Sheet IDs

Webhook URLs

Session keys or custom variables

This ensures the workflows connect correctly with your accounts.

### 7. Activate and Test
Enable each workflow in n8n.

Trigger them manually or via webhook.

Check your Google Sheets or LinkedIn drafts to verify correct output.

💡 Requirements
Docker installed

n8n running locally or on a server

Google Sheets API credentials


👤 Author
Rajat Surana

LinkedIn

GitHub
