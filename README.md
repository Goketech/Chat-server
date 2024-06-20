# Chat Server Project

## Overview
This project is a chat server built with Node.js, RabbitMQ, Nginx, and Docker. The chat server allows multiple clients to communicate with each other in real-time, leveraging RabbitMQ for message brokering, Nginx for load balancing, and Docker for containerization.

## Features
- Real-time communication between clients
- Scalable and load-balanced architecture
- Message brokering with RabbitMQ
- Containerized environment using Docker
- Reverse proxy and load balancing with Nginx

## Prerequisites
- Docker installed on your system
- Docker Compose installed on your system
- Node.js installed on your system
- Typescript installed on your system

## Setup

### Step 1: Clone the Repository
```bash
git clone https://github.com/goketech/chat-server.git
cd chat-server
```

### Step 2: Configure Environment Variables

Create a .env file in the chat-service directory and add the following environment variables:

```makefile
NODE_ENV="development"
PORT=8082
JWT_SECRET="{your_secret}"
MONGO_URI="{your_mongo_db_uri}"
MESSAGE_BROKER_URL="{RabbitMQ_uri}"
```

Create a .env file in the user-service directory and add the following environment variables:

```makefile
NODE_ENV="development"
PORT=8081
JWT_SECRET="{your_secret}"
MONGO_URI="{your_mongo_db_uri}"
MESSAGE_BROKER_URL="{RabbitMQ_uri}"
```

Create a .env file in the notification-service directory and add the following environment variables:

```makefile

NODE_ENV="development"
PORT=8083
MESSAGE_BROKER_URL="{RabbitMQ_uri}"
SMTP_HOST="{smtp_host}"
SMTP_PORT=smt_port
SMTP_USER="{smtp_user}"
SMTP_PASS="{smtp_password"
EMAIL_FROM="sender_email"
```

### Step 2: Build and Start the Docker Containers

```bash
docker-compose up --build
```
