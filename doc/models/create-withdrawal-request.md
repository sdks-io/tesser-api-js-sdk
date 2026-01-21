
# Create Withdrawal Request

## Structure

`CreateWithdrawalRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `toAccountId` | `string` | Required | Destination account ID. |
| `fromCurrency` | `string` | Required | Source currency code. |
| `toCurrency` | `string` | Required | Destination currency code. |
| `fromAmount` | `string \| undefined` | Optional | Amount to send. Required if to_amount is missing. |
| `toAmount` | `string \| undefined` | Optional | Amount to receive. Required if from_amount is missing. |
| `tenantId` | `string \| undefined` | Optional | Optional tenant ID. |
| `fromAccountId` | `string` | Required | Source account ID. |
| `fromNetwork` | `string` | Required | Network for the withdrawal. |

## Example (as JSON)

```json
{
  "to_account_id": "to_account_id4",
  "from_currency": "from_currency8",
  "to_currency": "to_currency0",
  "from_amount": "from_amount2",
  "to_amount": "to_amount8",
  "tenant_id": "tenant_id6",
  "from_account_id": "from_account_id2",
  "from_network": "from_network4"
}
```

