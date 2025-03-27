# **🌓 Voting App - Docker Swarm Deployment**

## **📌 Overview**  
This repository contains a **Python & Node.js-based Voting Application**, designed to demonstrate how to deploy and orchestrate a multi-service application using **Docker Swarm**.  

## **🏢 Architecture**  
The application consists of multiple services working together:  

### **1️⃣ Voting App (`voting_app`)**  
- Developed in **Python (Flask)**.  
- Allows users to **cast their votes**.  
- Deployed with **2 replicas** for **load balancing** and **high availability**.  

### **2️⃣ Redis Database (`my-redis`)**  
- Stores **voting data** temporarily before processing.  
- Provides quick retrieval and efficient vote management.  

### **3️⃣ Worker Application (`worker`)**  
- Built using **.NET**.  
- Retrieves votes from **Redis**, processes them, and stores the results in **PostgreSQL**.  

### **4️⃣ PostgreSQL Database (`my-postgres`)**  
- Stores the **processed voting results** permanently.  

### **5️⃣ Result Display App (`result-app`)**  
- Retrieves the **final voting results** from **Postgres**.  
- Displays **real-time voting results** to users.  

---

## **🚀 Deployment using Docker Swarm**  

### **1️⃣ Initialize Docker Swarm**  
```sh
docker swarm init
```

### **2️⃣ Deploy the Application Stack**  
Run the following command to deploy the application:  
```sh
docker stack deploy -c docker-compose.yml voting_app
```

### **3️⃣ Verify Running Services**  
Check if all services are running correctly:  
```sh
docker service ls
```

### **4️⃣ Access the Application**  
- **Voting App:** `http://<swarm-manager-ip>:5000`  
- **Result Display:** `http://<swarm-manager-ip>:5001`  

---

## **⚙️ Technologies Used**  
- **Backend:** Python (Flask), Node.js  
- **Database:** Redis, PostgreSQL  
- **Orchestration:** Docker Swarm  
- **Worker Service:** .NET  
- **Frontend:** HTML/CSS for voting and results display  

---

## **📜 License**  
This project is for **learning and demonstration purposes**.  

