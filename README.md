# library-management-microservice-practice
A micro-service-based library management system designed for practice and learning.

A full-stack, distributed Library Management System built with a React frontend and Spring Boot/Spring Cloud microservices backend.

---

## System Architecture

### 1. Frontend
- **Client App** (Port: '5173') -
    Application for users and administrators.

### 2. Backend Infrastructure Services
- **Config Server** (Port: '8888') -
    Centralized configuration repository.

- **Eureka Server** (Port: '8761') -
    Service discovery & registration registry.

### 3. Functional Microservices

| Developer | Service Name | Port | Description |
| :--- | :--- | :--- | :--- |
| Manoj | **Auth Service** | '8081' | User authentication, Authorization & Jwt token generation |
| Manoj | **User Service** | '8082' | Profile management, roles, & membersip details |
| Sahil | **Book Service** | '8083' | Book inventory, catalog, serach, and availability |
| Sahil | **Reservation & Issue Service** | '8084' | Book issuing, return workflows, and reservations |
| Pushkaraj | **Book exchange Service** | '8085' | Peer-to-peer book listing, swap requests, and exchange tracking |
| Pushkaraj | **Report Service** | '8086' | Usage analytics, statistics, and audit reports |

---

## Tech Stack

### Frontend
- **Library:**
        React.js
- **Styling:**
        Tailwind CSS
- **HTTP Client:**
        Axios
- **Icons/Components:**
        fontawesome

### Backend
- **Language & Framework:**
        Java 21, Spring Boot 4, Spring Cloud

- **Service Discovery:**
        Java 25, Spring Boot 4, Spring Cloud

- **API Gateway & Configurations:**
        Spring Cloud Gateway & Config Server

- **Database:**
        PostgreSQL

- **Containerization & Orchestration:**
        Docker, Docker Compose

---

## Git Workflow Rules

1. **'main':**
    Production-ready code only.
    Direct commits restricted.

2. **'dev':**
    Main integration branch.
    All feature branches merged here via Pull Requests(PRs).

3. **Feature Branches:**
    Sub-branches of 'dev' using naming conventions:
    - 'feature/frontend-<feature-name>'.
    - 'feature/<service-name>-<feature-name>'.
    
4. **Code Reviews:**
    Every PR requires review and approval from atleast one teammate before merging into 'dev'.

---

## Getting Started & Local Setup

### Prerequisites:

#### Installations required:
- Docker & Docker compose
- Java 21+
- Maven
- Node.js & npm

---

### Startup Flow:

#### Step 1: Clone repository:
COMMAND:
    
    git clone https://github.com/Rajrc2001/library-management-microservice-practice library-management-system

#### Step 2: Start Supporting Infrastructure via Docker Compose
Run all required infrastructure containers.

COMMAND:

    docker compose up -d

#### Step 3: Start Infrastructure Microservices(Backend)
Run Services:
1. Config Server(8888).
2. Eureka Server(8761).

#### Step 4: Start Functional Microservices(Backend)
Run all services via IDE or terminal.
COMMAND:

    mvn spring-boot:run

#### Step 5: Start Frontend Client
Run all services via IDE or terminal.
COMMAND:

    cd frontend
    npm install
    npm run dev