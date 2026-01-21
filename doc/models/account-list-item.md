
# Account List Item

## Structure

`AccountListItem`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the account. |
| `workspaceId` | `string \| undefined` | Optional | ID of the workspace. |
| `tenantId` | [`AccountListItemTenantId \| undefined`](../../doc/models/containers/account-list-item-tenant-id.md) | Optional | This is a container for any-of cases. |
| `counterpartyId` | [`AccountListItemCounterpartyId \| undefined`](../../doc/models/containers/account-list-item-counterparty-id.md) | Optional | This is a container for any-of cases. |
| `type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | Account type. |
| `name` | `string` | Required | Account name. |
| `bankName` | [`AccountListItemBankName \| undefined`](../../doc/models/containers/account-list-item-bank-name.md) | Optional | This is a container for any-of cases. |
| `bankCodeType` | [`AccountListItemBankCodeType \| undefined`](../../doc/models/containers/account-list-item-bank-code-type.md) | Optional | This is a container for any-of cases. |
| `bankIdentifierCode` | [`AccountListItemBankIdentifierCode \| undefined`](../../doc/models/containers/account-list-item-bank-identifier-code.md) | Optional | This is a container for any-of cases. |
| `cryptoWalletAddress` | [`AccountListItemCryptoWalletAddress \| undefined`](../../doc/models/containers/account-list-item-crypto-wallet-address.md) | Optional | This is a container for any-of cases. |
| `bankAccountNumber` | [`AccountListItemBankAccountNumber \| undefined`](../../doc/models/containers/account-list-item-bank-account-number.md) | Optional | This is a container for any-of cases. |
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
  "counterparty_id": "String5",
  "bank_name": "String5",
  "bank_code_type": "String5"
}
```

