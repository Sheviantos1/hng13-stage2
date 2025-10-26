# HNGx Stage 2 DevOps Task – Blue/Green Deployment

## 🚀 Overview

This project sets up a Blue/Green deployment using Docker Compose and NGINX. Blue is the active app, Green is the backup. NGINX handles automatic failover and retries.

## 🧱 Stack

- Docker Compose
- NGINX
- Node.js (prebuilt images)
- Bash templating

## 📦 Setup

1. Clone the repo
2. Create a `.env` file based on `.env.example`
3. Run:

```bash
docker-compose up -d