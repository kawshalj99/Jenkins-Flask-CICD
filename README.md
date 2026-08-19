# Jenkins Flask CI/CD Pipeline

DevOps project demonstrating a complete CI/CD pipeline using Jenkins, Docker, GitHub, and Python.

## Architecture

GitHub → Jenkins → Docker Test Environment → Pytest → Docker Build → Container Deployment → Health Check

## Technologies

- Git & GitHub
- Jenkins
- Docker
- Docker Desktop
- Python
- Flask
- Pytest
- Jenkins Pipeline
- Linux shell scripting

## Pipeline Workflow

1. Jenkins checks out the source code from GitHub.
2. A temporary Python Docker container is created for testing.
3. Python dependencies are installed inside the isolated container.
4. Automated tests are executed using Pytest.
5. A Docker image is built for the Flask application.
6. The previous application container is stopped and removed.
7. A new Flask container is deployed.
8. Jenkins performs an automated health check.
9. The pipeline reports SUCCESS or FAILURE.

## Project Structure

```text
Jenkins-Flask-CICD/
│
├── app.py
├── Dockerfile
├── Jenkinsfile
├── requirements.txt
├── README.md
├── .gitignore
│
├── jenkins/
│   └── Dockerfile
│
└── tests/
    └── test_app.py