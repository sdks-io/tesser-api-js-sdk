
# Update Tenant Request

## Structure

`UpdateTenantRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `businessLegalName` | `string \| undefined` | Optional | Updated legal business name.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `businessDba` | [`UpdateTenantRequestBusinessDba \| undefined`](../../doc/models/containers/update-tenant-request-business-dba.md) | Optional | This is a container for any-of cases. |
| `businessAddressCountry` | [`UpdateTenantRequestBusinessAddressCountry \| undefined`](../../doc/models/containers/update-tenant-request-business-address-country.md) | Optional | This is a container for any-of cases. |
| `webhookUrl` | [`UpdateTenantRequestWebhookUrl \| undefined`](../../doc/models/containers/update-tenant-request-webhook-url.md) | Optional | This is a container for any-of cases. |

## Example (as JSON)

```json
{
  "business_legal_name": "business_legal_name0",
  "business_dba": "String1",
  "business_address_country": "String7",
  "webhook_url": "String7"
}
```

