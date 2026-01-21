
# Update Payment Request

## Structure

`UpdatePaymentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `originatorAccountId` | `string` | Required | ID of the account originating the payment. |
| `sourceAccountId` | `string` | Required | ID of the source account (e.g., wallet). |
| `beneficiaryAccountId` | `string` | Required | ID of the beneficiary account. |
| `organizationReferenceId` | `string \| undefined` | Optional | Optional external reference ID to update. |

## Example (as JSON)

```json
{
  "originator_account_id": "originator_account_id2",
  "source_account_id": "source_account_id6",
  "beneficiary_account_id": "beneficiary_account_id6",
  "organization_reference_id": "organization_reference_id6"
}
```

