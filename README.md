# AirLine-Project
this is the base node js project template , which any one can use as it has been 
prepared , by keeping some of the most important code principles and project
management and recomendations . feel free to chnage any thing

'src' ->Inside the src  all the actual sopurce code  regarding the project will
reside. this will not include any kind of test. ( you might want to make separate test folder)

Lets take a look inside the 'src' folder
 'config'-> In this folder anything and everything regarding any configurations o: setup of a Library or module will be done. For example: setting up dotenv so that we can use the environment variables anywhere in a cleaner fashion, this is done in the server-config.js. One more example can be to setup you logging library that can help you to prepare meaningful logs, so configuration for this library should also be done here.

 'routes' ->In the routes folder, we register a route and the corresponding middleware and controllers to it. middlewares they are just going to intercept the incoming requests where we can write our validators, authenticators etc.

  'controllers'-> they are kind of the last middlewares as post them you call you business layer to execute the budiness logic. In controllers we just receive the incoming requests and data and then pass it to the business Layer, and once business Layer returns an output, we structure the API response in controllers and send the output.


  "repositories" ->this folder contains all the logic using which we interact the DB by writing queries, all the raw queries or ORM queries will go here.

   "services" ->contains the buiness logic and interacts with repositories for data from the database 

  "utils" -> contains helper methods, error classes etc.


  ### Setup the project Download this template from github and open it in your favourite text editor.
   Go inside the folder path and execute the following command: 
  ''' npm install'''
  - in the root directory create a '.env' file and add the following env variable 

  - go inside the 'src' folder  and execute the following commmands
''' npx sequelize init'''



- By exexcuting the above command  you will get  the migrations and seeders folders  along with the config.json file inside the config folder

if you are seting up your development environment, then write user name of your db, password of your db and in dialect
whatever db you are using for ex;
mysql,posgres,  mariadb etc.
if you are setting up test or prod environment , make sure you also replace the host with the  hosted db url


  Inside 'src/config' folder create a file name 'config.json' and write the following code;

  '''
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
'''
- run your server npm start 
