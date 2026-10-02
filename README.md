# City-wide Hospital Resource Management

A full-stack healthcare operations platform designed to manage patient flow, appointments, queue coordination, hospital admissions, and inter-hospital transfers across a city-wide network of medical facilities.

This repository combines a Java Spring Boot backend with an Angular frontend to provide a working hospital management system for staff, doctors, and administrators.

## Project Overview

The application is built to support:
- appointment booking and queue management
- doctor-specific patient monitoring dashboards
- patient history and medical record tracking
- admission and bed allocation workflows
- ICU and specialty transfer coordination between hospitals
- WhatsApp-based appointment interactions and bot-driven workflows

## Architecture

```text
City-wide-hospital-resource-management/
├── hospital-backend/       # Spring Boot REST API and business logic
│   ├── src/main/java/      # Java backend source code
│   ├── src/test/java/      # Backend tests
│   ├── pom.xml             # Maven config
│   └── target/             # Build artifacts
│
├── hospital-frontend/      # Angular UI application
│   ├── src/               # Frontend source code
│   ├── public/            # Static assets
│   ├── package.json        # NPM scripts and dependencies
│   ├── angular.json        # Angular project config
│   └── ...
│
├── README.md               # Repository overview
├── CHANGES_ADDED.md        # Feature and enhancement notes
├── .idea/                  # IDE configuration
└── ...
```

## Key Features

### Patient & Queue Management
- appointment booking for patients
- queue generation and token assignment
- doctor-scoped queue views
- patient lookup by ID or phone number

### Clinical Workflows
- consultation completion and medical record creation
- diagnosis, prescription, symptoms, and vitals tracking
- patient medical history access for doctors
- follow-up scheduling support

### Hospital Resource Coordination
- bed availability checks
- admission requests and bed assignment
- ICU transfer workflows
- city-wide hospital search for resource shortages

### Communication & Automation
- WhatsApp booking flow
- demo bot simulation for patient interaction
- webhook support for inbound WhatsApp messages

## Technology Stack

### Backend
- Java 21
- Spring Boot 3.4.2
- Spring Web
- Spring Data JPA
- Spring Security
- WebSockets
- MySQL
- JWT authentication

### Frontend
- Angular 22
- TypeScript
- RxJS
- HTML / CSS
- Angular CLI

## Repository Details

This repository is primarily composed of:
- Java: 65.7%
- HTML: 13.5%
- TypeScript: 11.1%
- CSS: 8.4%
- Python: 1.3%

## Prerequisites

Before running the project, install:
- Java 21 or newer
- Maven
- Node.js 20 or newer
- npm
- MySQL database

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Priyanshu0-O/City-wide-hospital-resource-management.git
cd City-wide-hospital-resource-management
```

### 2. Start the backend

```bash
cd hospital-backend
mvn clean install
mvn spring-boot:run
```

The backend exposes the API and handles business logic, authentication, queue processing, medical records, and hospital resource coordination.

### 3. Start the frontend

```bash
cd hospital-frontend
npm install
npm start
```

The frontend should be available locally at:

```text
http://localhost:4200/
```

## Configuration Notes

The project includes backend configuration for:
- MySQL connection settings
- JWT authentication
- WhatsApp integration (if enabled)
- application-specific hospital and resource settings

Common configuration files include:
- `hospital-backend/src/main/resources/application.yml`
- environment variables for secrets and external services

## Usage Flow

A typical flow in the system may look like:
1. A patient books an appointment.
2. The system creates a queue entry and allocates a token.
3. A doctor reviews the queue and completes the consultation.
4. The doctor records diagnosis, prescription, and vitals.
5. If required, the system initiates an admission or transfer.
6. The application updates city-wide hospital resource data.

## Project Status

This repository is a demo-ready healthcare management system with both backend and frontend components working together for city-wide patient and hospital resource management.

## Notes

The repository also contains a `CHANGES_ADDED.md` file documenting major feature additions and bug fixes implemented across the project, including:
- patient history tracking
- WhatsApp booking support
- doctor-specific dashboards
- ICU transfer improvements
- improved patient and queue data handling

## License

This project does not currently declare an explicit license in the repository metadata.

## Contributing

Contributions are welcome. When working on this repository:
- keep frontend and backend APIs aligned
- validate queue and transfer logic carefully
- test medical record workflows before deployment
- document significant changes in the relevant project files
