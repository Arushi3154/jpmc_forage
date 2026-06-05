# jpmc_forage
# JPMorgan Chase & Co. — Midas Backend Engineering Pipeline

## 📌 Project Overview
This repository contains my implementation of the **Midas-Core** processing system completed as part of the JPMorgan Chase Advanced Software Engineering Virtual Experience on Forage. The project simulates an enterprise-level, high-volume transactional backend infrastructure designed to consume, process, validate, and persist high-velocity financial records accurately.

## 🛠️ Architecture & Tech Stack
* **Core Framework:** Java 17, Spring Boot 3.x
* **Event Streaming & Messaging:** Apache Kafka
* **Database & Persistence:** H2 In-Memory Relational Database, Spring Data JPA
* **Build Tool:** Maven
* **Configuration Syntax:** YAML (`application.yml`)

---

## 📊 Core Engineering Tasks & Implementations

### 🔹 Task 1: Enterprise Project Scaffolding
* **Objective:** Establish the development sandbox, verify dependency tracking, and decode the underlying codebase architecture.
* **Implementation:** Configured a local enterprise workspace running Java 17 and Spring Boot. Engineered build specifications in Maven to verify smooth serialization properties across data modules.

### 🔹 Task 2: Kafka Event-Driven Ingestion System
* **Objective:** Decouple transaction streaming layers from core database processing using asynchronous message brokers.
* **Implementation:** * Configured `application.yml` bindings for Kafka components to map transaction serialization profiles.
  * Engineered a specialized `TransactionListener` component decorated with `@KafkaListener` to autonomously consume stream messages from dedicated Kafka topics.
  * Handled JSON payload deserialization to bind stream payloads dynamically into concrete `Transaction` foundation structures.

### 🔹 Task 3: Relational Persistence Layer (In Progress / Completed)
* **Objective:** Implement data persistence and transactional integrity checks.
* **Implementation:** Configured Spring Data JPA repositories mapped to standard relational database schemas within an in-memory H2 DB environment. Created backend service wrappers that save verified, incoming data stream components without blocking performance.

---

## 🏗️ System Architecture & Data Flow
The system acts as a classic decoupled processing channel:
1. **Producer Side:** Mock transaction feeds emit real-time string data into the Kafka engine (`transactions` topic).
2. **Broker Management:** Kafka acts as the independent, distributed buffer—decoupling heavy transmission logic from the listener thread.
3. **Consumer Layer:** The custom Spring Boot `TransactionListener` catches the raw bytes, triggers internal JSON parsing mechanisms, maps it to a relational entity schema, and securely commits it to the H2 database repository layer.

---

## 🚀 How To Build & Run Locally

### Prerequisites
* Java 17 or higher
* Apache Kafka (running locally or via Docker container configurations)
* Maven installed

### Steps to Execute
1. Clone your personal workspace repository:
   ```bash
   git clone [https://github.com/Arushi3154/YOUR_REPO_NAME.git](https://github.com/Arushi3154/YOUR_REPO_NAME.git)
   cd YOUR_REPO_NAME
