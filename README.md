[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/3veDIsfC)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=22105326&assignment_repo_type=AssignmentRepo)
# FastAPI Backend Project

This is a FastAPI backend project.

## Prerequisites

- Python 3.10+
- pip
- virtualenv (optional but recommended)

## Setup Instructions

### 1. Clone the repository


git clone <your-repo-url>
cd backend
### 2. Create a virtual environment
python -m venv venv
Activate the virtual environment:
macOS/Linux:
source venv/bin/activate
Windows (Command Prompt):
venv\Scripts\activate
Windows (PowerShell):
.\venv\Scripts\Activate.ps1
### 3. Install dependencies
pip install -r requirements.txt
### 4. Configure environment variables
cp .env.example .env
Open .env and set your SQL database URL:
DATABASE_URL=postgresql://username:password@localhost:5432/dbname
Replace username, password, localhost, 5432, and dbname with your database credentials.
### 5. Run database migrations
alembic upgrade head
### 6. Start the FastAPI server
uvicorn app.main:app --reload
You should see output like:
INFO:     Will watch for changes in these directories: [...]
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [...]
Open your browser and navigate to http://127.0.0.1:8000 to see your API running.
### 7. Optional: Access API docs
Swagger UI: http://127.0.0.1:8000/docs
ReDoc: http://127.0.0.1:8000/redoc
