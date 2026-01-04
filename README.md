# DevOps Assignment

## Assumptions
- Sample backend/frontend used for demonstration
- No actual application code included


This repository demonstrates a basic DevOps setup using Docker, Docker Compose, Nginx, and Jenkins.

## Architecture
User → Nginx → Frontend  
             → Backend → Database  

## Components
- Frontend container
- Backend container
- PostgreSQL database
- Nginx reverse proxy
- Jenkins CI/CD pipeline

## CI/CD Flow
1. Developer pushes code to GitHub
2. Jenkins pulls the code
3. Docker images are built
4. Application is deployed using Docker Compose

## High Availability
- Containers use restart policies
- Services can be scaled horizontally
- Nginx can act as a load balancer

## Kubernetes (Future Scope)
- Services can be deployed as Kubernetes Deployments
- Ingress for routing
- HPA for auto-scaling

## Caching (Future Scope)
- Redis can be added to reduce database load

