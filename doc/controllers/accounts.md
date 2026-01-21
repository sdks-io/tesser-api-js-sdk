# Accounts

```ts
const accountsController = new AccountsController(client);
```

## Class Name

`AccountsController`

## Methods

* [Find All](../../doc/controllers/accounts.md#find-all)
* [Create Bank](../../doc/controllers/accounts.md#create-bank)
* [Create Wallet](../../doc/controllers/accounts.md#create-wallet)
* [Find One 2](../../doc/controllers/accounts.md#find-one-2)
* [Update](../../doc/controllers/accounts.md#update)


# Find All

Retrieve all accounts (both bank and wallet accounts) for your workspace.

```ts
async findAll(
  authorization: string,
  type?: Type4Enum,
  tenantId?: string,
  counterpartyId?: string,
  includeSensitive?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<AccountListResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `type` | [`Type4Enum \| undefined`](../../doc/models/type-4-enum.md) | Query, Optional | Filter by account type |
| `tenantId` | `string \| undefined` | Query, Optional | Filter by tenant ID. At most one of tenant_id or counterparty_id may be provided. |
| `counterpartyId` | `string \| undefined` | Query, Optional | Filter by counterparty ID. At most one of tenant_id or counterparty_id may be provided. |
| `includeSensitive` | `boolean \| undefined` | Query, Optional | If true, includes sensitive fields like bank_account_number. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`AccountListResponse`](../../doc/models/account-list-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

try {
  const response = await accountsController.findAll(authorization);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |


# Create Bank

Create a new fiat bank account.

```ts
async createBank(
  authorization: string,
  body: CreateBankRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CreateBankResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateBankRequest`](../../doc/models/create-bank-request.md) | Body, Required | Bank account details |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CreateBankResponse`](../../doc/models/create-bank-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

const body: CreateBankRequest = {
  name: 'Operating Account - EU',
  bankName: 'Chase Bank',
  bankCodeType: 'SWIFT',
  bankIdentifierCode: 'CHASUS33',
  bankAccountNumber: '123456789',
  counterpartyId: '2a7e1c9f-4b3d-4a82-b6e0-8f5c2d1a9b3e',
};

try {
  const response = await accountsController.createBank(
    authorization,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |


# Create Wallet

Create a new stablecoin wallet account.

```ts
async createWallet(
  authorization: string,
  body: CreateWalletRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CreateWalletResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateWalletRequest`](../../doc/models/create-wallet-request.md) | Body, Required | Wallet account details |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CreateWalletResponse`](../../doc/models/create-wallet-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

const body: CreateWalletRequest = {
  workspaceId: 'b53f6690-3242-4942-9907-885779632832',
  name: 'Treasury Wallet (Omnibus)',
  type: Type3Enum.StablecoinEthereum,
  signature: 'eyJwdWJsaWNLZXkiOiJwdWJfZXhhbXBsZSIsInNpZ25hdHVyZSI6InNpZ19leGFtcGxlIiwic2NoZW1lIjoiRUQyNTUxOSJ9',
};

try {
  const response = await accountsController.createWallet(
    authorization,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |


# Find One 2

Retrieve a specific account (wallet or bank) by its unique identifier

```ts
async findOne2(
  id: string,
  authorization: string,
  includeSensitive?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<AccountResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | Account ID (UUID) |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `includeSensitive` | `boolean \| undefined` | Query, Optional | If true, includes sensitive fields like bank_account_number. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`AccountResponse`](../../doc/models/account-response.md).

## Example Usage

```ts
const id = '7a3d8f2e-6b4c-4a91-b8e5-2f9c1d7e3a0b';

const authorization = 'Bearer <token>';

try {
  const response = await accountsController.findOne2(
    id,
    authorization
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |


# Update

Update an existing account's information.

```ts
async update(
  id: string,
  authorization: string,
  body: UpdateAccountRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<UpdateAccountResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | Account ID (UUID) |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdateAccountRequest`](../../doc/models/update-account-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`UpdateAccountResponse`](../../doc/models/update-account-response.md).

## Example Usage

```ts
const id = '7a3d8f2e-6b4c-4a91-b8e5-2f9c1d7e3a0b';

const authorization = 'Bearer <token>';

const body: UpdateAccountRequest = {
  name: 'Updated Treasury Wallet',
};

try {
  const response = await accountsController.update(
    id,
    authorization,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |

