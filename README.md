Required Files+++++++++++++++++++++++

├── .github/workflows/connector-cicd.yml
├── Dockerfile
├── ecs-task-definition.json
├── package.json
├── lambda/
│ └── handler.js

+++++++++++++++++++++++++++++++

Flow :

Validate
   ↓
Unit Tests
   ↓
Build Connector Dependencies
   ↓
Build Docker Image (Dockerfile)
   ↓
Trivy Scan
   ↓
Push to ECR
   ↓
Package Lambda
   ↓
Deploy ECS Service
   ↓
Smoke Test
