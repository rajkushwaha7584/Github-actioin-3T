# Github-actioin-3T

This project demonstrates a complete CI/CD deployment flow using **GitHub Actions, Docker, Docker Hub, AWS EC2, AWS OIDC, AWS SSM, and Docker Compose**.

The application contains:

- Frontend service
- Backend service
- MySQL database
- Docker Compose based deployment
- GitHub Actions CI/CD pipeline
- AWS OIDC + SSM based EC2 deployment without SSH key

---

## Project Flow

```text
Code push
   ↓
CI pipeline
   ↓
Docker image build/push
   ↓
CD pipeline
   ↓
GitHub OIDC se AWS role assume karta hai
   ↓
AWS SSM command EC2 par bhejta hai
   ↓
EC2 par commands run hoti hain:
   git pull
   .env create
   docker compose up -d --build
