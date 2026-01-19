# MongoDB Change Streams Todo App

A simple ASP.NET Core 8.0 web application that demonstrates MongoDB change streams functionality with a Todo API.

## Prerequisites

- .NET 8.0 SDK or later
- MongoDB Atlas account or MongoDB instance
- Valid MongoDB connection string

## Setup

1. **Clone the repository:**

   ```bash
   git clone <repository-url>
   cd mongo-change-streams-dotnet
   ```

2. **Configure MongoDB Connection:**
   Update the MongoDB connection string in `TodoApp/appsettings.json`:
   ```json
   {
     "DataBaseConnection": {
       "ConnectionString": "mongodb+srv://user:password@your-cluster.mongodb.net/?retryWrites=true&w=majority",
       "DatabaseName": "TodoApp",
       "CollectionName": "TodoItems"
     }
   }
   ```

## Running the Application

1. **Restore dependencies:**

   ```bash
   dotnet restore
   ```

2. **Run the application:**

   ```bash
   dotnet run
   ```

3. **Access the API:**
   - Open browser: `https://localhost:5001`
   - Swagger UI: `https://localhost:5001/swagger`

## Features

- RESTful API for Todo CRUD operations
- MongoDB integration with change streams
- Swagger/OpenAPI documentation
- Background service for monitoring database changes
- Built with ASP.NET Core 8.0

## Project Structure

```
TodoApp/
├── Controllers/      # API endpoints
├── Services/         # Business logic
├── Repositories/     # Data access layer
├── Domain/          # Entity models
├── Configurations/  # Configuration classes
├── Background/      # Background services (change streams)
└── Properties/      # Application settings
```

## Technologies

- ASP.NET Core 8.0
- MongoDB.Driver 2.28.0
- Swagger/Swashbuckle 6.4.0
- Newtonsoft.Json 13.0.3
