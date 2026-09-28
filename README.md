<img width="1536" height="1024" alt="project-node-mongo" src="https://github.com/user-attachments/assets/2d7fa6c3-6eb4-440f-bbc0-33e832cda646" />

# App Node.js connection with MongoDB

This Node.js application connects to a MongoDB database and exposes a REST API with the following endpoints:

- **GET /items**: Retrieves all records in the collection.
- **POST /items**: Adds a new record (fields: name, state).
- **DELETE /items/:id**: Deletes a record by its ID.

## Collection Structure
- **name**: String
- **state**: String

## 🛠️ Technologies

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

## Step-by-Step Execution Guide
This project can be run using either Docker Compose (recommended for quick development and deployment) or by running Node.js and MongoDB individually.

## OPTION 1: Quick Start with Docker Compose (Recommended)
This option automatically spins up the MongoDB database and the Node.js API service inside isolated containers.

## Prerequisites
Docker and Docker Desktop installed on your machine.

## Steps
Clone the repository

```Bash
git clone https://github.com/diegopineda77/docker-mongo-app.git
cd docker-mongo-app
```
Start the services using Docker Compose

```Bash
docker-compose up --build -d
```
The -d flag runs the containers in detached (background) mode.

## Verify the running containers

```Bash
docker ps
```
Test the API
The application will be accessible at http://localhost:3000 (or the port defined in your docker-compose.yml).

Stop the application

```Bash
docker-compose down
```



## OPTION 2: Manual Local Setup
Use this approach if you prefer running the Node.js application directly on your host machine connected to a local or remote MongoDB instance.

## Requirements
- Node.js (v14 or higher)
- MongoDB

## Active MongoDB instance running locally or a MongoDB Atlas connection URI.

## Steps
Clone the repository and enter the directory

```Bash
git clone https://github.com/diegopineda77/docker-mongo-app.git
cd docker-mongo-app
```
Install dependencies

```Bash
npm install
```
Configure environment variables
Create a .env file in the root directory and specify your database connection string:

```Code snippet
PORT=3000
MONGO_URI=mongodb://localhost:27017/your_database_name
```
Start the server

```Bash
npm start
```
Test the Endpoints
You can send HTTP requests using tools like Postman, cURL, or Thunder Client:

GET /items: Fetch all records.

POST /items: Add a new record with a JSON body such as { "name": "Sample", "state": "Active" }.

DELETE /items/:id: Delete a specific record by its ID.

