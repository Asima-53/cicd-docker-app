# CI/CD Pipeline with GitHub Actions and Docker

![CI/CD Pipeline](https://github.com/Asima-53/cicd-docker-app/actions/workflows/ci-cd.yml/badge.svg)

A simple Node.js app that is **automatically tested, built into a Docker image, and pushed to Docker Hub** on every push to `main`.

## How it works

```
git push --> GitHub Actions (test + build) --> Docker Hub --> docker run
```

## Tech stack

Node.js, Express, Docker, GitHub Actions, Docker Hub, GitHub Secrets

## Run it

```bash
docker pull asiima331/cicd-docker-app:latest
docker run -p 3000:3000 asiima331/cicd-docker-app:latest
```

Open http://localhost:3000

## Setup

Add these secrets in **Settings > Secrets and variables > Actions**:

- `DOCKERHUB_USERNAME`: your Docker Hub username
- `DOCKERHUB_TOKEN`: a Docker Hub access token (Read & Write)

## What I learned

- Containerizing an app with Docker
- Building a CI/CD workflow with GitHub Actions
- Keeping credentials safe with GitHub Secrets
- Debugging pipeline failures from workflow logs

## Next steps

Auto-deploy to AWS EC2 and provision the infrastructure with Terraform.
