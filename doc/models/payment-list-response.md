
# Payment List Response

## Structure

`PaymentListResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Data7[]`](../../doc/models/data-7.md) | Required | - |
| `pagination` | [`Pagination \| undefined`](../../doc/models/pagination.md) | Optional | Pagination details |

## Example (as JSON)

```json
{
  "data": [
    {
      "id": "id0",
      "workspace_id": "workspace_id2",
      "organization_reference_id": "String9",
      "direction": "internal",
      "payment_type": "withdrawal",
      "source_account_id": "String9",
      "originator_account_id": "String1",
      "beneficiary_account_id": "String7",
      "from_amount": "from_amount6",
      "from_currency": "from_currency2",
      "from_network": "String9",
      "to_amount": "to_amount2",
      "to_currency": "to_currency4",
      "risk_status": "approved",
      "created_at": "2016-03-13T12:52:32.123Z",
      "updated_at": "2016-03-13T12:52:32.123Z",
      "expires_at": "2016-03-13T12:52:32.123Z"
    }
  ],
  "pagination": {
    "page": 17.58,
    "limit": 146.72,
    "total": 255.86,
    "total_pages": 208.24,
    "has_next": false,
    "has_prev": false
  }
}
```

