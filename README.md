# Bebop

Another web framework for Node.js

## Install

```bash
# install with npm:
npm install krzyurb/bebop

# or with yarn:
yarn add https://github.com/krzyurb/bebop
```

## Usage Example

### Javascript

```js
const { App } = require('bebop');

// basic server config
const config = { appName: 'myJsApp', port: 3003 };

// endpoint definition
const helloEndpoint = {
  method: 'get',
  path: '/hello',
  perform: () => ({ status: 200, body: 'Hello world!' }),
};

// create application
const app = new App(config, [helloEndpoint]);

// run server
app.listen();
```

### Typescript

```ts
import { App, Response, HTTPMethods } from "bebop";

// basic server config
const config = { appName: "myTsApp", port: 3003 };

// endpoint definition
const endpoint = {
  path: "/hello",
  method: HTTPMethods.GET,
  perform: () => Response.success("Hello world!"),
};

// create application
const app = new App(config, [endpoint]);

// run server
app.listen();

```
