
# Counterparty List Response

## Structure

`CounterpartyListResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Counterparty[]`](../../doc/models/counterparty.md) | Required | List of counterparties |

## Example (as JSON)

```json
{
  "data": [
    {
      "id": "id0",
      "workspace_id": "workspace_id2",
      "classification": "individual",
      "tenant_id": "String1",
      "individual_first_name": "String3",
      "individual_last_name": "String7",
      "individual_address_country": "String3",
      "individual_date_of_birth": "String7",
      "created_at": "created_at8",
      "updated_at": "updated_at6"
    }
  ]
}
```

