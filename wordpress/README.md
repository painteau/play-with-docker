# 📢 WordPress Deployment on Play-With-Docker

## ⭐ Features
- 🚀 Quick deployment of WordPress and MariaDB
- 🐳 Uses Docker for easy container management
- 🔄 Automatic updates with Watchtower
- 🛠 Persistent storage with Docker volumes

## 📌 Prerequisites
- You must be logged in as **root** on a Play-With-Docker instance.
- Docker must be installed on the instance.

## 🛠 Setup & Installation

### 1️⃣ Download the `docker-compose.yml` file
Run the following command to fetch the file from the GitHub repository:

```bash
wget https://raw.githubusercontent.com/painteau/play-with-docker/main/wordpress/docker-compose.yml
```

### 2️⃣ Start the services using Docker Compose
Run:

```bash
docker compose up -d
```

### 3️⃣ Check container status
Ensure all containers are running:

```bash
docker ps
```

### 4️⃣ Access WordPress
Open your browser and visit:

```
http://<your_instance_IP>:8080
```

Replace `<your_instance_IP>` with your machine's IP address.

### 5️⃣ Manage containers
To stop the containers:

```bash
docker compose down
```

To restart after a reboot:

```bash
docker compose up -d
```

## ⚙ Options

| Option | Description |
|--------|-------------|
| `docker compose up -d` | Starts WordPress and MariaDB in detached mode |
| `docker compose down` | Stops and removes the containers |
| `docker ps` | Lists running containers |

## 🔧 Troubleshooting
- If WordPress is not accessible, verify the container status with `docker ps`.
- Check logs for errors:
  ```bash
  docker logs <container_name>
  ```
- Ensure the correct IP address is used to access WordPress.

## 📜 License
This project is licensed under the MIT License.

## ⚠ Security Notice
This project is not made for production, but only for testing purposes.

## 💡 Contributing
1. Fork the repository on GitHub: [play-with-docker](https://github.com/painteau/play-with-docker)
2. Create a new branch (feature-branch)
3. Commit and push your changes to your branch, and create a pull request.
For major changes, please open an issue first to discuss the proposed modifications.

