
# Create Bank Request

## Structure

`CreateBankRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workspaceId` | `string \| undefined` | Optional | ID of the workspace. |
| `name` | `string` | Required | Name of the bank account.<br><br>**Constraints**: *Minimum Length*: `1` |
| `bankName` | `string` | Required | Name of the bank.<br><br>**Constraints**: *Minimum Length*: `1` |
| `bankCodeType` | `string` | Required | Type of bank code (e.g., 'SWIFT').<br><br>**Constraints**: *Minimum Length*: `1` |
| `bankIdentifierCode` | `string` | Required | Bank identifier code value.<br><br>**Constraints**: *Minimum Length*: `1` |
| `bankAccountNumber` | `string` | Required | Bank account number (IBAN, etc).<br><br>**Constraints**: *Minimum Length*: `1` |
| `counterpartyId` | `string \| undefined` | Optional | ID of the counterparty owner. |

## Example (as JSON)

```json
{
  "workspace_id": "b53f6690-3242-4942-9907-885779632832",
  "name": "Operating Account - EU",
  "bank_name": "Chase Bank",
  "bank_code_type": "SWIFT",
  "bank_identifier_code": "CHASUS33",
  "bank_account_number": "123456789",
  "counterparty_id": "counterparty_id2"
}
```

