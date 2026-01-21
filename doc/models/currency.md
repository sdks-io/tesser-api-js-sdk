
# Currency

## Structure

`Currency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | Display name for the currency (e.g., 'Circle USD') |
| `key` | `string` | Required | Currency code/key (e.g., 'USDC', 'USD') |
| `decimals` | `number` | Required | Number of decimal places for the currency |
| `network` | [`CurrencyNetwork`](../../doc/models/containers/currency-network.md) | Required | This is a container for any-of cases. |

## Example (as JSON)

```json
{
  "name": "name8",
  "key": "key8",
  "decimals": 116.22,
  "network": "String5"
}
```

