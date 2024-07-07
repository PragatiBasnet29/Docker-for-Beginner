# Lab-1

## Docker Setup and Management

### Docker Installation

Ensure Docker is installed on your system. You can check the Docker version with the following command:

```sh
sudo docker version
```

### Managing Docker Containers

#### Listing All Containers

To list all containers (running and stopped), use:

```sh
docker ps -a
```

#### Running a Container

To run a container, for example, Redis:

```sh
docker run redis
```

#### Stopping a Container

To stop a running container, use:

```sh
docker stop <container_id_or_name>
```

Example:

```sh
docker stop inspiring_bose
```

#### Removing a Container

To remove a container, first stop it (if it's running), then remove it:

```sh
docker rm <container_id_or_name>
```

Example:

```sh
docker rm jolly_rosalind
```

#### Running a Container in Detached Mode

To run a container in detached mode, use the `-d` flag:

```sh
docker run -d nginx:1.14-alpine webapp
```

### Managing Docker Images

#### Listing All Images

To list all Docker images, use:

```sh
docker images
```

#### Pulling an Image

To pull an image from a repository, use:

```sh
docker pull <image_name>
```

Example:

```sh
docker pull nginx:1.14-alpine
```

#### Removing an Image

To remove an image, use:

```sh
docker rmi <image_name>
```

Example:

```sh
docker rmi ubuntu
```

### Useful Docker Commands

#### Running a Command in a New Container

To run a command in a new container, use:

```sh
docker run <image_name> <command>
```

Example:

```sh
docker run alpine /bin/sh
```

#### Inspecting a Container

To display detailed information on a container, use:

```sh
docker inspect <container_id_or_name>
```

#### Viewing Container Logs

To view the logs of a container, use:

```sh
docker logs <container_id_or_name>
```

#### Executing a Command in a Running Container

To execute a command in a running container, use:

```sh
docker exec -it <container_id_or_name> <command>
```

Example:

```sh
docker exec -it inspiring_bose /bin/sh
```

### Example Workflow

1. **Pulling an Image:**

    ```sh
    docker pull nginx:1.14-alpine
    ```

2. **Running a Container:**

    ```sh
    docker run -d nginx:1.14-alpine webapp
    ```

3. **Listing Running Containers:**

    ```sh
    docker ps
    ```

4. **Stopping a Container:**

    ```sh
    docker stop webapp
    ```

5. **Removing a Container:**

    ```sh
    docker rm webapp
    ```

6. **Removing an Image:**

    ```sh
    docker rmi nginx:1.14-alpine
    ```

---

This README file provides a basic guide to managing Docker containers and images, ensuring you can easily perform common tasks.
