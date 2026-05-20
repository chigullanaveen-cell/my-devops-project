# Jenkins Workflow Documentation

## Jenkins Pipeline Workflow

```text
GitHub Push
     │
     ▼
Webhook Trigger
     │
     ▼
Jenkins Job Starts
     │
     ▼
Checkout Source Code
     │
     ▼
Build Stage
     │
     ▼
Test Stage
     │
     ▼
Deploy Stage
     │
     ▼
Docker Container Deployment
```

## Pipeline Stages

### 1. Checkout Stage
Jenkins fetches latest code from GitHub repository.

### 2. Build Stage
Application build process starts.

### 3. Test Stage
Basic tests execute automatically.

### 4. Deploy Stage
Application deploys using Docker container.

---

## Jenkins Features Configured
- GitHub Webhooks
- Automatic Builds
- Multi-stage Pipeline
- Docker Integration
- Jenkins Backups

---

## Jenkins URL
```text
http://EC2-PUBLIC-IP:8080
```

## Tools Used
- Jenkins
- Docker
- GitHub
- AWS EC2
- Ubuntu Linux
