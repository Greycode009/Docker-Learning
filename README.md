# Dockerized Node.js Application

A simple Node.js/Express application containerized with Docker and published to Docker Hub.

## Docker Image

Docker Hub image:

```text
greycode29/nodejs
```

Pull the image with:

```bash
docker pull greycode29/nodejs:latest
```

## Prerequisites

- Docker Desktop installed
- Docker Hub account
- Docker CLI available in the terminal

## Build the Image

From the project directory:

```bash
docker build -t docker-learning .
```

Check the image:

```bash
docker images
```

## Run the Container

Run the application on port `3000`:

```bash
docker run -p 3000:3000 docker-learning
```

Then open:

```text
http://localhost:3000
```

## Run With a Custom Port

For example, expose container port `9000` through host port `5000`:

```bash
docker run -it -e PORT=9000 -p 5000:9000 docker-learning
```

The first port is the host port and the second is the container port.

## Tag the Image for Docker Hub

Tag the local image with the Docker Hub repository:

```bash
docker tag docker-learning greycode29/nodejs:latest
```

Verify the image:

```bash
docker images
```

## Login to Docker Hub

```bash
docker login
```

Enter your Docker Hub credentials when prompted.

## Push the Image

```bash
docker push greycode29/nodejs:latest
```

## Pull the Image

On another machine:

```bash
docker pull greycode29/nodejs:latest
```

## Run the Docker Hub Image

```bash
docker run -p 3000:3000 greycode29/nodejs:latest
```

Then visit:

```text
http://localhost:3000
```

## Useful Docker Commands

### List Images

```bash
docker images
```

### List Running Containers

```bash
docker ps
```

### List All Containers

```bash
docker ps -a
```

### Stop a Container

```bash
docker stop <container-name-or-id>
```

### Remove a Container

```bash
docker rm <container-name-or-id>
```

### Remove an Image

```bash
docker rmi <image-name-or-id>
```

## Docker Workflow

```text
Dockerfile
    ↓
docker build
    ↓
Docker Image
    ↓
docker tag
    ↓
greycode29/nodejs:latest
    ↓
docker push
    ↓
Docker Hub
    ↓
docker pull
    ↓
Run anywhere with Docker
```

## What I Learned

- How to build a Docker image
- How to run a Node.js application inside a container
- How to map host and container ports
- How to tag an image for Docker Hub
- How to push an image to Docker Hub
- How to pull and run a published Docker image

## Local notes
- Docker project initialized.
