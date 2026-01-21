
# Create Payment Request

## Structure

`CreatePaymentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fromCurrency` | `string` | Required | Source currency code (e.g., 'USDC'). See GET /currencies for supported values.<br><br>**Constraints**: *Minimum Length*: `1` |
| `toCurrency` | `string` | Required | Destination currency code (e.g., 'USD'). See GET /currencies for supported values.<br><br>**Constraints**: *Minimum Length*: `1` |
| `fromAmount` | `string \| undefined` | Optional | Amount to send in source currency units. Required if to_amount is not provided. |
| `toAmount` | `string \| undefined` | Optional | Amount to receive in destination currency units. Required if from_amount is not provided. |
| `fromNetwork` | `string \| undefined` | Optional | Blockchain network for source currency (e.g., 'POLYGON'). See GET /networks for supported values.<br><br>**Constraints**: *Minimum Length*: `1` |
| `toNetwork` | `string \| undefined` | Optional | Blockchain network for destination currency (if applicable). See GET /networks for supported values.<br><br>**Constraints**: *Minimum Length*: `1` |
| `organizationReferenceId` | `string \| undefined` | Optional | Optional external reference ID for the organization. |
| `originatorAccountId` | `string \| undefined` | Optional | ID of the account originating the payment. |
| `sourceAccountId` | `string \| undefined` | Optional | ID of the source account (e.g., wallet). |
| `beneficiaryAccountId` | `string \| undefined` | Optional | ID of the beneficiary account. |

## Example (as JSON)

```json
{
  "from_currency": "from_currency8",
  "to_currency": "to_currency0",
  "from_amount": "from_amount2",
  "to_amount": "to_amount8",
  "from_network": "from_network4",
  "to_network": "to_network8",
  "organization_reference_id": "organization_reference_id4"
}
```

