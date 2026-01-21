
# Create Tenant Request

## Structure

`CreateTenantRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `businessLegalName` | `string` | Required | Legal name of the business tenant.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `businessDba` | [`CreateTenantRequestBusinessDba \| undefined`](../../doc/models/containers/create-tenant-request-business-dba.md) | Optional | This is a container for any-of cases. |
| `businessAddressCountry` | [`CreateTenantRequestBusinessAddressCountry \| undefined`](../../doc/models/containers/create-tenant-request-business-address-country.md) | Optional | This is a container for any-of cases. |
| `businessStreetAddress1` | [`CreateTenantRequestBusinessStreetAddress1 \| undefined`](../../doc/models/containers/create-tenant-request-business-street-address-1.md) | Optional | This is a container for any-of cases. |
| `businessStreetAddress2` | [`CreateTenantRequestBusinessStreetAddress2 \| undefined`](../../doc/models/containers/create-tenant-request-business-street-address-2.md) | Optional | This is a container for any-of cases. |
| `businessCity` | [`CreateTenantRequestBusinessCity \| undefined`](../../doc/models/containers/create-tenant-request-business-city.md) | Optional | This is a container for any-of cases. |
| `businessState` | [`CreateTenantRequestBusinessState \| undefined`](../../doc/models/containers/create-tenant-request-business-state.md) | Optional | This is a container for any-of cases. |
| `businessLegalEntityIdentifier` | [`CreateTenantRequestBusinessLegalEntityIdentifier \| undefined`](../../doc/models/containers/create-tenant-request-business-legal-entity-identifier.md) | Optional | This is a container for any-of cases. |
| `webhookUrl` | [`CreateTenantRequestWebhookUrl \| undefined`](../../doc/models/containers/create-tenant-request-webhook-url.md) | Optional | This is a container for any-of cases. |

## Example (as JSON)

```json
{
  "business_legal_name": "business_legal_name2",
  "webhook_url": "https://acme.com/webhooks/tesser",
  "business_dba": "String3",
  "business_address_country": "String9",
  "business_street_address1": "String3",
  "business_street_address2": "String7",
  "business_city": "String9"
}
```

