# Infrastructure Architecture Diagram

```text
                ┌──────────────────┐
                │    Developer     │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │ GitHub Repository│
                └────────┬─────────┘
                         │
                  GitHub Webhook
                         │
                         ▼
                ┌──────────────────┐
                │ Jenkins Server   │
                │ AWS EC2 Ubuntu   │
                └────────┬─────────┘
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
     Build Stage     Test Stage    Deploy Stage
                         │
                         ▼
                ┌──────────────────┐
                │ Docker Container │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │ Application Live │
                └──────────────────┘
```

## Components Used
- AWS EC2
- Jenkins
- Docker
- GitHub
- GitHub Webhooks
- Ubuntu Linux
