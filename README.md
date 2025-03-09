# tdms-microservices-Eurekha_Discovery-
This repo is created for microservice architecture.

# 🚀 Eureka Discovery Service - Tiffin Delivery & Management System

This repository contains the **Eureka Discovery Service** implementation for the **Tiffin Delivery and Management System (TDMS)**. The Eureka Server acts as a **Service Registry**, enabling dynamic service discovery for microservices such as **Payment Service**.

---

## 📌 **Features of Eureka Discovery Service**
✅ **Service Registration & Discovery** - Microservices register themselves and can discover each other dynamically.  
✅ **Microservices Communication** - Allows seamless inter-service communication without hardcoded URLs.  
✅ **Spring Boot & Netflix Eureka Integration** - Built using **Spring Boot & Spring Cloud Netflix Eureka**.

---

🔹 What is Eureka Discovery Service?
Netflix Eureka is a service registry for microservices that helps in dynamic service discovery. It allows different microservices to register themselves and communicate without hardcoded URLs.

🚀 Why We Use Eureka in TDMS?
In the Tiffin Delivery and Management System (TDMS), multiple microservices handle different functionalities (e.g., Payment Service, Order Service, Vendor Service).
Instead of manually configuring service URLs, we use Eureka for dynamic service discovery.
Payment Service registers itself with Eureka, making it easily accessible to other microservices like Order Service and Customer Service.
This enhances scalability, failover handling, and load balancing.

How Eureka is Integrated with Payment Service?
1️⃣ Eureka Server (Service Registry)
The Eureka Server is a standalone microservice that maintains a registry of all active services.
It runs on port 8761 and allows services to register dynamically.
Other services query Eureka to get the latest addresses of microservices.

2️⃣ Payment Service Registration with Eureka
The Payment Service registers itself with Eureka so that other microservices (like Order Service) can discover it dynamically.
So,any other service can dynamically discover Payment Service by its name instead of hardcoding URLs.

3️⃣ How Other Services Communicate with Payment Service?
Instead of using a fixed URL (http://localhost:8082), other microservices use the service name payment-service for communication.

Benefits of Eureka in TDMS
✅ No Hardcoded Service URLs → Improves flexibility & scalability
✅ Automatic Load Balancing → Works with Ribbon & Spring Cloud LoadBalancer
✅ High Availability & Failover Handling → If one instance fails, another is used
✅ Dynamic Scaling → Add or remove services without reconfiguring other services

