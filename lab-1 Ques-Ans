Here’s a **README** file in a question-answer format based on your Docker-related tasks:

---

# Docker Lab 1: Question & Answer Guide

## What is the version of Docker Server Engine running on the Host?
- **Answer**: 25.0.5

---

## How many images are available on this host?
- **Answer**: 9

### Output:
```bash
➜ docker images
REPOSITORY                      TAG       IMAGE ID       CREATED       SIZE
nginx                           alpine    0f0eda053dc5   3 weeks ago   43.2MB
nginx                           latest    5ef79149e0ec   3 weeks ago   188MB
postgres                        latest    69092dbdec0d   4 weeks ago   432MB
ubuntu                          latest    edbfe74c41f8   5 weeks ago   78MB
redis                           latest    dae83f665c92   6 weeks ago   117MB
mysql                           latest    a82a8f162e18   6 weeks ago   586MB
alpine                          latest    324bc02ae123   6 weeks ago   7.79MB
kodekloud/simple-webapp-mysql   latest    129dd9f67367   5 years ago   96.6MB
kodekloud/simple-webapp         latest    c6e3cd9aae36   5 years ago   84.8MB
```

---

## What is the difference between a container and an image?
- **Answer**:
  - **Container**: A running instance of an image that provides an isolated environment to run applications.
  - **Image**: A template that contains the application and environment configurations necessary to create a container.

---

## Run a container using the Redis image:
```bash
docker run redis
```

### Output:
```
1:C 09 Sep 2024 11:33:05.319 * oO0OoO0OoO0Oo Redis is starting oO0OoO0OoO0Oo
1:C 09 Sep 2024 11:33:05.319 * Redis version=7.4.0, bits=64, commit=00000000, modified=0, pid=1, just started
1:C 09 Sep 2024 11:33:05.319 # Warning: no config file specified, using the default config. In order to specify a config file use redis-server /path/to/redis.conf
1:M 09 Sep 2024 11:33:05.319 * monotonic clock: POSIX clock_gettime
1:M 09 Sep 2024 11:33:05.320 * Running mode=standalone, port=6379.
1:M 09 Sep 2024 11:33:05.387 * Server initialized
1:M 09 Sep 2024 11:33:05.387 * Ready to accept connections tcp
```

---

## Stop the container you just created:
```bash
docker stop <container_id>
```

### Output:
```bash
docker stop 6aa6e2775a10
```

---

## How many containers are running?
- **Answer**: 0

### Output:
```bash
➜ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

---

## How many containers are present on the host now (including both running and stopped ones)?
- **Answer**: 6

### Output:
```bash
➜ docker ps -a
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS                          PORTS     NAMES
83eaef7bca6b   alpine         "/bin/sh"                About a minute ago   Exited (0) About a minute ago             peaceful_jepsen
f1dd5b39b8c9   alpine         "sleep 1000"             About a minute ago   Up About a minute                         gracious_lichterman
5518210be8e4   nginx:alpine   "/docker-entrypoint.…"   About a minute ago   Up About a minute               80/tcp    nginx-2
872b712dcedb   nginx:alpine   "/docker-entrypoint.…"   About a minute ago   Up About a minute               80/tcp    nginx-1
c1551cd4e784   ubuntu         "sleep 1000"             About a minute ago   Up About a minute                         awesome_northcut
6aa6e2775a10   redis          "docker-entrypoint.s…"   7 minutes ago        Exited (0) 6 minutes ago                  ecstatic_lumiere
```

---

## What is the image used to run the `nginx-1` container?
- **Answer**: `nginx:alpine`

---

## What is the name of the container created using the Ubuntu image?
- **Answer**: `awesome_northcut`

---

## What is the state of the stopped Alpine container?
- **Answer**: Exited

---

## Delete all containers from the Docker host (both running and stopped):
```bash
docker stop <container_id | container_name>
docker rm <container_id | container_name>
```

---

## Delete the Ubuntu image:
```bash
docker rmi ubuntu
```

---

## Pull a Docker image that will be used to run a container later:
```bash
docker pull nginx:1.14-alpine
```

---

## Run a container with the `nginx:1.14-alpine` image and name it `webapp`:
```bash
docker run --name webapp nginx:1.14-alpine
```

---

This README provides answers and commands used to work with Docker containers and images, including basic operations such as running, stopping, pulling, and deleting containers.
