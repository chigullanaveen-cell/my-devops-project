# Deployment Flow Diagram

```text
Developer
   │
   ▼
Git Push
   │
   ▼
GitHub Repository
   │
   ▼
GitHub Webhook Trigger
   │
   ▼
Jenkins Pipeline
   │
   ├── Build Stage
   ├── Test Stage
   └── Deploy Stage
   │
   ▼
Docker Build
   │
   ▼
Docker Container Deployment
   │
   ▼
Application Live on EC2
```

## Deployment Process
1. Developer pushes code to GitHub
2. GitHub webhook triggers Jenkins automatically
3. Jenkins pipeline starts
4. Build stage executes
5. Test stage executes
6. Deployment stage executes
7. Docker container runs application
8. Application becomes live

## Technologies Used
- GitHub
- Jenkins
- Docker
- AWS EC2
- Ubuntu Linux
