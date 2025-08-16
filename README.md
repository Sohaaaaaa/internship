# Project 
khadeeja soha khan - 160923733063

Task Manager (Spring Boot)
A simple REST API for managing tasks with fields like title, description, deadline, priority, and status.

📋 Requirements
Java 17+ (Project is set to Java 22 in pom.xml)
Maven 3.9+
Internet connection (for Maven dependency download)
Optional: Postman or curl for API testing
📂 Project Structure
TaskManager/ │── pom.xml └── src/ └── main/ └── java/ └── com/example/taskmanager/ ├── controller/TaskController.java ├── model/Task.java └── service/TaskService.java

🚀 How to Run
Clone the project
git clone https://github.com/your-repo/TaskManager.git
cd TaskManager
Build the project
mvn clean install

Run the application
mvn spring-boot:run

OR run TaskManagerApplication.java from your IDE.

Verify server is running
http://localhost:8080

📌 API Endpoints

Create Task

POST /tasks

{ "title": "Learn Spring", "description": "Build REST API", "deadline": "2025-08-20", "priority": "High", "status": "Pending" }

Get All Tasks

GET /tasks

Get Task by ID

GET /tasks/{id}

Update Task

PUT /tasks/{id}

{ "title": "Learn Spring Boot", "description": "REST + Swagger", "deadline": "2025-08-25", "priority": "Medium", "status": "Completed" }

Delete Task

DELETE /tasks/{id}

🛠 Test with cURL

Create
curl -X POST http://localhost:8080/tasks
-H "Content-Type: application/json"
-d '{"title":"Learn Spring","description":"Build REST API","deadline":"2025-08-20","priority":"High","status":"Pending"}'

Get all
curl http://localhost:8080/tasks

Get by ID
curl http://localhost:8080/tasks/1

Update
curl -X PUT http://localhost:8080/tasks/1
-H "Content-Type: application/json"
-d '{"title":"Learn Spring Boot","description":"REST + Swagger","deadline":"2025-08-25","priority":"Medium","status":"Completed"}'

Delete
curl -X DELETE http://localhost:8080/tasks/1
