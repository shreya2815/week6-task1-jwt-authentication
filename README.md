# Week 6 Task 1: JWT User Authentication

## Description
A REST API built with Node.js and Express.js that provides user registration, login, password hashing, and JWT-based authentication.

## Technologies Used
- Node.js
- Express.js
- bcryptjs
- jsonwebtoken
- dotenv

## Features
- User registration
- Password hashing using bcrypt
- User login
- JWT token generation
- JWT token verification
- Protected profile route
- Error handling and input validation

## API Endpoints

### 1. Register User
POST /api/auth/register

Example request:
{
  "username": "testuser",
  "email": "test@example.com",
  "password": "Password123!"
}

### 2. Login User
POST /api/auth/login

Example request:
{
  "email": "test@example.com",
  "password": "Password123!"
}

Returns a JWT token after successful login.

### 3. Protected Profile
GET /api/auth/profile

Requires the header:
Authorization: Bearer <your_token>

## Setup Instructions

1. Install Node.js.
2. Clone or download this repository.
3. Install dependencies using npm install.
4. Create a .env file with JWT_SECRET and PORT.
5. Start the server using npm start.
6. Open http://localhost:3000.

## Environment Variables

JWT_SECRET=your_secret_key
PORT=3000

## Testing
Registration, login, and the protected profile endpoint were tested successfully.

## Note
This beginner project stores registered users in memory. User data is cleared when the server restarts. A database can be added for persistent storage.