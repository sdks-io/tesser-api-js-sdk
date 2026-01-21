
# Data 7

## Structure

`Data7`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the payment |
| `workspaceId` | `string` | Required | Workspace ID the payment belongs to |
| `organizationReferenceId` | [`Data7OrganizationReferenceId \| undefined`](../../doc/models/containers/data-7-organization-reference-id.md) | Optional | This is a container for any-of cases. |
| `direction` | [`Direction1Enum`](../../doc/models/direction-1-enum.md) | Required | Payment direction: 'inbound', 'outbound', 'internal' |
| `paymentType` | [`PaymentTypeEnum`](../../doc/models/payment-type-enum.md) | Required | Type of payment operation: 'payment' (wallet-to-wallet), 'offramp' (crypto-to-fiat), 'onramp' (fiat-to-crypto), 'withdrawal', 'deposit', or 'transfer'. |
| `sourceAccountId` | [`Data7SourceAccountId \| undefined`](../../doc/models/containers/data-7-source-account-id.md) | Optional | This is a container for any-of cases. |
| `originatorAccountId` | [`Data7OriginatorAccountId \| undefined`](../../doc/models/containers/data-7-originator-account-id.md) | Optional | This is a container for any-of cases. |
| `beneficiaryAccountId` | [`Data7BeneficiaryAccountId \| undefined`](../../doc/models/containers/data-7-beneficiary-account-id.md) | Optional | This is a container for any-of cases. |
| `fromAmount` | `string` | Required | Amount to send. |
| `fromCurrency` | `string` | Required | Source currency code. |
| `fromNetwork` | [`Data7FromNetwork \| undefined`](../../doc/models/containers/data-7-from-network.md) | Optional | This is a container for any-of cases. |
| `toAmount` | `string` | Required | Amount to receive. |
| `toCurrency` | `string` | Required | Destination currency code. |
| `toNetwork` | [`Data7ToNetwork \| undefined`](../../doc/models/containers/data-7-to-network.md) | Optional | This is a container for any-of cases. |
| `riskStatus` | [`RiskStatusEnum`](../../doc/models/risk-status-enum.md) | Required | Current risk status. |
| `riskStatusReasons` | [`Data7RiskStatusReasons \| undefined`](../../doc/models/containers/data-7-risk-status-reasons.md) | Optional | This is a container for any-of cases. |
| `riskReviewedBy` | [`Data7RiskReviewedBy \| undefined`](../../doc/models/containers/data-7-risk-reviewed-by.md) | Optional | This is a container for any-of cases. |
| `riskReviewedAt` | [`Data7RiskReviewedAt \| undefined`](../../doc/models/containers/data-7-risk-reviewed-at.md) | Optional | This is a container for any-of cases. |
| `balanceStatus` | [`Data7BalanceStatus \| undefined`](../../doc/models/containers/data-7-balance-status.md) | Optional | This is a container for any-of cases. |
| `balanceReservedAt` | [`Data7BalanceReservedAt \| undefined`](../../doc/models/containers/data-7-balance-reserved-at.md) | Optional | This is a container for any-of cases. |
| `steps` | [`Step[] \| undefined`](../../doc/models/step.md) | Optional | Optional list of system-generated steps that make up this payment/transfer route. |
| `createdAt` | `string` | Required | ISO 8601 timestamp of creation. |
| `updatedAt` | `string` | Required | ISO 8601 timestamp of last update. |
| `expiresAt` | `string` | Required | ISO 8601 timestamp when the quote expires. |

## Example (as JSON)

```json
{
  "id": "id4",
  "workspace_id": "workspace_id6",
  "organization_reference_id": "String3",
  "direction": "inbound",
  "payment_type": "onramp",
  "source_account_id": "String3",
  "originator_account_id": "String7",
  "beneficiary_account_id": "String1",
  "from_amount": "from_amount0",
  "from_currency": "from_currency6",
  "from_network": "String3",
  "to_amount": "to_amount6",
  "to_currency": "to_currency8",
  "risk_status": "approved",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z",
  "expires_at": "2016-03-13T12:52:32.123Z"
}
```

