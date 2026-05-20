# Troubleshooting Guide

# 1. Jenkins Not Opening

## Problem
Browser cannot access Jenkins on port 8080.

## Solution

Check running containers:

```bash
sudo docker ps
```

Restart Jenkins:

```bash
sudo docker restart jenkins
```

Verify EC2 security group allows port 8080.

---

# 2. GitHub Webhook Not Triggering

## Problem
Pipeline does not start automatically after GitHub push.

## Solution

Verify webhook URL:

```text
http://EC2-PUBLIC-IP:8080/github-webhook/
```

Check:
- GitHub webhook enabled
- Port 8080 open
- Jenkins running

---

# 3. Docker Permission Denied

## Problem

```text
permission denied while trying to connect to docker.sock
```

## Solution

```bash
sudo usermod -aG docker jenkins
sudo docker restart jenkins
```

---

# 4. Jenkins Pipeline Failure

## Problem
Pipeline stops during build/test/deploy stage.

## Solution

Check Jenkins logs:

```bash
sudo docker logs jenkins
```

Verify:
- Jenkinsfile exists
- GitHub repository correct
- Docker installed

---

# 5. Git Directory Error

## Problem

```text
fatal: not in a git directory
```

## Solution

Clear Jenkins workspace and rebuild pipeline.

---

# 6. Backup Script Failure

## Problem
Backup archive not creating.

## Solution

Verify:
- Backup directory exists
- Docker permissions available
- Jenkins container running

---

# Useful Linux Commands

## Check containers

```bash
sudo docker ps
```

## Restart Jenkins

```bash
sudo docker restart jenkins
```

## View logs

```bash
sudo docker logs jenkins
```

## Check disk usage

```bash
df -h
```

## Check memory usage

```bash
free -m
```
