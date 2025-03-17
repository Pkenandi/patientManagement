# Patient Management

## Overview
Patient Management is a microservices-based system designed to handle patient records, billing, analytics, notifications, and authentication. The system follows a modular architecture, utilizing Docker networking, gRPC communication, and Kafka for event-driven messaging.

## Architecture
The system consists of multiple microservices communicating through gRPC and Kafka. Each service is containerized and interacts via a Docker network.

## Modules

### Patient Service
The **Patient Service** is responsible for managing patient records, storing essential information, and handling interactions related to patient data. It acts as a Kafka producer to publish patient-related events.

### Billing Service
The **Billing Service** handles patient billing operations, invoice generation, and payment tracking. It communicates with the Patient Service via gRPC and processes billing requests.

### Analytics Service
The **Analytics Service** consumes patient-related events from Kafka and processes them for insights. It is responsible for generating reports and statistical data on patient trends.

### Notification Service
The **Notification Service** listens to patient events from Kafka and sends notifications to users (e.g., appointment reminders, billing alerts, etc.).

### Auth Service
The **Auth Service** manages user authentication and authorization, ensuring secure access to system resources. It integrates with the API Gateway for centralized authentication.

## Technology Stack
- **Microservices Architecture**: Each module is designed as an independent service.
- **Docker**: Used for containerization and deployment.
- **gRPC**: Communication between Patient Service and Billing Service.
- **Kafka**: Event-driven communication between services (Producer-Consumer pattern).
- **API Gateway**: Routes requests to respective microservices.
- **Frontend**: Client interface to interact with the system.

## Setup & Deployment
```sh
# Clone the repository
git clone https://github.com/your-repo/patient-management.git

# Navigate to the project directory
cd patient-management

# Start the Docker containers
docker-compose up -d

# Access the services via the API Gateway
```

## Contributing
Feel free to submit issues and pull requests. Contributions are welcome!

## License
This project is licensed under the MIT License.

