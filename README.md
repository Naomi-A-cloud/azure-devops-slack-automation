# Azure DevOps Slack Automation

Automating GitHub, Azure DevOps Pipelines, and Slack notifications using YAML, CI/CD, and Azure Service Hooks.

---

## Project Overview

This project demonstrates how to automate software development workflows by integrating **GitHub**, **Azure DevOps Pipelines**, and **Slack**.

Whenever new code is pushed to the GitHub repository:

1. Azure DevOps automatically detects the change.
2. The CI pipeline is triggered.
3. The pipeline executes successfully.
4. Azure DevOps sends a notification to Slack.
5. Team members receive an instant update.

This project simulates the type of automation commonly used by cloud engineering and DevOps teams to improve collaboration and deployment visibility.

---

## Architecture

```text
               +----------------+
               |    GitHub      |
               | Code Repository|
               +--------+-------+
                        |
                  Git Push Event
                        |
                        ▼
          +---------------------------+
          | Azure DevOps Pipeline     |
          | (YAML CI Pipeline)        |
          +------------+--------------+
                       |
               Pipeline Execution
                       |
                       ▼
          +---------------------------+
          | Azure DevOps Service Hook |
          +------------+--------------+
                       |
                 HTTP Webhook
                       |
                       ▼
                +-------------+
                |    Slack    |
                | Notification|
                +-------------+
```

---

## Technologies Used

- Azure DevOps
- Azure Pipelines
- YAML
- GitHub
- Slack
- Azure Service Hooks
- CI/CD
- Ubuntu Hosted Agent

---

## Pipeline Workflow

The pipeline is configured using **azure-pipelines.yml**.

Trigger:

```yaml
trigger:
- main
```

The pipeline runs automatically whenever code is pushed to the **main** branch.

---

## Project Features

- Automated Continuous Integration (CI)
- YAML-based pipeline configuration
- GitHub repository integration
- Azure DevOps pipeline execution
- Slack notifications
- Event-driven automation
- Cloud workflow orchestration

---

## Security

Sensitive information such as the Slack Webhook URL is **never stored directly in the YAML pipeline**.

Instead, secrets are securely managed using:

- Azure DevOps Variable Groups
- Secret Variables
- Secure Pipeline Permissions

This follows cloud security best practices by preventing credential exposure.

---

## Learning Outcomes

Through this project I gained hands-on experience with:

- Building Azure DevOps Pipelines
- Writing YAML pipelines
- Configuring Azure Service Hooks
- Integrating GitHub repositories
- Managing secure pipeline secrets
- Automating notifications
- Understanding CI workflow automation

---

## Future Improvements

- Build stage
- Test stage
- Security scanning
- Artifact publishing
- Docker image builds
- Azure deployment
- Infrastructure as Code (Terraform)
- Approval Gates
- Multi-stage CI/CD pipeline

---

## Repository Structure

```
azure-devops-slack-automation/
│
├── azure-pipelines.yml
├── README.md
└── LICENSE
```

---

## Screenshots

### Successful Azure DevOps Pipeline

_Add screenshot here_

---

### Slack Notification

_Add screenshot here_

---

## Author

**Naomi Nwogu**

Aspiring Cloud Engineer | Cloud Security Enthusiast

- LinkedIn: https://www.linkedin.com/in/naomi-nwogu-8339a5215/
- GitHub: https://github.com/Naomi-A-cloud

---

## License

This project is licensed under the MIT License.
