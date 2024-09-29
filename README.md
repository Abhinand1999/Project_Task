# To-Do Management
This application allows you to manage multiple todo projects, add and update todos, mark them as complete, and export project summaries as GitHub gists.

## Table of Contents
- [Features](Features)
- [Technologies](Technologies)
- [Prerequisites](Prerequisites)
- [Setup](Setup)
- [Running the Application](RunningtheApplication)
- [API Endpoints](APIEndpoints)
- [Exporting Project Summary to GitHub Gist](ExportingProjectSummarytoGitHubGist)
- [License](License)


## Features
1.Create a new project: Organize tasks into projects.
2.Manage todos within a project:
  * Add new todos.
  * Edit and update existing todos.
  * Mark todos as complete.
3.Export project summary: Export the project summary as a GitHub gist.


## Technologies
Frontend: React.js
Backend: Node.js, Express.js
Database: [MongoDB]
External API: GitHub Gist API

## Prerequisites
Node.js (v16 or above)
npm or yarn
A GitHub account for exporting project summaries as gists

# Setup
Backend (Node.js + Express)
1.Clone the repository:
git clone <repository-url>
cd <repository-folder>
2.Navigate to the backend directory:
cd backend
3.Install backend dependencies:
npm install
4.Create a .env file in the backend directory and add the following environment variables:
PORT=5000
MONGO_URL="mongodb://localhost:27017/todo-management"
JWT="your_secret_key"

5.Run the backend server:
npm start

## Testing
### Backend Testing (Node.js with Jest and Supertest)
We use Jest for unit tests and Supertest for testing API endpoints.

To run tests for the backend, navigate to the backend folder and run:

cd backend
npm test

## Frontend (React.js)
1.Navigate to the frontend directory:
cd ../frontend
2.Install frontend dependencies:
npm install
Update the API endpoint in your React project (config file) to point to the backend:
Base_URL="http://localhost:5000/api/v1"
npm start

## Running the Application
Start the backend server (npm start).
Start the frontend server (npm start).
Open your browser and navigate to http://localhost:3000 to view the application.

## API Endpoints

## Project Endpoints:

get /:id : Fetch selected projects.
get / : Fetch all projects.
post / : Create a new project.
put /:id : Update a project.


## Todo Endpoints:

post /:id : Add a new todo
patch /:id  :Mark a todo as complete
get /:id ,verifyToken,GetAllTodo) :Get todos within a project
delete /:id ,verifyToken,deleteTodo) : Delete a todo
patch /update/:id ,verifyToken,DiscriotionUpadte) :Update a todo 


## GitHub Gist Endpoints:

post id : Export project summary as a GitHub gist


Exporting Project Summary to GitHub Gist
To export a project summary to GitHub Gist, you need to:

## Ensure you have a valid GitHub access token in your .env file.
Make a POST request to post id :.
The API will create a gist with the project’s details (e.g., todos and status) on your GitHub account.


