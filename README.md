# Module 8

This module introduces the fundamental concepts and technologies that power web applications, including:

- **REST APIs** (Representational State Transfer Application Programming Interfaces): Standards that allow different software applications to communicate over the internet.
- **FastAPI**: A modern, fast (high-performance) web framework for building APIs with Python.
- **HTML** (HyperText Markup Language): The standard markup language for creating web pages.
- **JavaScript**: A programming language that enables interactive web pages and is an essential part of web applications.
- **Playwright**: A Python library for automating and testing web applications through browser interactions.

## Key Components

1. **Dockerfile** — Sets up a Docker container for a FastAPI Calculator Application by using the `mcr.microsoft.com/playwright/python:v1.47.0-noble` image as the base, installing necessary system packages and Python dependencies, creating a non-root user with sudo access, and configuring the environment to run the application.
2. **docker-compose.yml** — Defines a multi-service application, including a FastAPI web service, a PostgreSQL database, and a Redis cache, specifying their configurations, dependencies, and networking to facilitate seamless integration and deployment.
3. **main.py** — Defines the FastAPI application, including API endpoints for basic arithmetic operations and serving the HTML page, utilizing Pydantic models for input validation and Jinja2 templates for rendering responses.
4. **app/operations.py** — Contains arithmetic functions (`add`, `subtract`, `multiply`, `divide`).
5. **templates/index.html** — The HTML frontend that interacts with the API.

## Setting Up the Development Environment

1. **Clone the repository:**
git clone https://github.com/enp23/assignment8.git

2. **Navigate to the project directory:**
cd assignment8

3. **Create a virtual environment:**
python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate

4. **Install dependencies:**
pip install -r requirements.txt

5. **Install Playwright and set up browsers:**
playwright install

6. **Run the application:**
uvicorn main:app --reload

7. **Access the application:**
   Open a web browser and navigate to `http://localhost:8000`.

8. **Stop the application:**
   Press `CTRL + C`.

### Running with Docker

9. **Build and start the application in Docker:**
docker compose up --build

10. **Run the tests from within the container:**
docker compose exec web pytest

## Docker Hub

[https://hub.docker.com/repository/docker/en23/assignment8/](https://hub.docker.com/repository/docker/en23/assignment8/)