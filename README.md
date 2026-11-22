```markdown
# 2-Tier Dockerized Web Application

A containerized 2-tier web application featuring a PHP-based login and registration system running on Apache, paired with a MySQL database, orchestrated using Docker Compose.

## 🚀 Features

* **User Authentication:** Functional login and registration workflow through a web UI.
* **Multi-Container Architecture:** Isolated application (PHP/Apache) and database (MySQL) tiers running in separate containers.
* **Persistent Storage:** Uses Docker volumes to ensure MySQL database records persist across container restarts.
* **Isolated Networking:** Custom Docker network enabling seamless inter-container communication.
* **Secure Configuration:** Managed via environment variables for database credentials and settings.

## 🛠️ Tech Stack

* **Containerization & Orchestration:** Docker, Docker Compose
* **Frontend & Backend:** PHP, Apache
* **Database:** MySQL
* **OS/Environment:** Linux

## 🏗️ Architecture Overview

1. **Web Tier (`php-apache`):** Serves the frontend and handles backend authentication logic.
2. **Database Tier (`mysql`):** Stores and retrieves user registration and login data.

## ⚙️ Prerequisites

* [Docker](https://docs.docker.com/get-docker/) installed on your machine
* [Docker Compose](https://docs.docker.com/compose/install/) installed

## 📦 Getting Started

1. **Configure environment variables:**
Create a `.env` file in the root directory (if not already present) and specify your MySQL credentials:
```env
MYSQL_ROOT_PASSWORD=your_root_password
MYSQL_DATABASE=your_database_name
MYSQL_USER=your_db_user
MYSQL_PASSWORD=your_db_password

```


2. **Build and start the containers:**
```bash
docker-compose up -d --build

```


3. **Access the application:**
Open your browser and navigate to `http://localhost:<PORT>` (replace `<PORT>` with the host port mapped in your `docker-compose.yml`, typically `80` or `8080`).

## 🔧 Useful Commands

* **View running containers:** `docker ps`
* **Check application logs:** `docker-compose logs -f`
* **Access a container shell:** `docker exec -it <container_name> bash`
* **Stop and remove containers:** `docker-compose down`

```


```
