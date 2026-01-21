
# Account Safe

## Structure

`AccountSafe`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the account. |
| `workspaceId` | `string \| undefined` | Optional | ID of the workspace. |
| `tenantId` | [`AccountSafeTenantId \| undefined`](../../doc/models/containers/account-safe-tenant-id.md) | Optional | This is a container for any-of cases. |
| `counterpartyId` | [`AccountSafeCounterpartyId \| undefined`](../../doc/models/containers/account-safe-counterparty-id.md) | Optional | This is a container for any-of cases. |
| `type` | [`TypeEnum`](../../doc/models/type-enum.md) | Required | Account type. |
| `name` | `string` | Required | Account name. |
| `bankName` | [`AccountSafeBankName \| undefined`](../../doc/models/containers/account-safe-bank-name.md) | Optional | This is a container for any-of cases. |
| `bankCodeType` | [`AccountSafeBankCodeType \| undefined`](../../doc/models/containers/account-safe-bank-code-type.md) | Optional | This is a container for any-of cases. |
| `bankIdentifierCode` | [`AccountSafeBankIdentifierCode \| undefined`](../../doc/models/containers/account-safe-bank-identifier-code.md) | Optional | This is a container for any-of cases. |
| `cryptoWalletAddress` | [`AccountSafeCryptoWalletAddress \| undefined`](../../doc/models/containers/account-safe-crypto-wallet-address.md) | Optional | This is a container for any-of cases. |
| `createdAt` | `string` | Required | Creation timestamp. |
| `updatedAt` | `string` | Required | Last update timestamp. |

## Example (as JSON)

```json
{
  "id": "id2",
  "workspace_id": "b53f6690-3242-4942-9907-885779632832",
  "type": "fiat_bank",
  "name": "name2",
  "created_at": "created_at0",
  "updated_at": "updated_at2",
  "tenant_id": "String3",
  "counterparty_id": "String3",
  "bank_name": "String3",
  "bank_code_type": "String9"
}
```

