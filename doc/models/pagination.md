
# Pagination

Pagination details

## Structure

`Pagination`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `number` | Required | Current page number |
| `limit` | `number` | Required | Items per page |
| `total` | `number` | Required | Total number of items |
| `totalPages` | `number` | Required | Total number of pages |
| `hasNext` | `boolean` | Required | Has next page |
| `hasPrev` | `boolean` | Required | Has previous page |

## Example (as JSON)

```json
{
  "page": 1.8,
  "limit": 128.66,
  "total": 19.52,
  "total_pages": 188.86,
  "has_next": false,
  "has_prev": false
}
```

