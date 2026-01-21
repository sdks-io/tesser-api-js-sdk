# Tenants

```ts
const tenantsController = new TenantsController(client);
```

## Class Name

`TenantsController`

## Methods

* [Create 1](../../doc/controllers/tenants.md#create-1)
* [Find All 2](../../doc/controllers/tenants.md#find-all-2)
* [Find One 1](../../doc/controllers/tenants.md#find-one-1)
* [Update 2](../../doc/controllers/tenants.md#update-2)


# Create 1

Create a new tenant for your workspace. Tenants are business customers that integrate via APIs.

```ts
async create1(
  authorization: string,
  body: CreateTenantRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CreateTenantResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateTenantRequest`](../../doc/models/create-tenant-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CreateTenantResponse`](../../doc/models/create-tenant-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

const body: CreateTenantRequest = {
  businessLegalName: 'Acme Corporation',
  businessDba: 'Acme Co',
  businessAddressCountry: 'US',
  businessStreetAddress1: '123 Corp Blvd',
  businessStreetAddress2: 'Suite 100',
  businessCity: 'New York',
  businessState: 'NY',
  businessLegalEntityIdentifier: '123456789',
  webhookUrl: 'https://example.com/webhooks/tesser',
};

try {
  const response = await tenantsController.create1(
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

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e",
    "workspace_id": "b53f6690-3242-4942-9907-885779632832",
    "business_legal_name": "Acme Corporation",
    "business_dba": "Acme Co",
    "business_address_country": "US",
    "business_street_address1": "123 Corp Blvd",
    "business_street_address2": "Suite 100",
    "business_city": "New York",
    "business_state": "NY",
    "business_legal_entity_identifier": "9876543210",
    "country": "US",
    "webhook_url": "https://acme.com/webhooks/tesser",
    "created_at": "2024-01-15T10:30:00.000Z",
    "updated_at": "2024-01-15T10:30:00.000Z"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |


# Find All 2

Retrieve all tenants for your workspace with optional search filtering.

```ts
async findAll2(
  authorization: string,
  includeSecure?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<TenantListResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `includeSecure` | `boolean \| undefined` | Query, Optional | Include secure fields (PII) |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`TenantListResponse`](../../doc/models/tenant-list-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

try {
  const response = await tenantsController.findAll2(authorization);

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


# Find One 1

Retrieve a specific tenant by its unique identifier

```ts
async findOne1(
  id: string,
  authorization: string,
  includeSecure?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<TenantResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | Tenant ID (UUID) |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `includeSecure` | `boolean \| undefined` | Query, Optional | Include secure fields (PII) |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`TenantResponse`](../../doc/models/tenant-response.md).

## Example Usage

```ts
const id = '4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e';

const authorization = 'Bearer <token>';

try {
  const response = await tenantsController.findOne1(
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

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e",
    "workspace_id": "b53f6690-3242-4942-9907-885779632832",
    "business_legal_name": "Acme Corporation",
    "business_dba": "Acme Co",
    "business_address_country": "US",
    "business_street_address1": "123 Corp Blvd",
    "business_street_address2": "Suite 100",
    "business_city": "New York",
    "business_state": "NY",
    "business_legal_entity_identifier": "9876543210",
    "country": "US",
    "webhook_url": "https://acme.com/webhooks/tesser",
    "created_at": "2024-01-15T10:30:00.000Z",
    "updated_at": "2024-01-15T10:30:00.000Z"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |


# Update 2

Update an existing tenant's information.

Only the following fields can be updated:

- business_legal_name
- business_dba
- business_address_country
- webhook_url

At least one field must be provided.

```ts
async update2(
  id: string,
  authorization: string,
  body: UpdateTenantRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<UpdateTenantResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Template, Required | Tenant ID (UUID) |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdateTenantRequest`](../../doc/models/update-tenant-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`UpdateTenantResponse`](../../doc/models/update-tenant-response.md).

## Example Usage

```ts
const id = '4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e';

const authorization = 'Bearer <token>';

const body: UpdateTenantRequest = {
  businessDba: 'Acme Corp Updated',
  webhookUrl: 'https://acme.com/webhooks/tesser',
};

try {
  const response = await tenantsController.update2(
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

## Example Response *(as JSON)*

```json
{
  "data": {
    "id": "4e8c2a6f-1b9d-4f37-a5e0-7c3b8d2f1a9e",
    "workspace_id": "b53f6690-3242-4942-9907-885779632832",
    "business_legal_name": "Acme Corporation",
    "business_dba": "Acme Corp Updated",
    "business_address_country": "US",
    "business_street_address1": "123 Corp Blvd",
    "business_street_address2": "Suite 100",
    "business_city": "New York",
    "business_state": "NY",
    "business_legal_entity_identifier": "9876543210",
    "country": "US",
    "webhook_url": "https://acme.com/webhooks/tesser",
    "created_at": "2024-01-15T10:30:00.000Z",
    "updated_at": "2024-03-01T12:00:00.000Z"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Details coming soon | `ApiError` |

