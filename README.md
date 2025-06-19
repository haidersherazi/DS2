
# CI/CD Deployment of a FastAPI "Hello World" Application

**Team:** Release Me, Please  
**Course:** Digital Systems 2 — Deployment Project Assignment  

## 👥 Team Members

| Last Name | First Name         |
|-----------|--------------------|
| Sherazi   | Syed M. H. Ali     |
| Kachchhi  | Roamilkumar        |
| Khanduri  | Anjali             |
| Onah      | Onyedikachi        |
| Viegas    | Franklin           |

---

## Overview

This project demonstrates a complete DevOps CI/CD pipeline for deploying a **containerized FastAPI "Hello World" web service** using:

- **FastAPI**
- **Docker & Docker Hub**
- **GitHub Actions (CI/CD automation)**
- **Render (Cloud Hosting)**

The pipeline includes:
- Code testing with `pytest`
- Docker image build and push
- Auto-deployment via Render webhooks

---

## Live Systems

> ⚠️ **Note:** APIs are currently suspended due to limited hours. They will be reactivated on the presentation day.

### 🔗 GitHub Links
- [`stage` branch](https://github.com/haidersherazi/DS2/tree/stage)
- [`production` branch](https://github.com/haidersherazi/DS2/tree/production)

### DockerHub Repository
- [https://hub.docker.com/repositories/haidersherazi](https://hub.docker.com/repositories/haidersherazi)

**Images:**
- `docker.io/haidersherazi/hello-api-stage:latest`
- `docker.io/haidersherazi/hello-api-prod:latest`

### Deployed API Endpoints
- [Staging](https://hello-api-stage-latest.onrender.com/hello)
- [Production](https://hello-api-prod-latest.onrender.com/hello)

---

## System Architecture

### Tools Used
- **GitHub** – Source code and CI/CD triggers
- **GitHub Actions** – Pipeline automation
- **Docker & DockerHub** – Containerization and image registry
- **Render** – Cloud hosting platform

![Archit](https://github.com/user-attachments/assets/fee723f9-c451-43d4-868b-72926d5d2545)

## Deployment Strategy
### Branching Strategy
feature/*: For new features
stage: Deploys to staging after CI/CD validation
production: Final deployment to live production
main: Updated after production for clean feature branch base

### Pipeline Stages
Build: The Docker image is built using Dockerfile. Compiles dependencies and image—image is built but not pushed yet.
Test: pytest is run on FastAPI endpoint /hello. If it fails, deployment stops.
Deploy: Only runs if tests pass. Docker image pushed to Docker Hub; Render auto-deploys via webhook.

## Conclusion
This project successfully demonstrates an automated, secure, and production-ready CI/CD pipeline using containerization and cloud-native tools. The architecture ensures reliable deployment across staging and production environments with test validation and no manual intervention.

