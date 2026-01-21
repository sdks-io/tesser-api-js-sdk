
# Transfer Step

## Structure

`TransferStep`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the step. |
| `transferId` | `string` | Required | ID of the parent payment/transfer. |
| `stepSequence` | `number` | Required | Step sequence number (0-based or 1-based).<br><br>**Constraints**: `>= -9007199254740991`, `<= 9007199254740991` |
| `stepType` | [`StepTypeEnum`](../../doc/models/step-type-enum.md) | Required | Step type: 'stablecoin_transfer', 'offramp', 'onramp', 'fiat_transfer'. |
| `fromAccountAssetId` | [`TransferStepFromAccountAssetId \| undefined`](../../doc/models/containers/transfer-step-from-account-asset-id.md) | Optional | This is a container for any-of cases. |
| `fromAmount` | `string` | Required | Amount sent in this step. |
| `fromCurrency` | `string` | Required | Currency code sent in this step. |
| `toAccountAssetId` | [`TransferStepToAccountAssetId \| undefined`](../../doc/models/containers/transfer-step-to-account-asset-id.md) | Optional | This is a container for any-of cases. |
| `toAmount` | `string` | Required | Amount received in this step. |
| `toCurrency` | `string` | Required | Currency code received in this step. |
| `transactionHash` | [`TransferStepTransactionHash \| undefined`](../../doc/models/containers/transfer-step-transaction-hash.md) | Optional | This is a container for any-of cases. |
| `fees` | [`Fee1[] \| undefined`](../../doc/models/fee-1.md) | Optional | List of fees associated with this step. |
| `providerKey` | [`TransferStepProviderKey \| null \| undefined`](../../doc/models/containers/transfer-step-provider-key.md) | Optional | This is a container for any-of cases. |
| `status` | [`StatusEnum`](../../doc/models/status-enum.md) | Required | Step status: 'created', 'submitted', 'confirmed', 'finalized', 'failed'. |
| `statusReasons` | `(string \| null)[] \| null \| undefined` | Optional | Array of reasons explaining the current status (if any). |
| `submittedAt` | [`TransferStepSubmittedAt \| undefined`](../../doc/models/containers/transfer-step-submitted-at.md) | Optional | This is a container for any-of cases. |
| `confirmedAt` | [`TransferStepConfirmedAt \| undefined`](../../doc/models/containers/transfer-step-confirmed-at.md) | Optional | This is a container for any-of cases. |
| `finalizedAt` | [`TransferStepFinalizedAt \| undefined`](../../doc/models/containers/transfer-step-finalized-at.md) | Optional | This is a container for any-of cases. |
| `completedAt` | [`TransferStepCompletedAt \| undefined`](../../doc/models/containers/transfer-step-completed-at.md) | Optional | This is a container for any-of cases. |
| `failedAt` | [`TransferStepFailedAt \| undefined`](../../doc/models/containers/transfer-step-failed-at.md) | Optional | This is a container for any-of cases. |
| `createdAt` | `string` | Required | ISO 8601 timestamp of creation. |
| `updatedAt` | `string` | Required | ISO 8601 timestamp of last update. |
| `fromAccountId` | [`TransferStepFromAccountId \| undefined`](../../doc/models/containers/transfer-step-from-account-id.md) | Optional | This is a container for any-of cases. |
| `toAccountId` | [`TransferStepToAccountId \| undefined`](../../doc/models/containers/transfer-step-to-account-id.md) | Optional | This is a container for any-of cases. |

## Example (as JSON)

```json
{
  "id": "id4",
  "transfer_id": "transfer_id0",
  "step_sequence": 244,
  "step_type": "stablecoin_transfer",
  "from_account_asset_id": "String5",
  "from_amount": "from_amount0",
  "from_currency": "from_currency6",
  "to_account_asset_id": "String5",
  "to_amount": "to_amount6",
  "to_currency": "to_currency8",
  "transaction_hash": "String1",
  "fees": [
    {
      "fee_amount": "fee_amount2",
      "fee_currency": "fee_currency8",
      "type": "type0",
      "metadata": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "fee_amount": "fee_amount2",
      "fee_currency": "fee_currency8",
      "type": "type0",
      "metadata": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "provider_key": "alfred",
  "status": "submitted",
  "created_at": "2016-03-13T12:52:32.123Z",
  "updated_at": "2016-03-13T12:52:32.123Z"
}
```

