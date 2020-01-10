# express-svelte-template

This is a project template for [Express](https://expressjs.com/) and [Svelte](https://svelte.dev) apps. It includes basic [TypeScript](https://www.typescriptlang.org/) setup and [Jest](https://jestjs.io/) tests setup for the backend.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit somi92/express-svelte-template my-app
cd my-app
```

_Note that you will need to have [Node.js](https://nodejs.org) installed._

## Get started

Change appropriate project fields in `package.json` (name, version and description).

Install the dependencies:

```bash
cd my-app
npm install
```

### Development mode

Start development mode:

```bash
npm run dev:live
```

The script will run the backend and frontend build processes in parallel.

Backend Express API will be started on [localhost:8080](http://localhost:8080). Navigate to [localhost:8080/hello](http://localhost:8080/hello) to see a sample response. Make a change to TypeScript (`.ts`) file in `src`, save it and reload the page to see your changes.

Navigate to [localhost:5000](http://localhost:5000). You should see your frontend Svelte app running. Edit a component file in `src/client`, save it and the page should automatically reload so you can see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

### Production build

Run production build:

```bash
npm run prod
```

The script will run the production build process which outputs its results in the `dist` directory. You can run the production build locally with:

```bash
npm run prod:start
```

Navigate to [localhost:8080](http://localhost:8080) to see your app running (both the API and the frontend are served from localhost:8080).

To run the both scripts in one go:

```bash
npm run prod:live
```

### Tests

Run the backend tests with:

```bash
npm run test
```

To run the tests in watch mode (tests will re-run on save):

```bash
npm run test:watch
```

## License

[MIT License](LICENSE.md).
