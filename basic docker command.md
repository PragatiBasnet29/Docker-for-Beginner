
# Run the NGINX image. If the image is not present, it will pull it from Docker Hub.
docker run nginx

# Only pulls the image the first time. For subsequent operations, the same image will be reused.

# List all running containers and display basic information such as container ID, creation date, etc.
docker ps

# Each container gets a unique (random) container ID.

# Run an image with the given name (replace 'image_name' with your desired image).
docker run image_name

# Access Docker Hub to explore and pull images.
hub.docker.com

# Run an interactive terminal session with the image.
docker run -it IMAGE_NAME bash

# Check the operating system by displaying release information.
cat /etc/*release*

# Exit the container.
exit

# Display all running containers.
docker ps

# Run the container with the image and make it sleep for 20 seconds.
docker run image_name sleep 20

# Display all running containers again.
docker ps

# Clear the terminal.
clear

# Display all containers, both running and stopped (including ones that have exited).
docker ps -a

# Difference between the following commands:
# docker run -d docker_image sleep 2000
# - Runs the container in detached mode (-d) and makes it sleep for 2000 seconds in the background.

# docker stop container_id/name
# - Stops the running container with the specified container ID or name.

# Difference between `docker ps` and `docker ps -a`:
# `docker ps` shows only running containers.
# `docker ps -a` shows all containers, including stopped ones.

# If we pull an Ubuntu container and don't run it, the image will be stored locally and can be run later without needing to pull it again.
docker pull ubuntu

# Remove a specific container.
docker rm container_name

# List all images.
docker images

# Remove an image by name.
docker rmi image_name

# Pull the Ubuntu image without running it immediately.
docker pull ubuntu

# Run an Ubuntu container interactively.
docker run ubuntu

# Run an Ubuntu container in detached mode.
docker run -d ubuntu

# Execute a command within a running container (replace 'container_name' with the container's actual name).
docker exec container_name cat /etc/*release*
```

Key corrections:
- Added spaces between `cat` and `/etc/*release*`.
- Clarified the `docker run -d` command's behavior.
- Provided explanations for `docker ps` vs `docker ps -a`.