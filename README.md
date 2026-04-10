# 🌱 Automated Greenhouse Management System (AGMS)

## 📌 Overview

Automated Greenhouse Management System (AGMS) is a cloud-native, microservice-based application designed to monitor and control greenhouse environments using real-time IoT data. The system integrates with an external IoT provider to fetch temperature and humidity readings and automatically triggers actions based on predefined rules.

---

## 🎯 Features

* 🌡️ Real-time temperature & humidity monitoring
* 🤖 Rule-based automation (Fan/Heater control)
* 🏡 Zone management with environmental thresholds
* 🌱 Crop lifecycle tracking (Seedling → Vegetative → Harvested)
* 🔐 Secure API access using JWT authentication
* ⚡ Microservice architecture with service discovery

---

## 🏗️ System Architecture

### 🔹 Infrastructure Services

* **Eureka Server** – Service Discovery
* **API Gateway** – Centralized routing & security
* **Config Server** – Centralized configuration management

### 🔹 Domain Microservices

* **Zone Service (8081)** – Manage greenhouse zones & thresholds
* **Sensor Service (8082)** – Fetch IoT data & push to automation
* **Automation Service (8083)** – Rule engine for decision making
* **Crop Service (8084)** – Manage crop lifecycle

---

## ⚙️ Technologies Used

* **Backend:** Spring Boot, Spring Cloud
* **Security:** JWT Authentication
* **Communication:** OpenFeign / REST APIs
* **Config Management:** Spring Cloud Config
* **Service Discovery:** Netflix Eureka
* **API Testing:** Postman

---

## 🔗 External IoT API

* Base URL: `http://104.211.95.241:8080/api`
* Provides real-time temperature & humidity data
* Requires JWT authentication

---

## 🚀 How to Run the Project

### 1️⃣ Start Infrastructure Services

1. Start **Config Server**
2. Start **Eureka Server**
3. Start **API Gateway**

### 2️⃣ Start Microservices

4. Start **Zone Service**
5. Start **Sensor Service**
6. Start **Automation Service**
7. Start **Crop Service**

---

## 🔄 System Workflow

1. Sensor Service fetches IoT data every 10 seconds
2. Data is sent to Automation Service
3. Automation Service checks zone thresholds
4. Actions are triggered (Fan ON / Heater ON)
5. Logs are stored and displayed

---

## 📬 API Testing

* Import the **Postman Collection (.json)** provided in this repository
* Test all endpoints via API Gateway

---

## 📊 Eureka Dashboard

📷 Screenshot available in `/docs` folder showing all services running (Status: UP)

---

## 📁 Project Structure

```
AGMS/
 ├── config-server/
 ├── eureka-server/
 ├── api-gateway/
 ├── zone-service/
 ├── sensor-service/
 ├── automation-service/
 ├── crop-service/
 └── docs/
```

---

## 👨‍💻 Author

**Janith Umayanga**
Software Engineering Undergraduate

---

## 📜 License

This project is developed for academic purposes.
