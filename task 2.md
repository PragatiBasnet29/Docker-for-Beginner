```asciidoc
= Docker Usage Guide

This README provides a guide to common Docker commands including running containers, port mapping, volume mapping, inspecting containers, and viewing logs.

== Table of Contents
. Running Redis
. Standard Input and Interactive Mode
. Port Mapping
. Volume Mapping
. Inspecting Containers
. Viewing Container Logs

== Running Redis
By default, Docker pulls and runs the latest version of Redis when you don't specify a version.

```bash
docker run redis
```

If you want to run an older version of Redis, you need to specify the version by using a tag.

```bash
docker run redis:4.0
```

This will run Redis version `4.0`.

== Standard Input and Interactive Mode
Some Docker images, like `kodekloud/simple-prompt-docker`, expect user input. By default, if you run the following command, it will skip the prompt and return a default message.

```bash
docker run kodekloud/simple-prompt-docker
```

Output:
```
Hello and welcome!
```

To interact with the application inside the container, you need to use the `-i` flag for interaction and the `-t` flag to attach the terminal:

```bash
docker run -it kodekloud/simple-prompt-docker
```

This allows interaction with the container:
```
/prompt-application$ ./app.sh
Welcome! Please enter your name: Mumshad
Hello and welcome Mumshad!
```

== Port Mapping
Port mapping allows you to expose container ports to your local machine. Running a web application inside Docker typically exposes ports inside the container, but you need to map it to your host’s port for external access.

For example, running a web app:

```bash
docker run kodekloud/webapp
```

This runs the app inside the container, but to access it on your local machine, map port `50000` in the container to port `80` on the host:

```bash
docker run -p 80:50000 kodekloud/webapp
```

You can run multiple containers on different ports by assigning each one a different host port.

== Volume Mapping
Volume mapping allows you to persist data outside the container or share files between your host and the container. By default, container data will be deleted when the container is removed. For example:

```bash
docker run mysql
```

This runs MySQL, but all the data will be lost if you delete the container. To persist the data, use volume mapping:

```bash
docker run -v /opt/datadir:/var/lib/mysql mysql
```

In this case, `/opt/datadir` on your host is mapped to `/var/lib/mysql` inside the container, so the MySQL data will persist in `/opt/datadir` even if the container is stopped or deleted.

== Inspecting Containers
The `docker inspect` command provides detailed information about a container, including its configuration, network settings, and runtime parameters.

```bash
docker inspect blissful_hopper
```

This will output a JSON structure with comprehensive details about the container.

== Viewing Container Logs
To view the logs produced by a running or stopped container, use the `docker logs` command:

```bash
docker logs <container_name>
```

This shows all output from the container, including standard output and error logs, which is useful for debugging.

== Conclusion
This guide covers essential Docker commands such as running containers, interacting with them, mapping ports, persisting data through volume mapping, and retrieving logs.
```

### Summary of Changes:
1. **Command Blocks**: All Docker commands are now inside `bash` blocks for clarity.
2. **Descriptions Outside**: Explanations are placed outside the code blocks to make it easier to distinguish between the command and its description.
3. **Consistent Formatting**: Ensured all sections follow a consistent format for easy readability.

Let me know if you'd like further adjustments!
