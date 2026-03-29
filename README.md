# Node.js MongoDB App

Esta aplicación Node.js se conecta a una base de datos MongoDB y expone una API REST con los siguientes endpoints:

- **GET /items**: Consulta todos los registros de la colección.
- **POST /items**: Agrega un nuevo registro (campos: name, state).
- **DELETE /items/:id**: Borra un registro por su ID.

## Estructura de la colección
- **name**: String
- **state**: String

## Uso
1. Instala las dependencias: `npm install`
2. Configura la cadena de conexión de MongoDB en el archivo `.env`.
3. Inicia el servidor: `npm start`

## Requisitos
- Node.js
- MongoDB
