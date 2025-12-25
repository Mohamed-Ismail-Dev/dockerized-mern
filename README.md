# MERN Stack Application with Docker

A simple **MERN (MongoDB, Express, React, Node.js)** stack application, containerized using **Docker** and easily deployable with **Docker Compose**.

---

## Table of Contents

- [Features](#features)  
- [Prerequisites](#prerequisites)  
- [Docker Setup](#docker-setup)  
  - [Create Network](#create-network)  
  - [Run MongoDB](#run-mongodb)  
  - [Build and Run Backend](#build-and-run-backend)  
  - [Build and Run Frontend](#build-and-run-frontend)  
- [Using Docker Compose](#using-docker-compose)  
- [Screenshots](#screenshots)  
- [License](#license)  

---

## Features

- React frontend served via Docker container  
- Node.js backend with Express API  
- MongoDB database for employee records  
- Containerized setup using Docker and Docker Compose  

---

## Prerequisites

- Docker installed  
- Docker Compose installed  
- Git installed  

---

### Create a network for the docker containers

`docker network create test`

### Build the client 

```sh
cd /frontend
docker build -t mern-client .
```

### Run the client

`docker run --name=client --network=test -d -p 80:80 mern-client`

### Verify the client is running

Open your browser and type `http://localhost`

### Run the mongodb container

`docker run --network=demo --name mongodb -d -p 27017:27017 -v ~/opt/data:/data/db mongo:latest`

### Build the server

```sh
cd /backend
docker build -t mern-server .
```

### Run the server

`docker run --name=server --network=test -d -p 5050:5050 mern-server`

## Using Docker Compose

`docker compose up -d`

<img width="1919" height="816" alt="Screenshot 2025-12-25 144129" src="https://github.com/user-attachments/assets/1c4a2b4d-d61c-4a0c-8e1a-7e02c7134da9" />


