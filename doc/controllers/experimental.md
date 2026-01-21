# Experimental

```ts
const experimentalController = new ExperimentalController(client);
```

## Class Name

`ExperimentalController`


# Execute Payment

Accepts a signature for a payment step. Currently echoes the request, structured for future execution logic.

```ts
async executePayment(
  paymentId: string,
  stepId: string,
  authorization: string,
  body: ExecutePaymentRequestDto,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PaymentResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paymentId` | `string` | Template, Required | Payment ID to execute. |
| `stepId` | `string` | Template, Required | Transfer step ID to execute. |
| `authorization` | `string` | Header, Required | Bearer token for authentication.<br><br>To obtain a token, make a request to Auth0:<br><br>```bash<br>curl --request POST \<br>  --url https://dev-awqy75wdabpsnsvu.us.auth0.com/oauth/token \<br>  --header 'content-type: application/json' \<br>  --data '{<br>    "client_id":"YOUR_CLIENT_ID",<br>    "client_secret":"YOUR_CLIENT_SECRET",<br>    "audience":"https://sandbox.tesserx.co",<br>    "grant_type":"client_credentials"<br>  }'<br>```<br><br>The response will contain an `access_token` field which should be used as the Bearer token. |
| `body` | [`ExecutePaymentRequestDto`](../../doc/models/execute-payment-request-dto.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`PaymentResponse`](../../doc/models/payment-response.md).

## Example Usage

```ts
const paymentId = 'payment_id0';

const stepId = 'step_id4';

const authorization = 'Bearer <token>';

const body: ExecutePaymentRequestDto = {
  signature: '0xabcdef1234567890abcdef1234567890abcdef1234567890abcdef1234567890',
  turnkeyStamp: {
    stampHeaderName: 'X-Stamp',
    stampHeaderValue: '...',
    turnkeyBody: '...',
  },
};

try {
  const response = await experimentalController.executePayment(
    paymentId,
    stepId,
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

