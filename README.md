# Node.js MongoDB App

This Node.js application connects to a MongoDB database and exposes a REST API with the following endpoints:

- **GET /items**: Retrieves all records in the collection.
- **POST /items**: Adds a new record (fields: name, state).
- **DELETE /items/:id**: Deletes a record by its ID.

## Collection Structure
- **name**: String
- **state**: String

## Usage
1. Install dependencies: `npm install`
2. Configure the MongoDB connection string in the `.env` file.
3. Start the server: `npm start`

## Requirements
- Node.js
- MongoDB