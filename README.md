# 🚀 n8n Automations

A collection of powerful and customizable **n8n workflows** for automating social media content creation, hosted locally using **Docker**.

---

## 📘 Overview

This repository provides a suite of time-saving **n8n workflows** designed to streamline your content creation process. Each workflow is:

- Fully customizable  
- Runs locally via Docker  
- Gives you complete control over your data and automation  

---

## ✨ Included Workflows

### 1. 🔗 LinkedIn Post Generation
- Automatically generates engaging posts for your LinkedIn profile  
- Configurable to pull content ideas from various sources  
- Saves drafted ideas or posts directly to Google Sheets  

### 2. 📸 Instagram Content Idea Generation
- Helps brainstorm and generate content ideas for your Instagram feed  
- Produces post hooks, captions, and strategies for consistent posting  
- Stores all ideas neatly in Google Sheets for future use  

---

## 🛠️ Technology Stack

- **n8n** – Workflow automation engine powering logic and integrations  
- **Docker** – Containerized local hosting for easy setup and portability  
- **Google Sheets API** – Stores generated post ideas and drafts  
- **Google Docs API** – Saves LinkedIn post ideas as drafts  

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
- Go to Workflows → Import → Upload JSON in the n8n dashboard
- Select the .json workflow files from this repository (e.g., LinkedIn or Instagram)
- Click Import to add them to your workspace
  
### 5. Configure Credentials
Inside n8n, set up the following:
- Google Sheets OAuth2 credentials for saving generated content
- Google Docs OAuth2 credentials for saving LinkedIn drafts
- Any other required API keys specific to your setup
  
### 6. Update Placeholders
Before activating the workflows, replace the following:
- Google Sheet IDs
- Webhook URLs
- Session keys or custom variables
This ensures proper connectivity with your accounts.

### 7. Activate and Test
- Enable each workflow in n8n
- Trigger them manually or via webhook
- Verify output in your Google Sheets or LinkedIn drafts

---

## 💡 Requirements
- Docker installed
- n8n running locally or on a server
- Google Sheets API credentials


## 👤 Author
Rajat Surana
Connect with me on [LinkedIn](https://in.linkedin.com/in/rajat-surana)
Visit my GitHub: [@rajatsurana19](https://github.com/rajatsurana19)








