# MERN E-Commerce

A full-stack e-commerce web application built using the MERN stack (MongoDB, Express.js, React, Node.js). This project provides a comprehensive foundation for building scalable online stores.

## Features

- **Authentication & Authorization**: Secure user registration and login using JWT (JSON Web Tokens), Passport.js with Local, Google OAuth, and Facebook login strategies.
- **Product Management**: Ability to manage products, categories, and inventory.
- **Shopping Cart**: Fully functional shopping cart system with Redux state management.
- **Payment Integration**: Support for payment gateways (e.g., Stripe, PayPal integration ready).
- **Admin Dashboard**: Role-based access control for managing users, products, and orders.
- **Real-time Notifications**: Socket.io integration for instant updates and notifications.
- **Mailing**: Integration with Mailgun and Mailchimp for email services and newsletters.

## Technologies Used

*   **Frontend:**
    *   React.js
    *   Redux & Redux-Thunk (State Management)
    *   React Router (Routing)
    *   Bootstrap & Reactstrap (UI Framework)
    *   SASS (Styling)
    *   Webpack (Module Bundler)
*   **Backend:**
    *   Node.js
    *   Express.js
    *   MongoDB (NoSQL Database) & Mongoose (ODM)
    *   Passport.js (Authentication)
    *   Socket.io (WebSockets)
    *   AWS SDK

## Prerequisites

Before running the project, make sure you have the following installed on your machine:

*   [Node.js](https://nodejs.org/) (v14 or later recommended)
*   [npm](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)
*   [MongoDB](https://www.mongodb.com/) (running locally or a cloud instance like MongoDB Atlas)

## Getting Started

Follow these steps to set up the project locally:


### 2. Install dependencies

From the root directory, you can install both client and server dependencies using:

```bash
npm run postinstall
```
Alternatively, you can manually install them:
```bash
npm run install:client
npm run install:server
```

### 3. Environment Variables

Create a `.env` file in the `server` directory and add the necessary environment variables. Example variables you might need:

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
MAILGUN_KEY=your_mailgun_api_key
MAILGUN_DOMAIN=your_mailgun_domain
MAILCHIMP_KEY=your_mailchimp_api_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
FACEBOOK_CLIENT_ID=your_facebook_client_id
FACEBOOK_CLIENT_SECRET=your_facebook_client_secret
```

Create a `.env` file in the `client` directory (if required by your configuration, typically handled by dotenv-webpack).

### 4. Seed the Database (Optional)

You can generate sample data to test the application:

```bash
cd server
npm run seed:db
```

### 5. Run the Application

To run both the server and the client concurrently in development mode:

```bash
# from the root directory
npm run dev
```

*   **Client** will run on: `http://localhost:8080` (or as configured in webpack)
*   **Server** will run on: `http://localhost:3000`

## Scripts Overview

*   `npm run dev`: Starts both frontend and backend concurrently.
*   `npm run dev:client`: Starts only the frontend development server.
*   `npm run dev:server`: Starts only the backend server using nodemon.
*   `npm run install:client`: Installs frontend dependencies.
*   `npm run install:server`: Installs backend dependencies.
*   `npm run postinstall`: Installs both client and server dependencies simultaneously.
