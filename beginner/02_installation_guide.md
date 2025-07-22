# Ubuntu Installation Using Docker and Docker Compose

This guide explains how to run an Ubuntu container using Docker and manage it with Docker Compose.

---

## Prerequisites

- **Docker** installed on your system.  
  [Install Docker](https://docs.docker.com/get-docker/)

- **Docker Compose** installed.  
  [Install Docker Compose](https://docs.docker.com/compose/install/)

---

## Step 1: Verify Docker and Docker Compose Installation

Open a terminal and run:

```bash
docker --version
docker compose version
```

---

## Step 2: Build and Run the Container


Run these commands to build the custom image and start the container:

```bash
docker compose up -d --build
```

---

## Step 4: Access the Container

Enter the container with:

```bash
docker exec -it ubuntu_container bash
```


Inside, you can verify installed packages, e.g.,

```bash
curl --version
vim --version
git --version
```

---

## Step 5: Stopping and Removing the Container

```bash
docker compose down
```

If you want to install other packages or add files/configurations, just update the Dockerfile accordingly and rebuild with:

```bash
docker compose up -d --build
```

