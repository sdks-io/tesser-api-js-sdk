
# Execute Payment Request Dto

## Structure

`ExecutePaymentRequestDto`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `signature` | `string` | Required | Signature for the specified payment step. |
| `turnkeyStamp` | [`TurnkeyStamp \| undefined`](../../doc/models/turnkey-stamp.md) | Optional | Optional Turnkey stamp data for server-side signing |

## Example (as JSON)

```json
{
  "signature": "signature6",
  "turnkey_stamp": {
    "stampHeaderName": "stampHeaderName0",
    "stampHeaderValue": "stampHeaderValue4",
    "turnkeyBody": "turnkeyBody2"
  }
}
```

