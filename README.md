# DevOps Capstone

[![CI Build](https://github.com/chaitalisalunke28/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)](https://github.com/chaitalisalunke28/devops-capstone-project/actions/workflows/ci-build.yaml)

This repository contains the starter code for the **IBM-CD0285EN SkillsNetwork DevOps Capstone Project**, part of the [IBM DevOps and Software Engineering Professional Certificate](https://www.coursera.org/professional-certificates/devops-and-software-engineering).

## Usage

Use this template to complete the DevOps Capstone project. It contains the code needed to get started.

Do not fork the original starter repository. Use GitHub's **Use this template** feature to create your own repository.

## Development Environment

These labs are designed to run in the IBM Developer Skills Network Cloud IDE with OpenShift. Follow the links provided in the Coursera Capstone project to access the lab environment.

Initialize the environment by sourcing the setup script:

```bash
source bin/setup.sh
```

This installs Python 3.9, configures it as the default, creates a Python virtual environment, and activates it.

## Useful Commands

Activate the Python virtual environment:

```bash
source ~/venv/bin/activate
```

Install dependencies:

```bash
make install
```

Start the PostgreSQL Docker container:

```bash
make db
```

Check running containers:

```bash
docker ps
```

## Project Layout

The microservice code is in the `service` package, and tests are in the `tests` folder. The project follows the Model-View-Controller pattern.

- `service/config.py` — Flask configuration
- `service/models.py` — persistent data model and business logic
- `service/routes.py` — REST API routes
- `service/common/` — shared logging and error handlers
- `setup.cfg` — testing and lint configuration
- `tests/` — unit tests

## Data Model

The Account model contains these fields:

| Name | Type | Optional |
|---|---|---|
| id | Integer | No |
| name | String(64) | No |
| email | String(64) | No |
| address | String(256) | No |
| phone_number | String(32) | Yes |
| date_joined | Date | No |

## Your Task

Complete the microservice by implementing the REST APIs for **READ, UPDATE, DELETE, and LIST**, while maintaining at least **95% code coverage**. Follow Test-Driven Development: write tests for the desired functionality, then implement the code to make them pass.

## Local Kubernetes Development

For local Kubernetes development, install Docker Desktop and, optionally, Visual Studio Code with the Remote Containers extension.

The repository includes Makefile commands to:

1. Create a local K3D Kubernetes cluster: `make cluster`
2. Install Tekton: `make tekton`
3. Install ClusterTasks: `make clustertasks`

Use these commands in the local development environment, not the Coursera Cloud IDE.

## Author

[John Rofrano](https://www.coursera.org/instructor/johnrofrano), Senior Technical Staff Member, DevOps Champion at IBM Research and Coursera instructor.

## License

Licensed under the Apache License. See the [LICENSE file](https://github.com/chaitalisalunke28/devops-capstone-project/blob/main/LICENSE).
