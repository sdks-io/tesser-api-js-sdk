
# Payment Response

## Structure

`PaymentResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Data6`](../../doc/models/data-6.md) | Required | - |

## Example (as JSON)

```json
{
  "data": {
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
}
```

