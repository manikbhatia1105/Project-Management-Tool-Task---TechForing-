# Project-Management-Tool-Task---TechForing-


This is a Django-based backend project for managing users, projects, tasks, and comments in a project management tool. The API supports CRUD operations and authentication using JWT.

---

## Features
- User Registration and Authentication
- Project Management
- Task Management with Priorities and Status
- Commenting System
- Role-based Project Membership

---

## Setup Instructions

### Prerequisites
- Python 3.8+
- pip
- Virtual environment (optional, but recommended)

### Steps

1. **Clone the Repository**
   ```bash
   git clone <your-repository-url>
   cd CompleteProjectManagementTool
   ```

2. **Set Up a Virtual Environment**
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Apply Migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Run the Development Server**
   ```bash
   python manage.py runserver
   ```

The server will start at `http://127.0.0.1:8000`.

---

## API Endpoints

### Users
- `POST /api/users/register/` - Register a new user
- `POST /api/users/login/` - Authenticate and obtain a token
- `GET /api/users/{id}/` - Retrieve user details
- `PUT /api/users/{id}/` - Update user details
- `DELETE /api/users/{id}/` - Delete a user

### Projects
- `GET /api/projects/` - List all projects
- `POST /api/projects/` - Create a new project
- `GET /api/projects/{id}/` - Retrieve a specific project
- `PUT /api/projects/{id}/` - Update a project
- `DELETE /api/projects/{id}/` - Delete a project

### Tasks
- `GET /api/projects/{project_id}/tasks/` - List all tasks for a project
- `POST /api/projects/{project_id}/tasks/` - Create a task
- `GET /api/tasks/{id}/` - Retrieve task details
- `PUT /api/tasks/{id}/` - Update task details
- `DELETE /api/tasks/{id}/` - Delete a task

### Comments
- `GET /api/tasks/{task_id}/comments/` - List all comments for a task
- `POST /api/tasks/{task_id}/comments/` - Add a comment to a task
- `GET /api/comments/{id}/` - Retrieve a specific comment
- `PUT /api/comments/{id}/` - Update a comment
- `DELETE /api/comments/{id}/` - Delete a comment

---

## API Documentation
- API documentation is available via Swagger or Postman collection. To access Swagger:
  ```bash
  http://127.0.0.1:8000/swagger/
  ```

---

