# NESTJS TEMPLATE API

This is a REST API template made with NestJs, Prisma and PostgreSQL.
This project is configured to be used with docker compose.
Documentation of the endpoints was made with Swagger.
For unit and e2e tests, Vitest was used.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Testing](#testing)
- [Documentation](#documentation)
- [License](#license)
- [Contact Information](#contact-information)

## Installation

1. Clone the repository (You can also just fork the repository and use it as a template):
    ```sh
    git clone https://github.com/SamuelB7/nestjs-prisma-jwt-api-template.git
    cd nestjs-prisma-jwt-api-template
    ```

2. Copy the `.env.example` to `.env` and configure your environment variables:
    ```sh
    cp .env.example .env
    ```

3. Install dependencies:
    ```sh
    npm install
    ```

4. Make sure to have Docker Compose installed on your machine. The dockerfile.yml in this project will work fine, but I recommend that you change the name of the services and the name of the containers before using it. Also make sure that the environment variables in your .env are correct. 

5. Start the Docker containers:
    ```sh
    sudo docker compose up
    ```

6. Run database migrations:
    ```sh
    npm run prisma:migrate:deploy
    ```

7. If you want to change the structure of the users table you can change the schema and then run:

    ```sh
    npm run prisma:migrate <name-of-your-migration>
    ```

 - By default this project is configured to use PostgreSQL, if you want to use any other database, make sure to change the dockerfile.yml to use the correct image.

## Usage

To start the server in development mode, without docker run:
```sh
npm run start:dev
```
The server will be running at http://localhost:3333

## Testing

To run the unit tests of the api, use the command:
```sh
npm run test
```
To run the e2e tests, use:
```sh
npm run test:e2e
```

## Documentation

After starting the application, go to http://localhost:3333/documentation to check the documentation of the api endpoints

## License

This project is licensed under the MIT License

## Contact Information

For any inquiries, please contact belo.samuel@gmail.com