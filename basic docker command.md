# Docker Commands Guide

This guide covers common Docker commands for running and managing containers.

---

## Basic Docker Commands

### 1. Running an NGINX Container

```bash
docker run nginx
```
- **Explanation**: Runs the NGINX image. If the image is not present, it will pull the image from Docker Hub. This only happens the first time, afterward the same image will be reused for subsequent operations.

### 2. List Running Containers

```bash
docker ps
```
- **Explanation**: Lists all running containers and basic information about them such as:
  - Docker ID
  - Created date
  - Status
- **Note**: Each container gets a unique random ID.

### 3. Running an Image by Name

```bash
docker run <image_name>
```
- **Explanation**: Runs the image with the given name.

### 4. Explore Docker Hub

Visit [hub.docker.com](https://hub.docker.com) to explore available images.

---

## Interacting with Containers

### 5. Run a Container Interactively

```bash
docker run -it IMAGE_NAME bash
```
- **Explanation**: Runs a container interactively with a terminal.

### 6. Check Operating System Information

```bash
cat /etc/*release*
```
- **Explanation**: Displays the operating system release information within the container.

### 7. Exit the Container

```bash
exit
```
- **Explanation**: Exits the container.

### 8. List Running Containers Again

```bash
docker ps
```
- **Explanation**: Lists all currently running containers.

---

## Additional Container Operations

### 9. Run a Container with a Sleep Command

```bash
docker run image_name sleep 20
```
- **Explanation**: Runs the container and makes it sleep for 20 seconds.

### 10. Clear Terminal

```bash
clear
```
- **Explanation**: Clears the terminal screen.

### 11. List All Containers (Running and Stopped)

```bash
docker ps -a
```
- **Explanation**: Lists all containers, including those that are stopped.

---

## Understanding Detached Mode and Stopping Containers

### 12. Running a Container in Detached Mode

```bash
docker run -d docker_image sleep 2000
```
- **Explanation**: Runs the container in detached mode (`-d`), allowing it to run in the background for 2000 seconds.

### 13. Stopping a Running Container

```bash
docker stop container_id/name
```
- **Explanation**: Stops the container with the specified ID or name.

### 14. Difference Between `docker ps` and `docker ps -a`

- `docker ps`: Shows only running containers.
- `docker ps -a`: Shows all containers, including stopped ones.

---

## Pulling, Removing Containers and Images

### 15. Pulling an Ubuntu Container Without Running It

```bash
docker pull ubuntu
```
- **Explanation**: Pulls the Ubuntu image but does not run it. The image is stored locally and can be run later.

### 16. Removing a Container

```bash
docker rm container_name
```
- **Explanation**: Removes the specified container.

### 17. List All Docker Images

```bash
docker images
```
- **Explanation**: Lists all locally available images.

### 18. Removing a Docker Image

```bash
docker rmi image_name
```
- **Explanation**: Removes the specified Docker image from the local system.

---

## Additional Docker Commands

### 19. Pull an Image Without Running It

```bash
docker pull image_name
```
- **Explanation**: Pulls the specified image from Docker Hub but does not run it.

### 20. Running an Ubuntu Container

```bash
docker run ubuntu
```
- **Explanation**: Runs the Ubuntu container.

### 21. Running an Ubuntu Container in Detached Mode

```bash
docker run -d ubuntu
```
- **Explanation**: Runs the Ubuntu container in detached mode.

### 22. Execute a Command in a Running Container

```bash
docker exec container_name cat /etc/*release*
```
- **Explanation**: Runs a command inside the specified container to display the OS release information.

---

This README provides an overview of basic Docker commands for working with containers and images.
