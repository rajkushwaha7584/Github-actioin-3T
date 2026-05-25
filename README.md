# Github-actioin-3T
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
