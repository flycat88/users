
## About Users

This is a simple user management API using default laravel tools. 

To set up;

1. Clone the project to your computer using: ``` git clone https://github.com/flycat88/users.git ```

2. Run ``` composer install ``` to install project dependencies.

3. Copy the __.env.example__ file to a new file called __.env__ and fill in the database credentials.

4. Run the command ``` php artisan migrate ``` to set up the database tables.

5. Run the command ``` php artisan serve ``` to start the server

__Note__: Ensure ``` php ``` and ``` mariadb ``` is installed in your computer for this project to work.


## Example API Requests

### Get Single User

Send a ```GET``` request to the endpoint: ``` http://localhost:3000/api/users/{id} ```, with ```{id}``` being an ID for a user

### Get Users (with pagination)

Send a ```GET``` request to the endpoint: ``` http://localhost:3000/api/users/page=1&limit=10 ```.

The ```limit``` parameter sets the number of records per page, while ``` page ``` sets the page number


### Add a User

Send a ```POST``` request to the endpoint: ```http://localhost:3000/api/users/```, with the data formatted as: 

```
{
  "name": "Cathy Wacu",
  "email": "example@gmail.com",
  "password": "foureyes"
}
```

### Edit a User

Send a ```PUT``` request to the endpoint: ```http://localhost:3000/api/users/```, with the data formatted as: 

```
{
  "name": "Cathy Wacu",
  "email": "example@gmail.com"
}
```

The fields are optional, but at least one field is required


### Delete Single User

Send a ```DELETE``` request to the endpoint: ```http://localhost:3000/api/users/{id}```, with ```{id}``` being an ID for a user
