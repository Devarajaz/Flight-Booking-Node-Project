
`src` -> inside the src folder all the actual source code regarding the project will reside, this will not include any kind of tests. (you might want to make separate tests folder)

Lets take a look inside the `src` folder

 - `config` -> In this folder anything and everything regarding any configurations setup of a library or module will be done. For example: setting up `dotenv` so that we can use the environment variable anywhere in a cleaner fashion, this is done in the `server-config.js`. one more example can be to setup you logging library that can help you to prepare meaningful logs, so configuration for this library should also be done here.

 - `routes` -> In the routes folder, we register a route and the corresponding middleware and controllers to it.

 - `middleware` -> They are just going to intercept the incoming request where we can write our validators, authenticators etc.

 - `controllers` -> They are kind of the last middleware as post them you call you business layer to execute the business logic. In controllers we just receive the incoming request and date and then pass it to the business layer, and once business layer returns an output, we structure the API response in controllers and send the output.

 - `Repositories` -> This folder contains all the logic using which we interact the DB by writing queries, all the raw queries or ORM quaries will go here.

 - `services` -> contains the business logic and interacts with respositories for data from the database.

 - `utils` -> contains helper methods, error classes etc.

### Setup the project

 - Download this template from github and open it in your favourite tesxt editor. 
 - Go inside the folder path and execute the following command.
 - In the root directory create a `-env` file and add the following anv variables.
 ```
    PORT =<port number of your choice>
 ```
 ex: 
```
    PORT = 3000
``` 
 - Go inside the `src` folder and execute the following command: 
 ``` 
    npx sequelize init 
 ```
 - By executing the above command you will get migration and seeders folder along with a config.json inside the config folder.

 - If you are setting up your development environment, then write the username of your DB, password of your DB and in dialect mention whatever db you are using for ex: mysql, mariadb, etc

 - If you are setting up test or prod environment, make sure you also replace the host with the hosted db url.

 - To run the server execute 
 ``` 
 npm run dev
 ```

 
