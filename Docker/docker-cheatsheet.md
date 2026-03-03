Docker command reference organized by category.

## Container Commands

| Command | Description |
|---------|-------------|
| `docker run -it <image>` | Run container interactively |
| `docker run -d <image>` | Run container in detached mode |
| `docker run --rm <image>` | Auto-remove when exited |
| `docker run -p 8080:80 <image>` | Map host:container ports |
| `docker run -v $(pwd):/app <image>` | Mount volume |
| `docker run -e KEY=value <image>` | Set environment variable |
| `docker run --name <name> <image>` | Name the container |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker ps -q` | List only container IDs |
| `docker stop <container>` | Stop container gracefully |
| `docker stop $(docker ps -q)` | Stop all running containers |
| `docker kill <container>` | Force stop container |
| `docker start <container>` | Start stopped container |
| `docker restart <container>` | Restart container |
| `docker rm <container>` | Remove stopped container |
| `docker rm -f <container>` | Force remove running container |
| `docker rm $(docker ps -aq)` | Remove all stopped containers |
| `docker exec -it <container> bash` | Execute bash in container |
| `docker exec <container> <cmd>` | Execute command |
| `docker logs <container>` | View container logs |
| `docker logs -f <container>` | Follow log output |
| `docker logs --tail 100 <container>` | Show last 100 lines |
| `docker inspect <container>` | Detailed container info |
| `docker stats` | Live resource usage |
| `docker top <container>` | Running processes |
| `docker cp <container>:/path /host` | Copy from container to host |
| `docker cp /host <container>:/path` | Copy from host to container |

## Image Commands

| Command | Description |
|---------|-------------|
| `docker build -t <name>:<tag> .` | Build image from Dockerfile |
| `docker build -f <file> .` | Build with specific Dockerfile |
| `docker build --no-cache -t <name> .` | Build without cache |
| `docker pull <image>` | Pull from registry |
| `docker push <name>:<tag>` | Push to registry |
| `docker images` | List all images |
| `docker images -q` | List only image IDs |
| `docker rmi <image>` | Remove image |
| `docker rmi $(docker images -q)` | Remove all images |
| `docker tag <image> <newname>:<tag>` | Tag image |
| `docker history <image>` | Show image layers |
| `docker save -o <file> <image>` | Save to tar archive |
| `docker load -i <file>` | Load from tar archive |
| `docker import <file> <name>` | Import filesystem |

## Volume Commands

| Command | Description |
|---------|-------------|
| `docker volume create <name>` | Create named volume |
| `docker volume ls` | List all volumes |
| `docker volume inspect <name>` | Display volume details |
| `docker volume rm <name>` | Remove volume |
| `docker volume prune` | Remove unused volumes |
| `docker run -v <name>:/data <image>` | Mount named volume |
| `docker run --mount source=<name>,target=/data <image>` | Mount with options |

## Network Commands

| Command | Description |
|---------|-------------|
| `docker network create <name>` | Create custom network |
| `docker network create --driver <driver> <name>` | Create with driver |
| `docker network ls` | List all networks |
| `docker network inspect <name>` | Display network details |
| `docker network connect <net> <container>` | Connect container to network |
| `docker network disconnect <net> <container>` | Disconnect from network |
| `docker network rm <name>` | Remove network |
| `docker network prune` | Remove unused networks |
| `docker run --network <name> <image>` | Run in specific network |

## Docker Compose

| Command | Description |
|---------|-------------|
| `docker compose up` | Create and start containers |
| `docker compose up -d` | Start in detached mode |
| `docker compose up --build` | Rebuild before starting |
| `docker compose down` | Stop and remove containers |
| `docker compose down -v` | Remove containers + volumes |
| `docker compose down --rmi all` | Remove containers + images |
| `docker compose ps` | List running services |
| `docker compose logs` | View all service logs |
| `docker compose logs -f <service>` | Follow specific service logs |
| `docker compose build` | Build/rebuild services |
| `docker compose pull` | Pull latest images |
| `docker compose exec <service> <cmd>` | Execute in service |
| `docker compose run <service> <cmd>` | Run one-off command |
| `docker compose config` | Validate compose file |
| `docker compose restart` | Restart all services |
| `docker compose stop` | Stop without removing |
| `docker compose start` | Start stopped services |

## System Cleanup

| Command | Description |
|---------|-------------|
| `docker system df` | Show disk usage |
| `docker system df -v` | Detailed disk usage |
| `docker container prune` | Remove stopped containers |
| `docker container prune -f` | Force remove containers |
| `docker image prune` | Remove dangling images |
| `docker image prune -a` | Remove all unused images |
| `docker volume prune` | Remove unused volumes |
| `docker network prune` | Remove unused networks |
| `docker system prune` | Remove unused data |
| `docker system prune -a` | Remove all unused data |
| `docker system prune -a --volumes` | Remove everything + volumes |

## Dockerfile Instructions

| Instruction | Description |
|-------------|-------------|
| `FROM <image>` | Set base image |
| `WORKDIR /path` | Set working directory |
| `COPY <src> <dest>` | Copy files from host |
| `COPY . .` | Copy all files to image |
| `ADD <src> <dest>` | Copy + extract/remote URL |
| `RUN <command>` | Execute during build |
| `RUN ["exec", "param"]` | Exec form command |
| `ENV KEY=value` | Set environment variable |
| `ARG NAME=value` | Build-time variable |
| `EXPOSE <port>` | Document listening port |
| `USER <name>` | Set user for commands |
| `CMD ["exec", "param"]` | Default command (exec) |
| `CMD command param` | Default command (shell) |
| `ENTRYPOINT ["exec"]` | Fixed executable |
| `VOLUME ["/data"]` | Create mount point |
| `LABEL key=value` | Add metadata |
| `HEALTHCHECK CMD <cmd>` | Health check |
| `SHELL ["exec", "params"]` | Override default shell |
