# Recipe App API

The Recipe App API is a backend API built using Django and Django REST Framework. It allows users to create, update, and view recipes and ingredients. Users can also create accounts, authenticate with the API using a token, and manage their own recipes.

## Installation

1. Clone the repository

   ```
   git clone https://github.com/Palwisha-18/recipe-app-api.git
   ```

2. Navigate to the project directory

   ```
   cd recipe-app-api
   ```

3. Build the Docker image

   ```
   docker build -t recipe-app-api .
   ```

4. Run the Docker container

   ```
   docker run -p 8000:8000 recipe-app-api
   ```

5. The API should now be available at http://localhost:8000

## Usage

The Recipe App API has the following endpoints:

### Authentication

* `POST /api/user/create/` - create a new user
* `POST /api/user/token/` - authenticate and get an API token
* `POST /api/user/me/` - update the authenticated user's information

### Recipes

* `GET /api/recipe/` - list all recipes
* `GET /api/recipe/{id}/` - retrieve a specific recipe by ID
* `POST /api/recipe/` - create a new recipe
* `PUT /api/recipe/{id}/` - update a specific recipe by ID
* `DELETE /api/recipe/{id}/` - delete a specific recipe by ID

### Ingredients

* `GET /api/ingredient/` - list all ingredients
* `GET /api/ingredient/{id}/` - retrieve a specific ingredient by ID
* `POST /api/ingredient/` - create a new ingredient
* `PUT /api/ingredient/{id}/` - update a specific ingredient by ID
* `DELETE /api/ingredient/{id}/` - delete a specific ingredient by ID

To authenticate, include an `Authorization` header in your request with the value `Token {token}`, where `{token}` is the token obtained from the `/api/user/token/` endpoint.

## Contributing

If you'd like to contribute to the Recipe App API, please follow these steps:

1. Fork the repository
2. Create a new branch for your feature or bugfix
3. Make your changes and write tests if applicable
4. Run the tests with `docker-compose run app sh -c "python manage.py test && flake8"`
5. Submit a pull request
