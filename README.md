# Hospital Management System

A comprehensive, scalable, and user-friendly Hospital Management System designed to streamline hospital operations, patient care, and administrative processes.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Deployment Guide](#deployment-guide)
- [API Documentation](#api-documentation)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## 🏥 Project Overview

The Hospital Management System is a modern, integrated solution for managing all aspects of hospital operations including:

- **Patient Management**: Registration, records, and medical history
- **Appointment Scheduling**: Efficient scheduling and management
- **Staff Management**: Employee records and shift management
- **Billing & Invoicing**: Financial tracking and reporting
- **Department Management**: Organization and resource allocation
- **Inventory Management**: Medical supplies and equipment tracking
- **Lab Management**: Test ordering and results tracking
- **Pharmacy Management**: Medication dispensing and tracking

This system is built with modern web technologies ensuring reliability, scalability, and ease of use.

## ✨ Features

### Core Features

#### 1. **Patient Management**
- Patient registration and admission
- Medical history and records management
- Patient search and filtering
- Emergency contact information
- Insurance details management
- Patient discharge management

#### 2. **Appointment System**
- Real-time appointment scheduling
- Calendar view with availability
- Appointment reminders
- Appointment history tracking
- Doctor availability management
- Appointment cancellation and rescheduling

#### 3. **Staff Management**
- Employee records and profiles
- Role-based access control (RBAC)
- Shift scheduling and management
- Staff performance tracking
- Leave management
- Department assignments

#### 4. **Doctor Management**
- Doctor profiles and specialties
- Availability and schedule management
- Patient consultation history
- Prescription management
- Medical qualifications and certifications

#### 5. **Billing & Invoicing**
- Automated billing generation
- Invoice management and tracking
- Payment processing
- Insurance claim management
- Financial reports and analytics
- Receipt generation

#### 6. **Department Management**
- Department creation and management
- Department-wise resource allocation
- Staff assignment to departments
- Department performance metrics

#### 7. **Inventory Management**
- Medical supplies tracking
- Equipment inventory
- Stock level monitoring
- Low stock alerts
- Supplier management
- Inventory reports

#### 8. **Lab Management**
- Lab test ordering
- Test result tracking
- Sample management
- Lab report generation
- Test pricing and billing integration

#### 9. **Pharmacy Management**
- Medicine inventory
- Prescription fulfillment
- Medicine stock tracking
- Expiry date management
- Pharmacy reports

#### 10. **Administrative Features**
- Dashboard and analytics
- User management
- System configuration
- Data backup and recovery
- Audit logs
- Multi-user access control

## 🏗️ Architecture

### System Architecture Overview

```
┌─────────────────────────────────────────────────────────┐
│                    Frontend Layer                        │
│  (React/Vue/Angular - UI Components & Pages)            │
└──────────────────┬──────────────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────────────┐
│                   API Gateway Layer                      │
│  (Request routing, authentication, load balancing)      │
└──────────────────┬──────────────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────────────┐
│               Backend Services Layer                     │
│ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │
│ │ Patient Svc  │ │Appointment   │ │  Staff Svc   │    │
│ │              │ │  Svc         │ │              │    │
│ └──────────────┘ └──────────────┘ └──────────────┘    │
│ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │
│ │ Billing Svc  │ │ Inventory    │ │  Lab Svc     │    │
│ │              │ │  Svc         │ │              │    │
│ └──────────────┘ └──────────────┘ └──────────────┘    │
└──────────────────┬──────────────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────────────┐
│              Data Access Layer (DAL)                     │
│  (ORM, Query builders, Database abstraction)            │
└──────────────────┬──────────────────────────────────────┘
                   │
┌──────────────────▼──────────────────────────────────────┐
│           Database & Storage Layer                       │
│  (PostgreSQL/MySQL, Redis Cache, File Storage)          │
└─────────────────────────────────────────────────────────┘
```

### Technology Stack

**Frontend:**
- React.js / Vue.js / Angular (Modern UI Framework)
- HTML5 / CSS3 / SCSS
- JavaScript/TypeScript
- State Management (Redux/Vuex/NgRx)
- HTTP Client (Axios/Fetch API)

**Backend:**
- Node.js / Python / Java / .NET (Server Runtime)
- Express.js / Spring Boot / Django / ASP.NET
- RESTful API Architecture
- JWT/OAuth 2.0 Authentication
- Microservices Architecture (Optional)

**Database:**
- PostgreSQL (Primary Relational Database)
- MySQL (Alternative)
- MongoDB (For document storage if needed)
- Redis (Caching & Session Management)

**DevOps & Deployment:**
- Docker & Docker Compose
- Kubernetes (For production scaling)
- CI/CD Pipeline (GitHub Actions / Jenkins / GitLab CI)
- AWS / Azure / Google Cloud (Cloud Hosting)
- Nginx (Reverse Proxy & Load Balancer)

**Additional Tools:**
- JWT for Authentication
- Swagger/OpenAPI (API Documentation)
- Jest/Mocha (Testing Frameworks)
- SonarQube (Code Quality)
- ELK Stack (Logging & Monitoring)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

### System Requirements
- **OS**: Windows 10+, macOS 10.14+, or Linux (Ubuntu 18.04+)
- **RAM**: Minimum 4GB (8GB recommended)
- **Disk Space**: Minimum 10GB

### Software Dependencies

1. **Node.js & npm**
   - Version: Node.js 14.x or higher
   - Download: https://nodejs.org/

2. **Git**
   - Download: https://git-scm.com/

3. **Database**
   - PostgreSQL 12+ or MySQL 8.0+
   - Download: https://www.postgresql.org/ or https://www.mysql.com/

4. **Docker** (Optional but recommended)
   - Download: https://www.docker.com/

5. **Python** (If backend is Python-based)
   - Version: Python 3.8 or higher
   - Download: https://www.python.org/

6. **Java** (If backend is Java-based)
   - Version: JDK 11 or higher
   - Download: https://www.oracle.com/java/

## 🚀 Setup Instructions

### Step 1: Clone the Repository

```bash
git clone https://github.com/sumbwecommunityhospital-ui/hospital-management-system.git
cd hospital-management-system
```

### Step 2: Install Dependencies

#### Frontend Setup
```bash
cd frontend
npm install
# or
yarn install
```

#### Backend Setup

**For Node.js/Express Backend:**
```bash
cd backend
npm install
```

**For Python/Django Backend:**
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

**For Java/Spring Boot Backend:**
```bash
cd backend
mvn clean install
# or
gradle build
```

### Step 3: Database Setup

#### PostgreSQL Setup

```bash
# Create database
createdb hospital_management_system

# Create user (optional)
createuser hospital_user
```

Then configure your database connection in the backend `.env` file.

#### MySQL Setup

```bash
# Login to MySQL
mysql -u root -p

# Create database
CREATE DATABASE hospital_management_system;
CREATE USER 'hospital_user'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON hospital_management_system.* TO 'hospital_user'@'localhost';
FLUSH PRIVILEGES;
```

### Step 4: Environment Configuration

Create a `.env` file in the backend directory:

```env
# Server Configuration
NODE_ENV=development
PORT=5000
HOST=localhost

# Database Configuration
DB_HOST=localhost
DB_PORT=5432
DB_NAME=hospital_management_system
DB_USER=hospital_user
DB_PASSWORD=your_password
DB_DIALECT=postgres  # or mysql

# JWT Configuration
JWT_SECRET=your_jwt_secret_key_here
JWT_EXPIRY=7d

# Frontend Configuration
FRONTEND_URL=http://localhost:3000

# Email Configuration
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASSWORD=your_app_password
SMTP_FROM=noreply@hospitalsystem.com

# File Upload Configuration
UPLOAD_DIR=./uploads
MAX_FILE_SIZE=5242880  # 5MB

# Logging
LOG_LEVEL=debug
LOG_FILE=./logs/app.log

# Redis Configuration
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=

# External APIs
PAYMENT_GATEWAY_KEY=your_payment_key
```

Create a `.env` file in the frontend directory:

```env
REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_ENV=development
```

### Step 5: Database Migration (if applicable)

```bash
# Node.js/Sequelize
npm run migrate

# Python/Django
python manage.py migrate

# Spring Boot
mvn spring-boot:run
```

## 🔧 Configuration

### Authentication Configuration

The system uses JWT (JSON Web Tokens) for authentication:

1. Users log in with credentials
2. Backend verifies and issues JWT token
3. Token is stored in frontend (localStorage/sessionStorage)
4. Token is sent in Authorization header for subsequent requests
5. Backend validates token for protected routes

### Role-Based Access Control (RBAC)

Predefined roles:
- **Admin**: Full system access
- **Doctor**: Patient management, prescriptions
- **Nurse**: Patient monitoring, vital signs
- **Receptionist**: Appointments, patient registration
- **Lab Technician**: Lab tests and results
- **Pharmacist**: Pharmacy and prescriptions
- **Accountant**: Billing and invoicing
- **Staff**: Limited access based on assignment

### Email Configuration

The system sends emails for:
- Appointment reminders
- Appointment confirmations
- Password reset
- Invoice notifications

Ensure SMTP credentials are configured in `.env`.

## ▶️ Running the Application

### Development Mode

#### Frontend (Terminal 1)
```bash
cd frontend
npm start
# Frontend will be available at http://localhost:3000
```

#### Backend (Terminal 2)

**Node.js:**
```bash
cd backend
npm start
# or use nodemon for auto-reload
npm run dev
```

**Python/Django:**
```bash
cd backend
source venv/bin/activate
python manage.py runserver
```

**Java/Spring Boot:**
```bash
cd backend
mvn spring-boot:run
# or
./gradlew bootRun
```

#### Redis (Terminal 3 - if needed)
```bash
redis-server
```

### Production Mode

```bash
# Frontend Build
cd frontend
npm run build

# Backend Production Start
cd backend
npm run start:prod
```

## 📦 Deployment Guide

### Docker Deployment

#### Prerequisites
- Docker & Docker Compose installed

#### Step 1: Create Dockerfile for Frontend

Create `frontend/Dockerfile`:

```dockerfile
FROM node:16-alpine as builder
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

FROM nginx:alpine
COPY --from=builder /app/build /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

#### Step 2: Create Dockerfile for Backend

Create `backend/Dockerfile`:

```dockerfile
FROM node:16-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 5000
CMD ["npm", "start"]
```

#### Step 3: Docker Compose

Create `docker-compose.yml`:

```yaml
version: '3.8'

services:
  postgres:
    image: postgres:13-alpine
    environment:
      POSTGRES_DB: hospital_management_system
      POSTGRES_USER: hospital_user
      POSTGRES_PASSWORD: your_password
    ports:
      - "5432:5432"
    volumes:
      - postgres_data:/var/lib/postgresql/data
    networks:
      - hospital-network

  redis:
    image: redis:7-alpine
    ports:
      - "6379:6379"
    networks:
      - hospital-network

  backend:
    build:
      context: ./backend
      dockerfile: Dockerfile
    environment:
      DB_HOST: postgres
      REDIS_HOST: redis
    ports:
      - "5000:5000"
    depends_on:
      - postgres
      - redis
    networks:
      - hospital-network

  frontend:
    build:
      context: ./frontend
      dockerfile: Dockerfile
    ports:
      - "80:80"
    depends_on:
      - backend
    networks:
      - hospital-network

volumes:
  postgres_data:

networks:
  hospital-network:
    driver: bridge
```

#### Step 4: Deploy with Docker Compose

```bash
docker-compose up -d
```

The application will be available at `http://localhost`

### Cloud Deployment (AWS Example)

#### Step 1: Push Docker Image to ECR

```bash
# Create ECR repository
aws ecr create-repository --repository-name hospital-system

# Build and push image
docker build -t hospital-system:latest .
docker tag hospital-system:latest <aws_account_id>.dkr.ecr.<region>.amazonaws.com/hospital-system:latest
docker push <aws_account_id>.dkr.ecr.<region>.amazonaws.com/hospital-system:latest
```

#### Step 2: Deploy to ECS/EKS

```bash
# For ECS Fargate
aws ecs create-service --cluster hospital-cluster \
  --service-name hospital-service \
  --task-definition hospital-task:1 \
  --desired-count 3 \
  --launch-type FARGATE
```

#### Step 3: Setup RDS Database

```bash
# Create RDS PostgreSQL instance via AWS Console or CLI
aws rds create-db-instance \
  --db-instance-identifier hospital-db \
  --db-instance-class db.t3.micro \
  --engine postgres \
  --master-username hospital_user
```

#### Step 4: Setup Load Balancer

- Create Application Load Balancer (ALB)
- Configure target groups
- Setup SSL/TLS certificates
- Configure health checks

### Kubernetes Deployment

Create `k8s/deployment.yaml`:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: hospital-backend
spec:
  replicas: 3
  selector:
    matchLabels:
      app: hospital-backend
  template:
    metadata:
      labels:
        app: hospital-backend
    spec:
      containers:
      - name: backend
        image: hospital-system:latest
        ports:
        - containerPort: 5000
        env:
        - name: DB_HOST
          valueFrom:
            configMapKeyRef:
              name: hospital-config
              key: db-host
        - name: DB_PASSWORD
          valueFrom:
            secretKeyRef:
              name: hospital-secrets
              key: db-password
---
apiVersion: v1
kind: Service
metadata:
  name: hospital-backend-service
spec:
  selector:
    app: hospital-backend
  ports:
  - protocol: TCP
    port: 80
    targetPort: 5000
  type: LoadBalancer
```

Deploy:

```bash
kubectl apply -f k8s/deployment.yaml
```

### CI/CD Pipeline (GitHub Actions)

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy Hospital Management System

on:
  push:
    branches: [ main, develop ]
  pull_request:
    branches: [ main ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    
    - name: Setup Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '16'
    
    - name: Install dependencies
      run: |
        cd frontend && npm install
        cd ../backend && npm install
    
    - name: Run tests
      run: |
        cd frontend && npm test
        cd ../backend && npm test
    
    - name: SonarQube Scan
      uses: SonarSource/sonarcloud-github-action@master
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}

  build:
    needs: test
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'
    
    steps:
    - uses: actions/checkout@v2
    
    - name: Build Docker images
      run: |
        docker build -t hospital-system-frontend:${{ github.sha }} ./frontend
        docker build -t hospital-system-backend:${{ github.sha }} ./backend
    
    - name: Push to Docker Hub
      run: |
        docker login -u ${{ secrets.DOCKER_USERNAME }} -p ${{ secrets.DOCKER_PASSWORD }}
        docker push hospital-system-frontend:${{ github.sha }}
        docker push hospital-system-backend:${{ github.sha }}
    
    - name: Deploy to production
      run: |
        # Add your deployment commands here
        echo "Deploying to production..."
```

## 📚 API Documentation

### Authentication Endpoints

#### Login
```
POST /api/auth/login
Content-Type: application/json

{
  "email": "doctor@hospital.com",
  "password": "password123"
}

Response:
{
  "token": "eyJhbGciOiJIUzI1NiIs...",
  "user": {
    "id": 1,
    "email": "doctor@hospital.com",
    "role": "doctor"
  }
}
```

#### Logout
```
POST /api/auth/logout
Authorization: Bearer <token>
```

### Patient Endpoints

#### Get All Patients
```
GET /api/patients
Authorization: Bearer <token>
```

#### Create Patient
```
POST /api/patients
Authorization: Bearer <token>
Content-Type: application/json

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "phone": "1234567890",
  "dateOfBirth": "1990-01-15"
}
```

#### Get Patient by ID
```
GET /api/patients/:id
Authorization: Bearer <token>
```

#### Update Patient
```
PUT /api/patients/:id
Authorization: Bearer <token>
Content-Type: application/json
```

#### Delete Patient
```
DELETE /api/patients/:id
Authorization: Bearer <token>
```

### Appointment Endpoints

#### Get Appointments
```
GET /api/appointments?doctorId=1&patientId=1&status=scheduled
Authorization: Bearer <token>
```

#### Create Appointment
```
POST /api/appointments
Authorization: Bearer <token>
Content-Type: application/json

{
  "patientId": 1,
  "doctorId": 2,
  "scheduledTime": "2026-01-10T14:00:00Z",
  "reason": "Regular checkup"
}
```

For complete API documentation, see [API_DOCUMENTATION.md](./API_DOCUMENTATION.md)

## 📁 Project Structure

```
hospital-management-system/
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Patient/
│   │   │   ├── Appointment/
│   │   │   ├── Doctor/
│   │   │   └── ...
│   │   ├── pages/
│   │   ├── services/
│   │   ├── redux/
│   │   ├── styles/
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   └── Dockerfile
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── middleware/
│   │   ├── services/
│   │   ├── utils/
│   │   ├── config/
│   │   └── app.js
│   ├── tests/
│   ├── .env.example
│   ├── package.json
│   ├── Dockerfile
│   └── server.js
├── docker-compose.yml
├── kubernetes/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── configmap.yaml
├── .github/
│   └── workflows/
│       └── deploy.yml
├── README.md
├── API_DOCUMENTATION.md
└── CONTRIBUTING.md
```

## 🧪 Testing

### Run Unit Tests

```bash
# Frontend
cd frontend
npm test

# Backend
cd backend
npm test
```

### Run Integration Tests

```bash
npm run test:integration
```

### Run E2E Tests

```bash
npm run test:e2e
```

### Code Coverage

```bash
npm run test:coverage
```

## 📝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please read [CONTRIBUTING.md](./CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 🐛 Troubleshooting

### Common Issues

#### Port Already in Use
```bash
# Find process using port 5000
lsof -i :5000
# Kill process
kill -9 <PID>
```

#### Database Connection Error
- Verify database is running
- Check credentials in `.env`
- Ensure database name exists

#### Node Modules Issues
```bash
rm -rf node_modules package-lock.json
npm install
```

#### Database Migration Issues
```bash
npm run migrate:rollback
npm run migrate
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## 📞 Support

For support, email support@hospitalsystem.com or open an issue in the GitHub repository.

### Getting Help
- 📖 **Documentation**: See [docs/](./docs/) folder
- 🐛 **Report Bug**: [GitHub Issues](https://github.com/sumbwecommunityhospital-ui/hospital-management-system/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/sumbwecommunityhospital-ui/hospital-management-system/discussions)

## 🙏 Acknowledgments

- Thanks to all contributors
- Community feedback and suggestions
- Open-source libraries and frameworks used

---

**Last Updated**: 2026-01-06  
**Version**: 1.0.0  
**Maintainer**: Sumbwe Community Hospital UI Team
