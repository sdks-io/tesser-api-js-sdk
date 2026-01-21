
# Update Counterparty Request

## Structure

`UpdateCounterpartyRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `classification` | [`ClassificationEnum \| undefined`](../../doc/models/classification-enum.md) | Optional | Classification: 'individual' or 'business'. |
| `tenantId` | [`UpdateCounterpartyRequestTenantId \| undefined`](../../doc/models/containers/update-counterparty-request-tenant-id.md) | Optional | This is a container for any-of cases. |
| `individualFirstName` | [`UpdateCounterpartyRequestIndividualFirstName \| undefined`](../../doc/models/containers/update-counterparty-request-individual-first-name.md) | Optional | This is a container for any-of cases. |
| `individualLastName` | [`UpdateCounterpartyRequestIndividualLastName \| undefined`](../../doc/models/containers/update-counterparty-request-individual-last-name.md) | Optional | This is a container for any-of cases. |
| `individualAddressCountry` | [`UpdateCounterpartyRequestIndividualAddressCountry \| undefined`](../../doc/models/containers/update-counterparty-request-individual-address-country.md) | Optional | This is a container for any-of cases. |
| `businessLegalName` | [`UpdateCounterpartyRequestBusinessLegalName \| undefined`](../../doc/models/containers/update-counterparty-request-business-legal-name.md) | Optional | This is a container for any-of cases. |
| `businessDba` | [`UpdateCounterpartyRequestBusinessDba \| undefined`](../../doc/models/containers/update-counterparty-request-business-dba.md) | Optional | This is a container for any-of cases. |
| `businessAddressCountry` | [`UpdateCounterpartyRequestBusinessAddressCountry \| undefined`](../../doc/models/containers/update-counterparty-request-business-address-country.md) | Optional | This is a container for any-of cases. |

## Example (as JSON)

```json
{
  "classification": "individual",
  "tenant_id": "00001eca-0000-0000-0000-000000000000",
  "individual_first_name": "String1",
  "individual_last_name": "String5",
  "individual_address_country": "String1"
}
```

