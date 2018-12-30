# NJIT FAQ Project - SPA Codebase

**Before you start contributing to this project's front-end codebase, make sure you have a good understanding of `Vue.js` and front-end Web development. Please look through the learning resources above to learn more about modern front-end Web frameworks.**

To start contributing, please familiarize yourself with the following sections:

-   [Development Setup & Scripts](#development-setup-&-scripts) - Learn about requirements for running this codebase on your machine
-   [Pull Requests](#pull-requests) - Learn about requirements that need to be satisfied before submitting a pull request

## Development Setup & Scripts

**You'll need to have Node 8.10.0 or later on your machine.**

Install project dependencies by running the following command:

```sh
npm install
```

#### Install all project dependencies

```sh
npm run serve
```

#### Compile and start hot-reloading server for local development

Make sure Laravel is up and running (`php artisan serve`) prior to typing this command.

```sh
npm run serve
```

#### Complie and minify for production

```sh
npm run build

# alternatively, when using command prompt on Windows
npm run build:win
```

#### Run tests

```sh
npm run test
```

#### Lint and fix files

```sh
npm run lint
```

#### Run unit tests

```sh
npm run test:unit
```

#### Run end-to-end tests

```sh
npm run test:e2e
```

## Pull Requests

Every `pull request` requires unit tests and must follow best practices for writing front-end code. In order to check whether your contribution is ready for a pull request, you can take advantage of the `scripts` specified in the `frontend/package.json` file.

The test script will run all unit tests to make sure your code behaves exactly how you're expecting.

```sh
npm run test:unit
```

To check whether your code is following best practices, you can use the following command:

```sh
npm run lint
```

If errors appear in your terminal, make sure you go back and fix them as necessary.

#### Notes on Linting and Unit Testing

Linting is done using the popular [`ESlint`](https://eslint.org) JavaScript linter. If you're unsure how to fix your linting errors, I recommend looking through the list of rules and how to fix them:

-   [ESLint Rules](https://eslint.org/docs/rules/)

---

**It is highly recommended that you go through the resources below to learn how to write tests for front-end code and `Vue.js`.**

All unit tests are executed using [`Jest`](https://jestjs.io/en/). To learn more about `Jest`, please look through its documentation:

-   [Jest Getting Started](https://jestjs.io/docs/en/getting-started.html)
-   [Jest Matchers](https://jestjs.io/docs/en/expect)

In addition to `Jest`, the [`vue-test-utils`](https://github.com/vuejs/vue-test-utils) package is used to test all `Vue.js` related code. It is **highly recommended** to go through its [documentation](https://vue-test-utils.vuejs.org/guides/#getting-started) to learn how to properly test `Vue.js` components.

-   [Unit Testing Introduction](https://vuejs.org/v2/guide/unit-testing.html)
-   [Unit Testing Vue Components](https://vuejs.org/v2/cookbook/unit-testing-vue-components.html)
-   [Knowing What to Test](https://vue-test-utils.vuejs.org/guides/#common-tips)

Each test file needs to be located in the `frontend/tests/unit` directory and should follow the `.spec` naming convention, for example:

```sh
frontend/src/components/MyComponent.vue
frontend/tests/unit/components/MyComponent.spec.js # your test code goes here
```
