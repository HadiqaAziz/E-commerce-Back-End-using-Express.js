# E-commerce Back-End using Express.js

Welcome to the E-commerce Back-End! This project provides the back-end functionality for an e-commerce website, allowing you to manage products, categories, and tags through a MySQL database with Express.js. Below is a step-by-step guide on how to use and run the app.

## Table of Contents
- [User Story](#user-story)
- [Acceptance Criteria](#acceptance-criteria)
- [Installation](#installation)
- [Setting Up the Database](#setting-up-the-database)
- [Starting the Application](#starting-the-application)
- [API Routes](#api-routes)
- [CRUD Operations](#crud-operations)

## User Story

As a manager at an internet retail company, you want a back-end system for your e-commerce website that uses the latest technologies to ensure your company can compete in the digital marketplace. This back-end setup allows for easy management of products, categories, and tags via a MySQL database.

## Acceptance Criteria

- **Database Connection**: 
  - The application uses Sequelize to connect to a MySQL database. After adding your database name, MySQL username, and password to an `.env` file, the connection to the database is established.
  
- **Database Setup**:
  - A functional database is created and seeded with test data when the schema and seed commands are run.

- **Starting the Application**:
  - The server starts when the appropriate command is executed, and the Sequelize models are synced to the MySQL database.

- **API Routes**:
  - The API GET routes for categories, products, and tags return data in a formatted JSON when tested in tools like Insomnia Core.

- **CRUD Operations**:
  - POST, PUT, and DELETE routes for products, categories, and tags allow successful creation, updating, and deletion of data in the database when tested in Insomnia Core.

## Installation

Follow these steps to install and set up the project locally.

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/e-commerce-back-end-using-express.js.git
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd e-commerce-back-end-using-express.js
   ```

3. **Install Dependencies**:
   Install the necessary npm packages:
   ```bash
   npm install
   ```

4. **Set Up Environment Variables**:
   Create a `.env` file in the root of your project and add your MySQL database name, MySQL username, and password:
   ```env
   DB_NAME='your-database-name'
   DB_USER='your-mysql-username'
   DB_PASSWORD='your-mysql-password'
   ```

## Setting Up the Database

1. **Create the Database**:
   Log into your MySQL shell and run the following commands to create your database:
   ```sql
   SOURCE db/schema.sql;
   ```

2. **Seed the Database**:
   After setting up the schema, seed the database with test data:
   ```bash
   npm run seed
   ```

## Starting the Application

To start the application and sync Sequelize models to the database, run the following command:
```bash
npm start
```

Your server should now be running on `http://localhost:3001`.

## API Routes

You can test the following API routes in tools like Insomnia Core:

- **Categories**:
  - GET: `/api/categories`
  - POST: `/api/categories`
  - PUT: `/api/categories/:id`
  - DELETE: `/api/categories/:id`

- **Products**:
  - GET: `/api/products`
  - POST: `/api/products`
  - PUT: `/api/products/:id`
  - DELETE: `/api/products/:id`

- **Tags**:
  - GET: `/api/tags`
  - POST: `/api/tags`
  - PUT: `/api/tags/:id`
  - DELETE: `/api/tags/:id`

## CRUD Operations

You can perform the following operations via the API routes in Insomnia Core:

- **Create** new categories, products, or tags using the POST routes.
- **Update** existing data using the PUT routes.
- **Delete** categories, products, or tags using the DELETE routes.

The application will return formatted JSON data for GET requests and respond appropriately to POST, PUT, and DELETE requests.

Now you're ready to manage your e-commerce database efficiently using this back-end system!
