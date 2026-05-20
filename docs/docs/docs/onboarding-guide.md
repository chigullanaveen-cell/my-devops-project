# Onboarding Guide

## Project Overview
This project demonstrates a complete DevOps CI/CD pipeline using Jenkins, Docker, GitHub, and AWS EC2.

---

# Prerequisites
Before starting, ensure the following tools are available:

- GitHub Account
- AWS Account
- Docker Installed
- Jenkins Installed
- Ubuntu/Linux Server

---

# Setup Steps

## 1. Clone Repository

```bash
git clone https://github.com/chigullanaveen-cell/my-devops-project.git
```

---

## 2. Start Jenkins

```bash
sudo docker start jenkins
```

---

## 3. Access Jenkins

Open browser:

```text
http://EC2-PUBLIC-IP:8080
```

---

## 4. Configure GitHub Webhook

GitHub Repository → Settings → Webhooks

Webhook URL:

```text
http://EC2-PUBLIC-IP:8080/github-webhook/
```

---

## 5. Trigger Pipeline

Push code to main branch:

```bash
git add .
git commit -m "update"
git push origin main
```

Webhook automatically triggers Jenkins pipeline.

---

# Pipeline Stages
- Build
- Test
- Deploy

---

# Backup Location

```text
~/backups
```

---

# Troubleshooting
Refer:
```text
docs/troubleshooting.md
```
