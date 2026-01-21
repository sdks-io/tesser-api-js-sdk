
# Payment

## Structure

`Payment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the payment. |
| `workspaceId` | `string` | Required | Workspace ID the payment belongs to. |
| `organizationReferenceId` | [`PaymentOrganizationReferenceId \| undefined`](../../doc/models/containers/payment-organization-reference-id.md) | Optional | This is a container for any-of cases. |
| `direction` | [`DirectionEnum`](../../doc/models/direction-enum.md) | Required | Payment direction: 'inbound', 'outbound', 'internal'. |
| `paymentType` | [`PaymentTypeEnum`](../../doc/models/payment-type-enum.md) | Required | Type of payment operation: 'payment' (wallet-to-wallet), 'offramp' (crypto-to-fiat), 'onramp' (fiat-to-crypto), 'withdrawal', 'deposit', or 'transfer'. |
| `sourceAccountId` | [`PaymentSourceAccountId \| undefined`](../../doc/models/containers/payment-source-account-id.md) | Optional | This is a container for any-of cases. |
| `originatorAccountId` | [`PaymentOriginatorAccountId \| undefined`](../../doc/models/containers/payment-originator-account-id.md) | Optional | This is a container for any-of cases. |
| `beneficiaryAccountId` | [`PaymentBeneficiaryAccountId \| undefined`](../../doc/models/containers/payment-beneficiary-account-id.md) | Optional | This is a container for any-of cases. |
| `fromAmount` | `string` | Required | Amount to send. |
| `fromCurrency` | `string` | Required | Source currency code. |
| `fromNetwork` | [`PaymentFromNetwork \| undefined`](../../doc/models/containers/payment-from-network.md) | Optional | This is a container for any-of cases. |
| `toAmount` | `string` | Required | Amount to receive. |
| `toCurrency` | `string` | Required | Destination currency code. |
| `toNetwork` | [`PaymentToNetwork \| undefined`](../../doc/models/containers/payment-to-network.md) | Optional | This is a container for any-of cases. |
| `riskStatus` | [`RiskStatusEnum`](../../doc/models/risk-status-enum.md) | Required | Current risk status. |
| `riskStatusReasons` | `(string \| null)[] \| null \| undefined` | Optional | List of reasons for risk status. |
| `riskReviewedBy` | [`PaymentRiskReviewedBy \| undefined`](../../doc/models/containers/payment-risk-reviewed-by.md) | Optional | This is a container for any-of cases. |
| `riskReviewedAt` | [`PaymentRiskReviewedAt \| undefined`](../../doc/models/containers/payment-risk-reviewed-at.md) | Optional | This is a container for any-of cases. |
| `balanceStatus` | [`PaymentBalanceStatus \| null \| undefined`](../../doc/models/containers/payment-balance-status.md) | Optional | This is a container for any-of cases. |
| `balanceReservedAt` | [`PaymentBalanceReservedAt \| undefined`](../../doc/models/containers/payment-balance-reserved-at.md) | Optional | This is a container for any-of cases. |
| `steps` | [`Step[] \| undefined`](../../doc/models/step.md) | Optional | Optional list of system-generated steps that make up this payment/transfer route. |
| `createdAt` | `string` | Required | ISO 8601 timestamp of creation. |
| `updatedAt` | `string` | Required | ISO 8601 timestamp of last update. |
| `expiresAt` | `string` | Required | ISO 8601 timestamp when the quote expires. |

## Example (as JSON)

```json
{
  "id": "id8",
  "workspace_id": "workspace_id0",
  "organization_reference_id": "String7",
  "direction": "outbound",
  "payment_type": "payment",
  "source_account_id": "String7",
  "originator_account_id": "String3",
  "beneficiary_account_id": "String7",
  "from_amount": "from_amount4",
  "from_currency": "from_currency0",
  "from_network": "String7",
  "to_amount": "to_amount0",
  "to_currency": "to_currency2",
  "risk_status": "unchecked",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z",
  "expires_at": "2016-03-13T12:52:32.123Z"
}
```

