

# Airline-Project
This is a base Node.js project template designed with best practices for project management and code structure. Feel free to modify it as needed.irline-Project
This is a base Node.js project template designed with best practices for project management and code structure. Feel free to modify it as needed.

# Project Structure
    src/: Contains all source code.
    config/: Configuration for libraries or modules (e.g., dotenv, logging).
    routes/: Defines API routes and connects them to controllers. Using dotenv in Node.js 
    controllers/: Handles API requests and responses by interacting with the business layer. 
    repositories/: Manages database queries (raw or ORM). NPM start script 
    services/: Contains business logic and interacts with repositories. 
    utils/: Includes helper methods, error classes, etc.


# 1-Setup Instructions
1 - Clone the Repository
Download or clone the project and open it in your preferred text editor.

 # 2- Install Dependencies
Run in the root directory:
  '''npm install'''

# 3-Setup Environment Variables
Create a .env file in the root directory and add required variables.

 # 4- Initialize Sequelize
In the src folder run:  
 '''npx sequelize init'''
 This will create the migrations, seeders, and config/config.json files.

 # 5- Configure Database
Update src/config/config.json with your database details:
{
  "development": {
    "username": "root",
    "password": null,
    "database": "database_development",
    "host": "127.0.0.1",
    "dialect": "mysql"
  },
  "test": {
    "username": "root",
    "password": null,
    "database": "database_test",
    "host": "127.0.0.1",
    "dialect": "mysql"
  },
  "production": {
    "username": "root",
    "password": null,
    "database": "database_production",
    "host": "127.0.0.1",
    "dialect": "mysql"
  }
}

 # 6- Start the Server
         Run:
  '''npm start'''



