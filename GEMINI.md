# GEMINI Project Context: Development Scripts

## Project Overview

This directory contains a collection of shell scripts designed to automate common development tasks. These scripts streamline the setup and execution of services and applications for different technology stacks.

## Scripts

Here is a breakdown of the available scripts and their functions:

*   **`docker.sh`**:
    *   **Purpose:** Starts required services using Docker Compose.
    *   **Command:** `docker compose up -d postgres rabbitmq`
    *   **Details:** This script launches `postgres` and `rabbitmq` containers in detached mode. It assumes a `docker-compose.yml` file is present in the directory where the script is executed.

*   **`java.sh`**:
    *   **Purpose:** Builds and runs a Java application using Maven, likely a Spring Boot project.
    *   **Commands:**
        ```bash
        mvn clean install -U
        mvn spring-boot:run
        ```
    *   **Details:** This script first cleans the project and updates dependencies, then runs the Spring Boot application.

*   **`python.sh`**:
    *   **Purpose:** Sets up a Python development environment and runs an ASGI application.
    *   **Commands:**
        ```bash
        python3 -m venv venv
        source venv/bin/activate
        uvicorn app.main:app --reload
        ```
    *   **Details:** This script creates a virtual environment, activates it, and starts a `uvicorn` server with hot-reloading, which is common for frameworks like FastAPI.

*   **`win_activate.sh`**:
    *   **Purpose:** A utility script for Windows activation.
    *   **Command:** `irm https://get.activated.win | iex`
    *   **Details:** This script downloads and executes a script from the internet to activate Windows.

## Usage

To use these scripts, navigate to your project's root directory in the terminal and execute the desired script using bash.

**Example:**

To start the Java application:
```bash
bash /home/kene/Workspace/cmd/java.sh
```

## Development Conventions

*   **Language:** All scripts are written in `bash`.
*   **Execution Context:** The scripts are generally intended to be run from the root directory of a project that they are designed to work with (e.g., `java.sh` from a Maven project directory).
*   **Modularity:** Each script is self-contained and focuses on a specific task.
