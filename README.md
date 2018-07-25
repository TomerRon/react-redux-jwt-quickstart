# react-redux-jwt-quickstart

This repository contains boilerplate code to get started on a full-stack web app that uses a Flux store and JSON Web Token for authentication.

Built on a React, Redux, Webpack, Express, PostgreSQL stack.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine.

### Prerequisites

Clone this repository:

```
git clone https://github.com/TomerRon/react-redux-jwt-quickstart
cd react-redux-jwt-quickstart
```

Install the required node modules:

```
npm i
```

### Setting it up

Create a file called `.env` in the root folder and set your environment variables:

```
$ touch .env
```

```
# .env: (you should generate your own keys)

JWT_SECRET=abcdef12345678
SESSION_SECRET=zyxwvuts87654321
```

Configure the database:

```
# /config/config.json:

"development": {
    "username": "your_db_username",
    "password": "your_db_password",
    "database": "your_db_name",
    "host": "localhost",
    "dialect": "postgres",
    "logging": false
}
```

Finally, run the database migrations:

```
$ node_modules/.bin/sequelize db:migrate
```

### Running the tests

```
$ npm test              # Run all tests

$ npm run test-server   # Run server tests (API, Auth)

$ npm run test-client   # Run client tests (Redux)
```

### Running the app

In a terminal window, run `webpack` to compile the React app. `webpack` in watch mode will recompile your React app whenever it changes:

```
$ webpack
```

In another terminal window, run `npm start` to start the Express server. `nodemon` will recompile the Express app whenever it changes:

```
$ npm start
```

## License

This project is licensed under the ISC License - see the [LICENSE.md](LICENSE.md) file for details.
