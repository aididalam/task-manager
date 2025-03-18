# Task Manager App

## Overview
This repository contains the Task Manager App, a full-stack application with a ReactJS frontend and a PHP-based backend, utilizing MySQL for data storage. The application allows users to create, update, delete, filter, and search for tasks efficiently.

## Demo URL
You can access the live demo of the application at:
[http://178.16.142.140:8333](http://178.16.142.140:8333)

### Demo Credentials
- **Email**: task@task.com
- **Password**: task1234

## Project Structure
- **task-backend/** - Contains the backend implementation using PHP with an MVC framework (Lumen).
- **task-frontend/** - Contains the frontend implementation using ReactJS with Vite.

> **Note:** Both `task-backend` and `task-frontend` are Git submodules and contain their respective `README.md` files with further details.

## Docker Configuration
The application is containerized using Docker Compose. The configuration includes:
- **Backend** (`lumen_app`): Runs the PHP backend service.
- **Database** (`db`): MySQL service for data storage.
- **Frontend** (`frontend_app`): ReactJS frontend service.

### Ports Used
- **Backend API**: `8330`
- **WebSocket**: `8331`
- **MySQL Database**: `8332`
- **Frontend**: `8333`

## How to Run
### Clone the Repository with Submodules
```sh
git clone --recurse-submodules https://github.com/aididalam/task-manager.git
cd task-manager
```

### Run Locally
```sh
docker compose up --build -d
```

### Run with Public IP or Domain
```sh
VITE_API_URL="http://YOUR_PUBLIC_IP_OR_DOMAIN:8330" \
VITE_WEB_SOCKET_URL="ws://YOUR_PUBLIC_IP_OR_DOMAIN:8331" \
docker compose up --build -d
```

## Accessing the Application
- **Frontend UI**: `http://localhost:8333`
- **API Endpoints**: `http://localhost:8330`
- **Database**: Connect via MySQL on `localhost:8332`

For additional configurations and setup details, refer to the `README.md` files inside the `task-backend` and `task-frontend` directories.


