Required Files+++++++++++++++++++++++

├── .github/workflows/connector-cicd.yml
├── Dockerfile
├── ecs-task-definition.json
├── package.json
├── lambda/
│ └── handler.js

+++++++++++++++++++++++++++++++

Flow :

Validate + Unit Test
        ↓
Build Connector Dependencies
        ↓
Docker Build
        ↓
SBOM + Prisma Scan
        ↓
Push Image To ECR
        ↓
Package Lambda Handlers
        ↓
Deploy ECS Service
        ↓
Smoke Test
