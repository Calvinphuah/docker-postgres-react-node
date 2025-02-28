# Express API & React App with PostgreSQL (Dockerized)

This repository demonstrates how to containerize a full-stack application using Docker Compose. The project consists of two main services:

- **Express API Service:** A Node.js Express server that provides API endpoints and connects to a PostgreSQL database.
- **React App:** A front-end application built with React.

Both services are orchestrated with Docker Compose for easy setup and deployment.

## Table of Contents

- [Project Structure](#project-structure)
- [Starting the Services](#stopping-the-services)
- [Stopping the Services](#stopping-the-services)
- [Notes](#notes)
- [License](#license)

## Prerequisites

- Docker (v20+ recommended)
- Docker Compose (v2+ recommended)

## Project Structure

```plaintext
.
├── express-pg-server
│   ├── Dockerfile
│   ├── package.json
│   ├── index.js
│   └── ... (other API files)
├── react
│   ├── Dockerfile
│   ├── package.json
│   ├── public
│   ├── src
│   └── ... (other React files)
├── docker-compose.yaml
└── README.md
```

## Setting Up Environment Variables

Before running the project, you must set up the required environment variables.

## Starting the Services

To start the containers, networks, images, and volumes, run:

```bash
docker compose up --build -d
```

## Stopping the Services

To stop and remove the containers, networks, images, and volumes, run:

```bash
docker compose down --rmi all -v
```

## Notes

- **Obsolete `version` field:**  
  Docker Compose v2+ no longer requires the `version` field in `docker-compose.yaml`. Remove it if you see warnings.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
