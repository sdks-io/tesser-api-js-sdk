# Counterparties

```ts
const counterpartiesController = new CounterpartiesController(client);
```

## Class Name

`CounterpartiesController`

## Methods

* [Create](../../doc/controllers/counterparties.md#create)
* [Find All 1](../../doc/controllers/counterparties.md#find-all-1)
* [Find One](../../doc/controllers/counterparties.md#find-one)
* [Update 1](../../doc/controllers/counterparties.md#update-1)


# Create

Create a new counterparty for your workspace.

A counterparty is any external party that your organization transacts with,
such as vendors, customers, or partners.

**Classifications:**

- **individual**: A natural person (requires first/last name)
- **business**: A legal entity (requires legal name)

```ts
async create(
  authorization: string,
  body: CreateCounterpartyRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CreateCounterpartyResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateCounterpartyRequest`](../../doc/models/create-counterparty-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CreateCounterpartyResponse`](../../doc/models/create-counterparty-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

const body: CreateCounterpartyRequest = {
  classification: ClassificationEnum.Individual,
  individualFirstName: 'John',
  individualLastName: 'Doe',
  individualAddressCountry: 'US',
  individualDateOfBirth: '1980-01-01',
  individualNationalIdentificationNumber: '123456789',
  individualStreetAddress1: '123 Main St',
  individualStreetAddress2: 'Apt 4B',
  individualCity: 'New York',
  individualState: 'NY',
  individualPostalCode: '10001',
};

try {
  const response = await counterpartiesController.create(
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


# Find All 1

Retrieve all counterparties for your workspace with optional filtering.

Use query parameters to filter results:

- **classification**: Filter by 'individual' or 'business'

```ts
async findAll1(
  authorization: string,
  classification?: Classification7Enum,
  includeSecure?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CounterpartyListResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `classification` | [`Classification7Enum \| undefined`](../../doc/models/classification-7-enum.md) | Query, Optional | Filter by classification |
| `includeSecure` | `boolean \| undefined` | Query, Optional | Include secure fields (PII) |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CounterpartyListResponse`](../../doc/models/counterparty-list-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

try {
  const response = await counterpartiesController.findAll1(authorization);

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


# Find One

Retrieve a specific counterparty by its unique identifier

```ts
async findOne(
  id: string,
  authorization: string,
  classification?: Classification7Enum,
  includeSecure?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CounterpartyResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | Counterparty ID (UUID) |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `classification` | [`Classification7Enum \| undefined`](../../doc/models/classification-7-enum.md) | Query, Optional | Filter by classification ('individual' or 'business'). |
| `includeSecure` | `boolean \| undefined` | Query, Optional | Include secure fields (PII) |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CounterpartyResponse`](../../doc/models/counterparty-response.md).

## Example Usage

```ts
const id = '3e9a7c2f-1b8d-4e56-a0f3-5c2d8b1e9a7f';

const authorization = 'Bearer <token>';

try {
  const response = await counterpartiesController.findOne(
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


# Update 1

Update an existing counterparty's information.

Only provide the fields you want to update. At least one field must be provided.

**Note:** If changing classification from 'individual' to 'business' (or vice versa),
make sure to also provide the appropriate fields for the new classification.

```ts
async update1(
  id: string,
  authorization: string,
  body: UpdateCounterpartyRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<UpdateCounterpartyResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | Counterparty ID (UUID) |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdateCounterpartyRequest`](../../doc/models/update-counterparty-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`UpdateCounterpartyResponse`](../../doc/models/update-counterparty-response.md).

## Example Usage

```ts
const id = '3e9a7c2f-1b8d-4e56-a0f3-5c2d8b1e9a7f';

const authorization = 'Bearer <token>';

const body: UpdateCounterpartyRequest = {
};

try {
  const response = await counterpartiesController.update1(
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

