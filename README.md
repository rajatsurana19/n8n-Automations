# n8n-Automations

A collection of automation workflows built using [n8n](https://n8n.io), hosted in Docker.  
These workflows help automate social media, content creation, and productivity tasks — including **Instagram** and **LinkedIn** automations.

---

## Setup

### Clone this repository
```bash
git clone https://github.com/rajatsurana19/n8n-Automations.git
Start n8n using Docker
Follow the commands below to run n8n locally.

bash
Copy code
# Pull the latest n8n image
docker pull n8nio/n8n

# Run n8n container
docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
Then open http://localhost:5678 in your browser to access the n8n dashboard.

Import a workflow into n8n
In the n8n dashboard, go to Workflows → Import → Upload JSON

Choose a workflow file from this repository (e.g., the Instagram or LinkedIn automation)

Configure credentials
Add these inside n8n:

Google Sheets OAuth2 credentials (for Sheets workflows)

LinkedIn OAuth credentials (for LinkedIn automation)

Any other required API keys

Update placeholders
Replace placeholder values such as:

Google Sheet IDs

Webhook URLs

Session keys or custom variables

Activate and test
Activate the workflow inside n8n

Trigger it manually or via webhook

Check that data appears correctly (for example, in Google Sheets)

Requirements
Docker installed

n8n running locally or on a server

Google Sheets credentials

LinkedIn developer credentials

Author
Rajat Surana
LinkedIn
GitHub
