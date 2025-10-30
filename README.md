# HNG Stage 2 — Blue-Green Deployment

This project demonstrates a blue-green deployment architecture using Docker Compose and NGINX. It runs two identical application containers (`blue` and `green`) and routes traffic based on the active pool defined in environment variables.

## 🔧 Setup Instructions

1. Clone the repository:
   `git clone https://github.com/Sheviantos1/hng13-stage2.git`
   `cd hng13-stage2`


- Create your .env file:
`cp .env.example .env`
- Start the containers:
`docker-compose up -d`


- Access the app:
- Main endpoint: `http://localhost:8080`
- Blue service: `http://localhost:8081`
- Green service: `http://localhost:8082`
🔁 Failover Testing
To simulate failure and test NGINX failover:
`curl http://localhost:8081/chaos/start`


Then access `http://localhost:8080` again to confirm traffic reroutes to the backup pool.

📦 Environment Variables

BLUE_IMAGE=yimikaade/wonderful:devops-stage-two
GREEN_IMAGE=yimikaade/wonderful:devops-stage-two
ACTIVE_POOL=blue
RELEASE_ID_BLUE=blue-v1.0.0
RELEASE_ID_GREEN=green-v1.0.0
PORT=3000

