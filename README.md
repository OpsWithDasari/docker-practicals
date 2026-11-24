# 🐳 Docker Practicals – OpsWithDasari

Welcome to the **Docker Practicals Repository!**

This repository is designed to help beginners and DevOps professionals learn Docker from basics to advanced concepts through hands-on practicals, real-time examples, and containerization projects.

Learn how to build Docker images, manage containers, create Dockerfiles, configure networking, manage persistent storage, and deploy applications using Docker.

## 🎯 Learning Objectives

- Understand Docker architecture and components.
- Learn Docker installation and configuration.
- Understand Docker images and containers.
- Execute essential Docker commands.
- Create custom Docker images using Dockerfiles.
- Manage Docker volumes and networks.
- Work with Docker Hub and container registries.
- Understand Docker Compose.
- Containerize real-time applications.
- Implement Docker in DevOps CI/CD pipelines.
- Learn Docker security and best practices.

## 📚 Topics Covered

### 1. Introduction to Docker
- What is Docker?
- Why Docker?
- Virtual Machines vs Containers.
- Docker architecture.
- Docker Engine.
- Docker Client and Daemon.
- Docker Registry.
- Docker lifecycle.

### 2. Docker Installation
- Docker installation on Linux.
- Docker Desktop installation on Windows.
- Docker installation on Ubuntu.
- Verify Docker installation.
- Start and stop Docker services.
- Docker post-installation configuration.

### 3. Basic Docker Commands
- docker --version
- docker info
- docker ps
- docker ps -a
- docker images
- docker pull
- docker run
- docker start
- docker stop
- docker restart
- docker rm
- docker rmi
- docker logs
- docker exec
- docker inspect

### 4. Docker Images
- What are Docker images?
- Image layers.
- Pulling images.
- Listing images.
- Removing images.
- Building custom images.
- Image tagging.
- Pushing images to Docker Hub.

### 5. Docker Containers
- Creating containers.
- Running containers.
- Interactive containers.
- Detached mode.
- Container lifecycle.
- Container logs.
- Container inspection.
- Container troubleshooting.

### 6. Dockerfile
- Introduction to Dockerfile.
- FROM instruction.
- RUN instruction.
- CMD instruction.
- ENTRYPOINT instruction.
- COPY and ADD.
- WORKDIR.
- ENV and ARG.
- EXPOSE.
- USER.
- Docker image optimization.
- Multi-stage Docker builds.

### 7. Docker Volumes and Storage
- Docker storage concepts.
- Docker volumes.
- Bind mounts.
- tmpfs mounts.
- Creating and managing volumes.
- Persistent application data.
- Volume backup and restore.

### 8. Docker Networking
- Docker networking concepts.
- Bridge network.
- Host network.
- None network.
- Custom bridge networks.
- Container communication.
- Port mapping.
- Network troubleshooting.

### 9. Docker Compose
- Introduction to Docker Compose.
- Compose YAML files.
- Services and networks.
- Volumes in Compose.
- Environment variables.
- Running multi-container applications.
- Docker Compose troubleshooting.

### 10. Docker Hub and Registry
- Docker Hub introduction.
- Creating Docker Hub account.
- Docker login.
- Docker tag.
- Docker push.
- Docker pull.
- Private repositories.
- Container registries.

### 11. Docker Security and Best Practices
- Running containers as non-root.
- Image vulnerability scanning.
- Docker secrets.
- Resource limits.
- Image optimization.
- Container security best practices.

## 📂 Repository Structure

```text
docker-practicals/
│
├── README.md
│
├── 01-docker-fundamentals/
├── 02-docker-installation/
├── 03-docker-basic-commands/
├── 04-docker-images/
├── 05-docker-containers/
├── 06-dockerfile/
├── 07-docker-volumes/
├── 08-docker-networking/
├── 09-docker-compose/
├── 10-docker-hub/
├── 11-docker-security/
│
└── real-time-projects/
    ├── project-01-nginx-container/
    ├── project-02-nodejs-docker/
    ├── project-03-mysql-docker/
    ├── project-04-multi-container-application/
    └── project-05-docker-cicd-pipeline/
```

## 💻 First Docker Practical

### Step 1: Verify Docker Installation

```bash
docker --version
docker info
```

### Step 2: Download Nginx Image

```bash
docker pull nginx
```

### Step 3: Run Nginx Container

```bash
docker run -d \
  --name my-nginx \
  -p 8080:80 \
  nginx
```

### Step 4: Verify Running Container

```bash
docker ps
```

### Step 5: Access Nginx Application

Open the following URL in your browser:

http://localhost:8080

### Step 6: View Container Logs

```bash
docker logs my-nginx
```

### Step 7: Stop and Remove Container

```bash
docker stop my-nginx
docker rm my-nginx
```

## 📝 Sample Dockerfile Practical

Create a file named `Dockerfile`.

```dockerfile
FROM nginx:alpine

LABEL maintainer="OpsWithDasari"

COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
```

Create an `index.html` file:

```html
<html>
<head>
    <title>OpsWithDasari</title>
</head>
<body>
    <h1>Welcome to OpsWithDasari!</h1>
    <h2>Learn Docker with Hands-on Practicals</h2>
</body>
</html>
```

Build the Docker image:

```bash
docker build -t opswithdasari-nginx:v1 .
```

Run the container:

```bash
docker run -d -p 8080:80 opswithdasari-nginx:v1
```

## 🚀 Real-Time Docker Projects

1. Deploy an Nginx web server using Docker.
2. Containerize a Python application.
3. Containerize a Node.js application.
4. Deploy MySQL using Docker.
5. Build a multi-container application using Docker Compose.
6. Configure Docker networking between containers.
7. Implement persistent storage using Docker volumes.
8. Push custom images to Docker Hub.
9. Implement Docker image optimization using multi-stage builds.
10. Integrate Docker with Jenkins CI/CD pipelines.

## 🛠️ Prerequisites

- Basic Linux knowledge.
- Basic command-line knowledge.
- Git and GitHub fundamentals.
- Linux or Windows operating system.
- Docker Engine or Docker Desktop.
- Basic application development knowledge (helpful for advanced projects).

## 🎓 Who Can Use This Repository?

- Beginners learning Docker.
- DevOps Engineers.
- Cloud Engineers.
- Software Developers.
- System Administrators.
- Site Reliability Engineers (SRE).
- Students preparing for DevOps interviews.

## 🌟 Learn. Practice. Become an Engineer.

Follow **OpsWithDasari** for practical DevOps tutorials covering Linux, Git, GitHub, Shell Scripting, Docker, Kubernetes, Jenkins, Terraform, AWS, and CI/CD automation.

Happy Learning! 🚀
