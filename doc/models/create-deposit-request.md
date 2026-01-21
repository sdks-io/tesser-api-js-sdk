
# Create Deposit Request

## Structure

`CreateDepositRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fromCurrency` | `string` | Required | Source currency code. |
| `toCurrency` | `string` | Required | Destination currency code. |
| `fromAmount` | `string \| undefined` | Optional | Amount to send. Required if to_amount is missing. |
| `toAmount` | `string \| undefined` | Optional | Amount to receive. Required if from_amount is missing. |
| `tenantId` | `string \| undefined` | Optional | Optional tenant ID. |
| `toAccountId` | `string` | Required | Destination account ID. |
| `toNetwork` | `string` | Required | Network for the deposit. |

## Example (as JSON)

```json
{
  "from_currency": "from_currency4",
  "to_currency": "to_currency6",
  "from_amount": "from_amount8",
  "to_amount": "to_amount4",
  "tenant_id": "tenant_id2",
  "to_account_id": "to_account_id0",
  "to_network": "to_network4"
}
```

