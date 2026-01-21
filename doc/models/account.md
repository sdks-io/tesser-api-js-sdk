
# Account

## Structure

`Account`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the account. |
| `workspaceId` | `string \| undefined` | Optional | ID of the workspace. |
| `tenantId` | [`AccountTenantId \| undefined`](../../doc/models/containers/account-tenant-id.md) | Optional | This is a container for any-of cases. |
| `counterpartyId` | [`AccountCounterpartyId \| undefined`](../../doc/models/containers/account-counterparty-id.md) | Optional | This is a container for any-of cases. |
| `type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | Account type. |
| `name` | `string` | Required | Account name. |
| `bankName` | [`AccountBankName \| undefined`](../../doc/models/containers/account-bank-name.md) | Optional | This is a container for any-of cases. |
| `bankCodeType` | [`AccountBankCodeType \| undefined`](../../doc/models/containers/account-bank-code-type.md) | Optional | This is a container for any-of cases. |
| `bankIdentifierCode` | [`AccountBankIdentifierCode \| undefined`](../../doc/models/containers/account-bank-identifier-code.md) | Optional | This is a container for any-of cases. |
| `cryptoWalletAddress` | [`AccountCryptoWalletAddress \| undefined`](../../doc/models/containers/account-crypto-wallet-address.md) | Optional | This is a container for any-of cases. |
| `bankAccountNumber` | [`AccountBankAccountNumber \| undefined`](../../doc/models/containers/account-bank-account-number.md) | Optional | This is a container for any-of cases. |
| `createdAt` | `string` | Required | Creation timestamp. |
| `updatedAt` | `string` | Required | Last update timestamp. |

## Example (as JSON)

```json
{
  "id": "id8",
  "workspace_id": "b53f6690-3242-4942-9907-885779632832",
  "type": "stablecoin_solana",
  "name": "name8",
  "created_at": "created_at6",
  "updated_at": "updated_at4",
  "tenant_id": "String9",
  "counterparty_id": "String7",
  "bank_name": "String7",
  "bank_code_type": "String5"
}
```

