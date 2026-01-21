
# Tenant

## Structure

`Tenant`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the tenant |
| `workspaceId` | `string` | Required | Workspace ID the tenant belongs to |
| `businessLegalName` | [`TenantBusinessLegalName`](../../doc/models/containers/tenant-business-legal-name.md) | Required | This is a container for any-of cases. |
| `businessDba` | [`TenantBusinessDba`](../../doc/models/containers/tenant-business-dba.md) | Required | This is a container for any-of cases. |
| `businessAddressCountry` | [`TenantBusinessAddressCountry`](../../doc/models/containers/tenant-business-address-country.md) | Required | This is a container for any-of cases. |
| `businessStreetAddress1` | [`TenantBusinessStreetAddress1`](../../doc/models/containers/tenant-business-street-address-1.md) | Required | This is a container for any-of cases. |
| `businessStreetAddress2` | [`TenantBusinessStreetAddress2`](../../doc/models/containers/tenant-business-street-address-2.md) | Required | This is a container for any-of cases. |
| `businessCity` | [`TenantBusinessCity`](../../doc/models/containers/tenant-business-city.md) | Required | This is a container for any-of cases. |
| `businessState` | [`TenantBusinessState`](../../doc/models/containers/tenant-business-state.md) | Required | This is a container for any-of cases. |
| `businessLegalEntityIdentifier` | [`TenantBusinessLegalEntityIdentifier`](../../doc/models/containers/tenant-business-legal-entity-identifier.md) | Required | This is a container for any-of cases. |
| `country` | [`TenantCountry`](../../doc/models/containers/tenant-country.md) | Required | This is a container for any-of cases. |
| `webhookUrl` | [`TenantWebhookUrl`](../../doc/models/containers/tenant-webhook-url.md) | Required | This is a container for any-of cases. |
| `createdAt` | `string` | Required | Creation timestamp in ISO 8601 format |
| `updatedAt` | `string` | Required | Last update timestamp in ISO 8601 format |

## Example (as JSON)

```json
{
  "id": "id0",
  "workspace_id": "workspace_id2",
  "business_legal_name": "String7",
  "business_dba": "String7",
  "business_address_country": "String9",
  "business_street_address1": "String7",
  "business_street_address2": "String3",
  "business_city": "String3",
  "business_state": "String7",
  "business_legal_entity_identifier": "String3",
  "country": "String5",
  "webhook_url": "String3",
  "created_at": "created_at8",
  "updated_at": "updated_at6"
}
```

