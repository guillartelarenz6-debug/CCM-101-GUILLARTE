
# Laboratory Activity 04 Mission Reflection

The boot time and operational setup of a Docker container are significantly faster than installing an operating system on a Virtual Machine. While a VM requires loading a full guest operating system, virtual hardware drivers, and system services—a process taking several minutes—a Docker container shares the host operating system kernel. It initializes in just a few seconds because it operates as an isolated process on the host using Linux namespaces and control groups (cgroups).

Port mapping (`-p 8080:80`) is necessary because containers run inside isolated network environments with private internal IP addresses. By default, network traffic sent to the host machine on port 8080 cannot reach the web server inside the container. Explicitly mapping host port 8080 to container port 80 creates a bridge that forwards incoming requests directly to the Nginx web server.

When executing the `docker rm` command, the container instance and its writable file layer are permanently deleted. Since container filesystems are stateless by default, any temporary data created inside the container during runtime that is not saved to a persistent Docker volume or bind mount will be lost.

Containerization fundamentally transforms collaboration between software developers and IT operations teams (DevOps). Packaging applications along with their dependencies into immutable Docker images eliminates environment mismatches (the "it works on my machine" problem). Operations teams can reliably run the exact same container image across development, staging, and production environments without dependency conflicts.

Through this activity, my GitHub cloud portfolio continues to grow from theoretical infrastructure models to practical hands-on application deployment and container orchestration skills.
