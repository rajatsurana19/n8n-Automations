n8n Automations
A collection of n8n workflows for automating social media content creation, hosted locally using Docker.

🚀 Overview
This repository contains powerful and time-saving n8n workflows designed to streamline your content creation process. These workflows are set up to run locally using Docker, giving you full control over your data and automation.

✨ Workflows Included
This project currently includes the following two main workflows:

LinkedIn Post Generation:

Automatically generates engaging posts for your LinkedIn profile.

Can be configured to pull from different data sources or content ideas.

Instagram Content Idea Generation:

Helps you brainstorm and generate new content ideas for your Instagram feed.

Keeps your content pipeline full with fresh and relevant topics.

🛠️ Technology Stack
n8n: The core workflow automation tool.

Docker: Used for easy local hosting and environment management.

⚙️ Local Setup & Installation
To get these automations running on your local machine, follow these steps:

Clone the Repository:

Bash

git clone https://github.com/rajatsurana19/n8n-Automations.git
Navigate to the Directory:

cd n8n-Automations
Run with Docker: This project is configured to run with Docker Compose.

# Pull the latest n8n image
docker pull n8nio/n8n

# Run n8n container
docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
  
Import Workflows:

On your n8n canvas, go to Workflows.

Click Import from File.

Upload the .json workflow files included in this repository to add them to your instance.

🧑‍💻 Connect with Me
Find this project helpful or have questions? Feel free to connect with me!

LinkedIn: https://in.linkedin.com/in/rajat-surana

GitHub: https://github.com/rajatsurana19
