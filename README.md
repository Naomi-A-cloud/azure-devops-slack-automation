# 🚀 Azure DevOps Slack Automation

## Project Overview

This project demonstrates how I automated notifications between GitHub, Azure DevOps, and Slack using Azure Pipelines, YAML, Service Hooks, and secure secret management.

Whenever code is pushed to the GitHub repository, Azure DevOps automatically triggers a CI pipeline. Once the pipeline completes successfully, a notification is sent to a Slack channel, providing immediate visibility into the pipeline status without requiring anyone to manually check Azure DevOps.

This project reflects a real-world DevOps workflow where automation improves collaboration, reduces manual effort, and provides faster feedback to engineering teams.

---

## Business Problem

Development teams often need to know immediately when new code has been integrated or when a pipeline has completed successfully. Without automated notifications, engineers must repeatedly check Azure DevOps, slowing collaboration and reducing visibility.

This solution automates that process by delivering pipeline notifications directly into Slack.

---

## Solution

I designed and implemented an automated CI notification workflow using:

- GitHub as the source code repository
- Azure DevOps Pipelines for Continuous Integration
- YAML for pipeline configuration
- Azure DevOps Variable Groups for secure secret management
- Slack Incoming Webhooks for notifications
- Azure DevOps Service Hooks for event-driven automation

---

## Technologies Used

- Azure DevOps
- Azure Pipelines
- GitHub
- Git
- YAML
- Slack
- Incoming Webhooks
- Azure DevOps Service Hooks
- Azure DevOps Variable Groups
- CI/CD

---

# Solution Architecture

> Architecture diagram coming next.

![Architecture](assets/architecture.png)

---

# Project Workflow

```text
Developer
      │
      ▼
Push Code to GitHub
      │
      ▼
GitHub Repository
      │
      ▼
Azure DevOps Pipeline
      │
      ▼
Runs YAML Pipeline
      │
      ▼
Retrieves Slack Webhook from Variable Group
      │
      ▼
Posts Notification to Slack Channel
```

---

## Security Best Practices

One of the most important lessons from this project was learning how to protect sensitive credentials.

Instead of hardcoding the Slack Webhook URL inside the YAML pipeline, I stored it securely inside an Azure DevOps Variable Group. This follows cloud security best practices by preventing secrets from being exposed in source code.

---

## Project Screenshots

The repository includes screenshots showing:

- GitHub Repository
- Azure Pipeline
- Successful Pipeline Execution
- Azure DevOps Service Hooks
- Slack Notification
- Variable Group Configuration

---

## Lessons Learned

This project helped me understand how cloud automation extends beyond simply running a pipeline.

I gained practical experience with:

- Building CI pipelines using YAML
- Integrating GitHub with Azure DevOps
- Configuring Azure DevOps Service Hooks
- Automating Slack notifications
- Managing secrets securely
- Troubleshooting cloud integrations
- Understanding how enterprise teams automate operational workflows

One of the biggest takeaways was recognising the importance of secure secret management. Rather than exposing sensitive values in configuration files, I learned how Azure DevOps Variable Groups provide a safer way to manage credentials used by automation workflows.

---

## Future Improvements

Next, I plan to expand this project by implementing:

- Azure Key Vault integration
- Multi-stage CI/CD pipelines
- Automated deployment to Azure
- Infrastructure as Code using Terraform
- Microsoft Teams notifications
- Pipeline approvals and environments

---

## Repository

GitHub Repository:

https://github.com/Naomi-A-cloud/azure-devops-slack-automation

---

## Author

**Naomi Nwogu**

Aspiring Cloud Engineer | Cloud Security Enthusiast | Azure | GitHub | Automation | CI/CD

I am building practical cloud engineering projects to strengthen my skills in infrastructure, automation, cloud security, and DevOps while transitioning into a professional Cloud Engineering career.
