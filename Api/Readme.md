# BlockEstate API

BlockEstate is a backend API for managing users, authentication, and property listings. This project is built using Node.js, Express, and MongoDB.

## Features

- User authentication (signup, signin, Google login, signout)
- CRUD operations for users
- CRUD operations for property listings
- JWT-based authentication
- Error handling middleware

## Prerequisites

Before running the application, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/)
- [npm](https://www.npmjs.com/) (comes with Node.js)

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd BlockEstate/Api
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add the following environment variables:

   ```env
   MONGO=<your-mongodb-connection-string>
   JWT_Secret=<your-jwt-secret>
   ```

4. Install `nodemon` globally (if not already installed):

   ```bash
   npm install -g nodemon
   ```

## Running the Application

To start the application:

1. Run the server with `nodemon` for automatic restarts on file changes:

   ```bash
   nodemon index.js
   ```

2. Alternatively, you can run the server with Node.js:

   ```bash
   node index.js
   ```

The server will run on `http://localhost:3000`.

## API Endpoints

### User Routes (`/api/user`)
- `GET /test` - Test endpoint
- `POST /update/:id` - Update user (requires authentication)
- `DELETE /delete/:id` - Delete user (requires authentication)
- `GET /listings/:id` - Get user listings (requires authentication)

### Auth Routes (`/api/auth`)
- `POST /signup` - User signup
- `POST /signin` - User signin
- `POST /google` - Google login
- `GET /signout` - User signout

### Listing Routes (`/api/listing`)
- `POST /create` - Create a listing (requires authentication)
- `DELETE /delete/:id` - Delete a listing (requires authentication)

## Project Structure

```
BlockEstate/Api
├── Models
│   ├── listing.model.js
│   └── user_model.js
├── Routes
│   ├── auth.route.js
│   ├── listing.route.js
│   └── user.route.js
├── controllers
│   ├── auth.controller.js
│   ├── listing.controller.js
│   └── user.controller.js
├── utils
│   ├── error.js
│   └── verifyUser.js
├── index.js
└── .env
```
