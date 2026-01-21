# Treasury

```ts
const treasuryController = new TreasuryController(client);
```

## Class Name

`TreasuryController`

## Methods

* [Create Deposit](../../doc/controllers/treasury.md#create-deposit)
* [Create Withdrawal](../../doc/controllers/treasury.md#create-withdrawal)


# Create Deposit

Create a deposit payment.

```ts
async createDeposit(
  authorization: string,
  body: CreateDepositRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateDepositRequest`](../../doc/models/create-deposit-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentResponse`](../../doc/models/payment-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

const body: CreateDepositRequest = {
  fromCurrency: 'USD',
  toCurrency: 'USDC',
  toAccountId: '44031e7e-d416-45f0-a46b-ded12b9751ca',
  toNetwork: 'ETHEREUM',
  fromAmount: '1000',
};

try {
  const response = await treasuryController.createDeposit(
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


# Create Withdrawal

Create a withdrawal payment.

```ts
async createWithdrawal(
  authorization: string,
  body: CreateWithdrawalRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`CreateWithdrawalRequest`](../../doc/models/create-withdrawal-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentResponse`](../../doc/models/payment-response.md).

## Example Usage

```ts
const authorization = 'Bearer <token>';

const body: CreateWithdrawalRequest = {
  toAccountId: '44031e7e-d416-45f0-a46b-ded12b9751ca',
  fromCurrency: 'USDC',
  toCurrency: 'USD',
  fromAccountId: '55042f8f-e527-56f1-b57c-eef23ca862db',
  fromNetwork: 'ETHEREUM',
  fromAmount: '1000',
};

try {
  const response = await treasuryController.createWithdrawal(
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

