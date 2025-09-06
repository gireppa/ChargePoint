# Project Setup Guide

##  Prerequisites
- Java 24 installed  
- Maven 3.9.11 installed  
- Docker & Docker Compose installed and running(refer [docker-compose.yml](docker-compose.yml) in project)  

---

##  Steps to Run the Project

### 1. Unzip the Project Folder
```bash
unzip your-project.zip
cd your-project
```

---

### 2. Check the Project Structure
Ensure that `pom.xml` is present at the root of the project folder.

---

### 3. Clean and Build the Project
```bash
mvn clean install
```

---

### 4. Start Required Docker Services
```bash
docker compose up -d
```

---

### 5. Start the Spring Boot Server
```bash
mvn spring-boot:run
```

---

### 6. Test with Postman
- URL: http://localhost:8088/authenticate  
- Method: POST  
- Headers: 
  - Content-Type: application/json  

- Body:
json
{
  "stationUuid": "25aac66b-6051-478a-95e2-6d3aa343b025",
  "driverIdentifier": {
    "id": "id1234"
  }
}


project should now be up and running!
