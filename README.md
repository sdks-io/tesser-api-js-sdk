
# Getting Started with Tesser API (v1)

## Introduction

The Tesser Payments Platform API documentation (v1)

## Install the Package

Run the following command from your project directory to install the package from npm:

```bash
npm install tesser-api-sdk@1.0.0
```

For additional package details, see the [Npm page for the tesser-api-sdk@1.0.0 npm](https://www.npmjs.com/package/tesser-api-sdk/v/1.0.0).

## Test the SDK

To validate the functionality of this SDK, you can execute all tests located in the `test` directory. This SDK utilizes `Jest` as both the testing framework and test runner.

To run the tests, navigate to the root directory of the SDK and execute the following command:

```bash
npm run test
```

Or you can also run tests with coverage report:

```bash
npm run test:coverage
```

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| bearerAuthCredentials | [`BearerAuthCredentials`](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/auth/oauth-2-bearer-token.md) | The credential object for bearerAuth |

The API client can be initialized as follows:

### Code-Based Client Initialization

```ts
import { Client } from 'tesser-api-sdk';

const client = new Client({
  bearerAuthCredentials: {
    accessToken: 'AccessToken'
  },
  timeout: 0,
});
```

### Configuration-Based Client Initialization

```ts
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'tesser-api-sdk';

// Provide absolute path for the configuration file
const absolutePath = path.resolve('./config.json');

// Read the configuration file content
const fileContent = fs.readFileSync(absolutePath, 'utf-8');

// Initialize client from JSON configuration content
const client = Client.fromJsonConfig(fileContent);
```

See the [Configuration-Based Client Initialization](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/configuration-based-client-initialization.md) section for details.

### Environment-Based Client Initialization

```ts
import * as dotenv from 'dotenv';
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'tesser-api-sdk';

// Optional - Provide absolute path for the .env file
const absolutePath = path.resolve('./.env');

if (fs.existsSync(absolutePath)) {
  // Load environment variables from .env file
  dotenv.config({ path: absolutePath, override: true });
}

// Initialize client using environment variables
const client = Client.fromEnvironment(process.env);
```

See the [Environment-Based Client Initialization](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/environment-based-client-initialization.md) section for details.

## Authorization

This API uses the following authentication schemes.

* [`bearer (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/auth/oauth-2-bearer-token.md)

## List of APIs

* [Payments](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/payments.md)
* [Health](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/health.md)
* [Accounts](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/accounts.md)
* [Currencies](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/currencies.md)
* [Counterparties](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/counterparties.md)
* [Tenants](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/tenants.md)
* [Networks](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/networks.md)
* [Experimental](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/experimental.md)
* [Treasury](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/controllers/treasury.md)

## SDK Infrastructure

### Configuration

* [HttpClientOptions](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/http-client-options.md)
* [RetryConfiguration](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/retry-configuration.md)
* [ProxySettings](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/proxy-settings.md)
* [Configuration-Based Client Initialization](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/configuration-based-client-initialization.md)
* [Environment-Based Client Initialization](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/environment-based-client-initialization.md)

### HTTP

* [HttpRequest](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/http-request.md)

### Utilities

* [ApiResponse](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/api-response.md)
* [ApiError](https://www.github.com/sdks-io/tesser-api-js-sdk/tree/1.0.0/doc/api-error.md)

