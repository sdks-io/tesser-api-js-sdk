# Payments

```ts
const paymentsController = new PaymentsController(client);
```

## Class Name

`PaymentsController`

## Methods

* [Get Payments](../../doc/controllers/payments.md#get-payments)
* [Create Payment](../../doc/controllers/payments.md#create-payment)
* [Get Payment by Id](../../doc/controllers/payments.md#get-payment-by-id)
* [Update Payment](../../doc/controllers/payments.md#update-payment)
* [Review Payment](../../doc/controllers/payments.md#review-payment)


# Get Payments

Retrieve all payments for the authenticated user's organization.

```ts
async getPayments(
  authorization: string,
  startDate?: string,
  endDate?: string,
  paymentType?: PaymentType3Enum,
  page?: number,
  limit?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentListResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `startDate` | `string \| undefined` | Query, Optional | Filter payments created on or after this ISO 8601 date. |
| `endDate` | `string \| undefined` | Query, Optional | Filter payments created before this ISO 8601 date. |
| `paymentType` | [`PaymentType3Enum \| undefined`](../../doc/models/payment-type-3-enum.md) | Query, Optional | Filter payments by type ('withdrawal', 'deposit', 'onramp', 'offramp', 'payment', 'transfer'). |
| `page` | `number \| undefined` | Query, Optional | Page number for pagination (1-based). |
| `limit` | `number \| undefined` | Query, Optional | Number of items per page. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentListResponse`](../../doc/models/payment-list-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

try {
  const response = await paymentsController.getPayments(authorization);

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


# Create Payment

Create a payment. Returns the created payment details.

```ts
async createPayment(
  authorization: string,
  body: CreatePaymentRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreatePaymentRequest`](../../doc/models/create-payment-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentResponse`](../../doc/models/payment-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

const body: CreatePaymentRequest = {
  fromCurrency: 'USDC',
  toCurrency: 'USDC',
  fromAmount: '0.01',
  toAmount: '0.01',
  fromNetwork: 'POLYGON',
  toNetwork: 'POLYGON',
  organizationReferenceId: 'ref_123',
  originatorAccountId: '2113b166-5873-42fd-85fe-5b1a02940d43',
  sourceAccountId: '6de8a7e9-be79-4885-9b65-b25b11d38078',
  beneficiaryAccountId: '53b7aabd-97bc-4a4f-9f9c-1c1c69474889',
};

try {
  const response = await paymentsController.createPayment(
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


# Get Payment by Id

Retrieve a specific payment by ID.

```ts
async getPaymentById(
  paymentId: string,
  authorization: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string` | Template, Required | - |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentResponse`](../../doc/models/payment-response.md).

## Example Usage

```ts
const paymentId = 'paymentId2';

const authorization = 'Bearer <token>';

try {
  const response = await paymentsController.getPaymentById(
    paymentId,
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


# Update Payment

Update a payment with accounts.

```ts
async updatePayment(
  paymentId: string,
  authorization: string,
  body: UpdatePaymentRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string` | Template, Required | - |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`UpdatePaymentRequest`](../../doc/models/update-payment-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentResponse`](../../doc/models/payment-response.md).

## Example Usage

```ts
const paymentId = 'paymentId2';

const authorization = 'Bearer <token>';

const body: UpdatePaymentRequest = {
  originatorAccountId: '2113b166-5873-42fd-85fe-5b1a02940d43',
  sourceAccountId: '6de8a7e9-be79-4885-9b65-b25b11d38078',
  beneficiaryAccountId: '53b7aabd-97bc-4a4f-9f9c-1c1c69474889',
  organizationReferenceId: 'ref_456',
};

try {
  const response = await paymentsController.updatePayment(
    paymentId,
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


# Review Payment

Manually review and approve or reject a payment requiring risk review.

```ts
async reviewPayment(
  paymentId: string,
  authorization: string,
  body: ReviewPaymentRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string` | Template, Required | Unique identifier of the payment to review |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`ReviewPaymentRequest`](../../doc/models/review-payment-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentResponse`](../../doc/models/payment-response.md).

## Example Usage

```ts
const paymentId = '5a9c3e7f-2b1d-4f48-a6e0-8c4b2d1f9a3e';

const authorization = 'Bearer <token>';

const body: ReviewPaymentRequest = {
  isApproved: true,
};

try {
  const response = await paymentsController.reviewPayment(
    paymentId,
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

