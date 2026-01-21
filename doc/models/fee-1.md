
# Fee 1

## Structure

`Fee1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `feeAmount` | `string` | Required | Fee amount. |
| `feeCurrency` | `string` | Required | Fee currency code. |
| `type` | `string` | Required | Fee type (e.g., 'gas', 'provider'). |
| `metadata` | [`Fee1Metadata \| undefined`](../../doc/models/containers/fee-1-metadata.md) | Optional | This is a container for any-of cases. |

## Example (as JSON)

```json
{
  "fee_amount": "fee_amount6",
  "fee_currency": "fee_currency6",
  "type": "type8",
  "metadata": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

