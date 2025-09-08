🧩 Microservices Quiz App

This is a microservices-based quiz application designed with a service-oriented architecture, where different functionalities are handled by separate, independent services.
This approach allows for scalability, flexibility, and easier maintenance.

⚡ Architecture Overview

The application is composed of several independent services that communicate with each other.

Core Services

Question Service → Manages all quiz questions (create, retrieve, organize).

Quiz Service → Orchestrates the quiz flow, assembles questions, and calculates scores.

API Gateway (Implicit) → Routes client requests to the right backend service.

📌 Core Services & Responsibilities
📝 Question Service

Handles all question-related logic.

Endpoints:

POST /question/add → Add a new question

GET /question/allQuestions → Retrieve all questions

GET /question/category/{category} → Fetch questions by category

🎯 Quiz Service

Handles the overall quiz flow, relying on the Question Service for data.

Endpoints:

POST /quiz/create → Create a new quiz from available questions

GET /quiz/get/{id} → Retrieve a quiz by its ID

POST /quiz/submit/{id} → Submit answers and return the final score

🛠️ Technologies

Spring Boot → For building each microservice

PostgreSQL → For Database

REST APIs → For inter-service communication

🚀 Getting Started
✅ Prerequisites

Java Development Kit (JDK 17 or higher)

Maven 3.6.3 or higher

⚙️ Setup

Clone the repository:

git clone <repository_url>
cd microservice-quiz-app


Build each service:
Navigate into each service directory (e.g., question-service, quiz-service) and run:

mvn clean install


Run the services:
Start the main application class for each service:

mvn spring-boot:run

📜 License

This project is licensed under the MIT License – see the LICENSE
 file for details.
