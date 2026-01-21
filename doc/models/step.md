
# Step

## Structure

`Step`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the step. |
| `transferId` | `string` | Required | ID of the parent payment/transfer. |
| `stepSequence` | `number` | Required | Step sequence number (0-based or 1-based).<br><br>**Constraints**: `>= -9007199254740991`, `<= 9007199254740991` |
| `stepType` | [`StepTypeEnum`](../../doc/models/step-type-enum.md) | Required | Step type: 'stablecoin_transfer', 'offramp', 'onramp', 'fiat_transfer'. |
| `fromAccountAssetId` | [`StepFromAccountAssetId \| undefined`](../../doc/models/containers/step-from-account-asset-id.md) | Optional | This is a container for any-of cases. |
| `fromAccountId` | [`StepFromAccountId \| undefined`](../../doc/models/containers/step-from-account-id.md) | Optional | This is a container for any-of cases. |
| `fromAmount` | `string` | Required | Amount sent in this step. |
| `fromCurrency` | `string` | Required | Currency code sent in this step. |
| `toAccountAssetId` | [`StepToAccountAssetId \| undefined`](../../doc/models/containers/step-to-account-asset-id.md) | Optional | This is a container for any-of cases. |
| `toAccountId` | [`StepToAccountId \| undefined`](../../doc/models/containers/step-to-account-id.md) | Optional | This is a container for any-of cases. |
| `toAmount` | `string` | Required | Amount received in this step. |
| `toCurrency` | `string` | Required | Currency code received in this step. |
| `transactionHash` | [`StepTransactionHash \| undefined`](../../doc/models/containers/step-transaction-hash.md) | Optional | This is a container for any-of cases. |
| `fees` | [`Fee1[] \| undefined`](../../doc/models/fee-1.md) | Optional | List of fees associated with this step. |
| `providerKey` | [`StepProviderKey \| undefined`](../../doc/models/containers/step-provider-key.md) | Optional | This is a container for any-of cases. |
| `status` | [`Status1Enum`](../../doc/models/status-1-enum.md) | Required | Step status: 'created', 'submitted', 'confirmed', 'finalized', 'failed'. |
| `statusReasons` | [`StepStatusReasons \| undefined`](../../doc/models/containers/step-status-reasons.md) | Optional | This is a container for any-of cases. |
| `submittedAt` | [`StepSubmittedAt \| undefined`](../../doc/models/containers/step-submitted-at.md) | Optional | This is a container for any-of cases. |
| `confirmedAt` | [`StepConfirmedAt \| undefined`](../../doc/models/containers/step-confirmed-at.md) | Optional | This is a container for any-of cases. |
| `finalizedAt` | [`StepFinalizedAt \| undefined`](../../doc/models/containers/step-finalized-at.md) | Optional | This is a container for any-of cases. |
| `completedAt` | [`StepCompletedAt \| undefined`](../../doc/models/containers/step-completed-at.md) | Optional | This is a container for any-of cases. |
| `failedAt` | [`StepFailedAt \| undefined`](../../doc/models/containers/step-failed-at.md) | Optional | This is a container for any-of cases. |
| `createdAt` | `string` | Required | ISO 8601 timestamp of creation. |
| `updatedAt` | `string` | Required | ISO 8601 timestamp of last update. |

## Example (as JSON)

```json
{
  "id": "id0",
  "transfer_id": "transfer_id6",
  "step_sequence": 202,
  "step_type": "onramp",
  "from_account_asset_id": "String1",
  "from_account_id": "String7",
  "from_amount": "from_amount6",
  "from_currency": "from_currency2",
  "to_account_asset_id": "String1",
  "to_account_id": "String9",
  "to_amount": "to_amount2",
  "to_currency": "to_currency4",
  "transaction_hash": "String5",
  "status": "completed",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z"
}
```

