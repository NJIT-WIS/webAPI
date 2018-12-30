# NJIT FAQ Project

To get started with this project, please have a look at the following:

-   [Local Development Setup](#local-development-setup) - Learn how to run this project locally on your machine
-   [Contributing](#contributing) - Learn how to contribue to this project

## Local Development Setup

**You'll need to have Node 8.10.0 or later and PHP 7.1.3 or later on your local development machine.**

To get started developing, clone this repository:

```sh
git clone git@github.com:kaw393939/webAPI.git
cd webAPI
```

Install project dependencies and create a database file:

```sh
composer install
touch database/database.sqlite
cp .env.example .env
```

Change the content of the `.env` file to the following:

```sh
APP_URL=http://127.0.0.1:8000

DB_CONNECTION=sqlite
DB_HOST=/absolute/path/to/database.sqlite
# DB_CONNECTION=mysql
# DB_HOST=127.0.0.1
# DB_PORT=3306
# DB_DATABASE=homestead
# DB_USERNAME=homestead
# DB_PASSWORD=secret
```

Run migration and generate necessary keys:

```sh
php artisan migrate
php artisan key:generate
php artisan jwt:secret
```

To seed the database:

```sh
php artisan db:seed
```

In order to use the Swagger API make sure that your .env includes:

```sh
L5_SWAGGER_GENERATE_ALWAYS=true
SWAGGER_VERSION=2.0
```

The Swagger Api can be found at:

```sh
http://127.0.0.1:8000/api/documentation
```

For routes that require an authentication token in `Swagger`, make sure to include `Bearer` before placing the value of your token, e.g.:

```sh
Bearer "AUTH_TOKEN"
```

Create a minified bundle of your front-end code:

```sh
cd frontend
npm install
npm run build
npm run build:win # alternatively, when using command prompt
```

Start your development server in the root directory:

```sh
php artisan serve
```

Open `127.0.0.1:3000` or `localhost:3000` to view it in the browser.

To run Dusk tests, after starting your local development server:

```sh
php artisan dusk
```

## Contributing

In order to contribute to codebase of this project, you need to have a knowledge of `Laravel` and `Vue.js`.

To get started learning about these two Web frameworks, please visit the following sites:

-   [Laravel.com](https://laravel.com) - official `Laravel` website
-   [Laracast.com/laravel](https://laracasts.com/skills/laravel) -
    video tutorials for learning `Laravel` from scratch
-   [Vue.js](https://vuejs.org/v2/guide/) - official `Vue.js` website
-   [Laracast.com/vuejs](https://laracasts.com/series/learn-vue-2-step-by-step) - video tutorials for learning `Vue.js` from scratch

### Contributing to Front-End Codebase

Please have a look at the [instructions](frontend/README.md) under the `frontend` directory.
