# Course Project: ASP.NET Core APIs for Stock Management

## Overview

This is a course project focused on building a RESTful API using ASP.NET Core. The API provides functionality for managing stocks and associated comments. It includes essential CRUD operations such as adding stocks, editing stocks, and adding comments. Additionally, the API offers authentication features using JSON Web Tokens (JWT) to secure endpoints.

## Features

- **Stock Management:**
  - Add new stocks
  - Edit existing stocks
  - View all available stocks

- **Commenting System:**
  - Add comments to stocks
  - View comments related to stocks

- **Authentication:**
  - User authentication using JWT (JSON Web Token) for secure access to certain endpoints
  - Token-based authentication to ensure secure communication between clients and the API

## API Endpoints

- `POST /api/stocks` – Add a new stock
- `PUT /api/stocks/{id}` – Edit an existing stock
- `GET /api/stocks` – Retrieve all stocks
- `GET /api/stocks/{id}` – Retrieve a specific stock by ID
- `POST /api/stocks/{id}/comments` – Add a comment to a specific stock
- `GET /api/stocks/{id}/comments` – Retrieve all comments for a specific stock

### Authentication Endpoints:

- `POST /api/auth/login` – Login and receive a JWT token
- `POST /api/auth/register` – Register a new user

## Authentication

This API uses JWT tokens for user authentication. To access certain endpoints (such as adding or editing stocks), a valid token must be included in the request headers.

### Example of Token Authentication:

1. **Login:**
   - POST to `/api/auth/login` with credentials (username and password).
   - Receive JWT token upon successful login.
   
2. **Accessing Protected Endpoints:**
   - Include the JWT token in the Authorization header:  
     `Authorization: Bearer <your-jwt-token>`

## Next Steps

- **Unit Testing:**
  - Implement unit testing using XUnit to ensure the stability and reliability of the API endpoints.
  
- **Frontend Development:**
  - Implement a frontend to interact with the API. The frontend will allow users to easily manage stocks, add comments, and view stock data in a user-friendly interface.

## Technologies Used

- **Backend:** ASP.NET Core
- **Authentication:** JWT (JSON Web Tokens)
- **Testing:** XUnit (upcoming implementation)
- **Frontend (upcoming):** To be implemented
