# Docker & Docker Compose – Quick Cheat Sheet

## 🔧 Docker Image Commands

| Command                    | Description                                      |
| -------------------------- | ------------------------------------------------ |
| `docker build -t <name> .` | Build image from Dockerfile in current directory |
| `docker images`            | List all images                                  |
| `docker rmi <image>`       | Remove an image                                  |
| `docker pull <image>`      | Pull image from Docker Hub                       |

---

## Docker Container Commands

| Command                            | Description                                    |
| ---------------------------------- | ---------------------------------------------- |
| `docker run -p 8000:8000 <image>`  | Run a container and map port                   |
| `docker run -it <image> bash`      | Start a container with an interactive terminal |
| `docker start <container>`         | Start a stopped container                      |
| `docker stop <container>`          | Stop a running container                       |
| `docker rm <container>`            | Remove a stopped container                     |
| `docker ps`                        | List running containers                        |
| `docker ps -a`                     | List all containers (including stopped)        |
| `docker exec -it <container> bash` | Open shell inside running container            |
| `docker logs <container>`          | Show logs                                      |
| `docker logs -f <container>`       | Follow live logs (like tail -f)                |

---

## 🧰 Docker Volume Commands

| Command                     | Description                    |
| --------------------------- | ------------------------------ |
| `docker volume ls`          | List all Docker volumes        |
| `docker volume rm <volume>` | Delete a specific volume       |
| `docker volume prune`       | Delete all unused volumes (⚠️) |

---

## Docker Compose Commands

| Command                              | Description                                      |
| ------------------------------------ | ------------------------------------------------ |
| `docker-compose up`                  | Start services defined in `docker-compose.yml`   |
| `docker-compose up --build`          | Rebuild and start services                       |
| `docker-compose up -d`               | Start services in background (detached)          |
| `docker-compose down`                | Stop and remove containers, networks             |
| `docker-compose down -v`             | Same as above, and remove volumes (⚠️ data loss) |
| `docker-compose exec -it <service> bash` | Open terminal in running container               |
| `docker-compose logs`                | Show logs from all services                      |
| `docker-compose logs -f`             | Follow logs live                                 |

---

## 🧠 Tips

| Use Case                 | Command                               |
| ------------------------ | ------------------------------------- |
| Build from Dockerfile    | `docker build -t myapp .`             |
| Rebuild only when needed | `docker-compose up` (cache used)      |
| Rebuild fresh            | `docker-compose build --no-cache`     |
| Clean all unused stuff   | `docker system prune` (⚠️ be careful) |
