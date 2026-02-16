# Jenkins CI/CD Pipeline with Docker

## Objective
Create a simple Jenkins pipeline to automate build, test, and deployment of an application using Docker.

## Tools Used
- Jenkins
- Docker
- GitHub

## Status
Project setup initialized.

## Jenkins Pipeline Setup

1. Jenkins is configured with a Pipeline job.
2. The pipeline is defined in a Jenkinsfile stored in the GitHub repository.
3. Jenkins pulls the code from GitHub and executes the pipeline stages:
   - Build
   - Test
   - Deploy
4. The pipeline can be triggered automatically on each code commit using GitHub webhooks.
