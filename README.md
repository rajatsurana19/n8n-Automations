# repo-info.yaml
repo:
  name: "n8n-Automations"
  short_description: "A collection of automation workflows built using n8n, hosted in Docker."
  long_description: |
    A collection of automation workflows built using n8n, hosted in Docker.
    These workflows help automate social media, content creation, and productivity tasks with minimal setup.

workflows:
  - id: instagram-idea-generator
    name: "Instagram Idea Generator"
    description: "Automatically creates engaging Instagram post ideas (hook, content, CTA) and saves them to Google Sheets."
    entrypoint: "Instagram-Automation/instagram-idea.json"
    notes: "Replace Google Sheet IDs and webhook URLs with your own values before activating."

  - id: linkedin-automation
    name: "LinkedIn Automation"
    description: "Automates LinkedIn-related tasks such as drafting post ideas or logging post drafts to Google Sheets. Configure LinkedIn API credentials and webhook triggers as needed."
    entrypoint: "LinkedIn-Automation/linkedin-automation.json"
    notes: "Add LinkedIn OAuth credentials in n8n and update any placeholders."

docker:
  run_instructions: |
    # Pull the latest n8n image
    docker pull n8nio/n8n

    # Run n8n container (simple local run)
    docker run -it --rm \
      -p 5678:5678 \
      -v ~/.n8n:/home/node/.n8n \
      n8nio/n8n

    # Open the n8n dashboard at:
    # http://localhost:5678

setup:
  steps:
    - step: "Clone the repository"
      command: "git clone https://github.com/rajatsurana19/n8n-Automations.git"
    - step: "Start n8n (Docker)"
      description: "Run the Docker commands above to start n8n locally."
    - step: "Import workflows"
      description: "In the n8n dashboard go to Workflows → Import → Upload JSON and select the workflow JSON files from this repo."
    - step: "Configure credentials"
      description: "Add Google Sheets OAuth2 credentials, LinkedIn OAuth credentials (if using LinkedIn automation), and any other API keys inside n8n Credentials."
    - step: "Replace placeholders"
      description: "Update placeholder values in workflows — such as Sheet IDs, webhook IDs/URLs, session keys — with your own values."
    - step: "Activate and test"
      description: "Activate the workflow and trigger it to confirm it performs as expected. Check logs and Google Sheets for outputs."

requirements:
  - "Docker (for running n8n)"
  - "n8n instance (local via Docker or hosted)"
  - "Google account and Google Sheets credentials (for workflows using Sheets)"
  - "LinkedIn developer credentials (if using LinkedIn automation)"
  - "Basic familiarity with n8n workflows and credential configuration"

structure:
  - folder: "Instagram-Automation"
    contents:
      - "instagram-idea.json"
      - "README.md (optional: notes specific to the workflow)"
  - folder: "LinkedIn-Automation"
    contents:
      - "linkedin-automation.json"
      - "README.md (optional: notes specific to the workflow)"
  - folder: "docs"
    contents:
      - "setup.md (optional)"
  - file: "repo-info.yaml"
  - file: "README.md (generate from repo-info.yaml or keep both)"

readme_content: |
  # n8n-Automations 🚀
  A collection of automation workflows built using [n8n](https://n8n.io), hosted in Docker.  
  These workflows help automate social media, content creation, and productivity tasks with minimal setup.

  ---

  ## 🧩 Overview
  This repository contains ready-to-use n8n workflows that can be imported directly into your own n8n instance.  
  Each workflow is designed to be **simple**, **modular**, and **easy to customize** for your needs.

  Current included workflows:
  - **Instagram Idea Generator** – Automatically creates engaging Instagram post ideas and saves them to Google Sheets.
  - **LinkedIn Automation** – Automates LinkedIn-related tasks such as drafting post ideas and logging drafts to Google Sheets.

  ---

  ## 🐳 Run n8n in Docker
  You can easily run n8n locally using Docker:

  ```bash
  # Pull the latest n8n image
  docker pull n8nio/n8n

  # Run n8n container
  docker run -it --rm \
    -p 5678:5678 \

    # setup-info.yaml
setup:
  title: "⚙️ Setup"
  steps:
    - step: "Clone this repository"
      command: "git clone https://github.com/rajatsurana19/n8n-Automations.git"
    - step: "Start n8n using Docker"
      description: "Run n8n locally in Docker as described in the instructions above."
    - step: "Import workflow into n8n"
      description: "In the n8n dashboard, go to Workflows → Import → Upload JSON and select a workflow file from this repository."
    - step: "Configure credentials"
      description: "Add Google Sheets, LinkedIn OAuth, and other API credentials inside n8n."
    - step: "Update placeholders"
      description: "Replace placeholder values such as Sheet IDs, Webhook URLs, and session keys in the workflow."
    - step: "Activate and test"
      description: "Activate the workflow in n8n and run a test to ensure everything is working correctly."

requirements:
  title: "🧠 Requirements"
  list:
    - "Docker installed"
    - "n8n running locally or on a server"
    - "Google Sheets credentials (for Sheets-based workflows)"
    - "LinkedIn credentials (for LinkedIn automation)"

author:
  title: "👤 Author"
  name: "Rajat Surana"
  links:
    linkedin: "https://www.linkedin.com/in/rajatsurana19"
    github: "https://github.com/rajatsurana19"


    -v ~/.n8n:/home/node/.n8n \
    n8nio/n8n
