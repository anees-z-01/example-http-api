# Example HTTP API

A compact Node.js HTTP service with route handling, authentication helpers, and a persistence abstraction. This is a useful repository for reviewing request flow without the weight of a full application framework.

## Read the service

`index.js` is the entry point. `lib/server.js` creates the server, `lib/api.js` defines the API, and `lib/db.js` selects persistence. The `test` directory separates route checks from model behavior.

Use the configuration keys in `.env.example` for local development. Install the locked dependencies with `npm ci`, then use the start and test scripts in `package.json`. Check `config.js` before choosing a port or database adapter; this sample is not a hosted service.

## What to evaluate

Follow an incoming request through routing, authentication, and model access. The next useful engineering work is consistent error responses and explicit request-size limits. A short API transcript showing success, invalid input, and unauthorized access would communicate more than a UI screenshot.

The original material included Git rebase exercise instructions. Those instructions describe its origin, not a requirement for someone running the API today. Upstream package attribution is retained.

A missing export separator was corrected. Static Node parsing and isolated checks of reverse, echo, and put/get handlers passed; external persistence, authentication, streaming, and HTTP integration were not exercised.
