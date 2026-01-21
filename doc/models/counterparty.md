
# Counterparty

## Structure

`Counterparty`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | Unique identifier for the counterparty. |
| `workspaceId` | `string` | Required | Workspace this counterparty belongs to. |
| `classification` | [`ClassificationEnum`](../../doc/models/classification-enum.md) | Required | Classification: 'individual' or 'business'. |
| `tenantId` | [`CounterpartyTenantId \| undefined`](../../doc/models/containers/counterparty-tenant-id.md) | Optional | This is a container for any-of cases. |
| `individualFirstName` | [`CounterpartyIndividualFirstName \| undefined`](../../doc/models/containers/counterparty-individual-first-name.md) | Optional | This is a container for any-of cases. |
| `individualLastName` | [`CounterpartyIndividualLastName \| undefined`](../../doc/models/containers/counterparty-individual-last-name.md) | Optional | This is a container for any-of cases. |
| `individualAddressCountry` | [`CounterpartyIndividualAddressCountry \| undefined`](../../doc/models/containers/counterparty-individual-address-country.md) | Optional | This is a container for any-of cases. |
| `individualDateOfBirth` | [`CounterpartyIndividualDateOfBirth \| undefined`](../../doc/models/containers/counterparty-individual-date-of-birth.md) | Optional | This is a container for any-of cases. |
| `individualNationalIdentificationNumber` | [`CounterpartyIndividualNationalIdentificationNumber \| undefined`](../../doc/models/containers/counterparty-individual-national-identification-number.md) | Optional | This is a container for any-of cases. |
| `individualStreetAddress1` | [`CounterpartyIndividualStreetAddress1 \| undefined`](../../doc/models/containers/counterparty-individual-street-address-1.md) | Optional | This is a container for any-of cases. |
| `individualStreetAddress2` | [`CounterpartyIndividualStreetAddress2 \| undefined`](../../doc/models/containers/counterparty-individual-street-address-2.md) | Optional | This is a container for any-of cases. |
| `individualCity` | [`CounterpartyIndividualCity \| undefined`](../../doc/models/containers/counterparty-individual-city.md) | Optional | This is a container for any-of cases. |
| `individualState` | [`CounterpartyIndividualState \| undefined`](../../doc/models/containers/counterparty-individual-state.md) | Optional | This is a container for any-of cases. |
| `individualPostalCode` | [`CounterpartyIndividualPostalCode \| undefined`](../../doc/models/containers/counterparty-individual-postal-code.md) | Optional | This is a container for any-of cases. |
| `businessLegalName` | [`CounterpartyBusinessLegalName \| undefined`](../../doc/models/containers/counterparty-business-legal-name.md) | Optional | This is a container for any-of cases. |
| `businessDba` | [`CounterpartyBusinessDba \| undefined`](../../doc/models/containers/counterparty-business-dba.md) | Optional | This is a container for any-of cases. |
| `businessAddressCountry` | [`CounterpartyBusinessAddressCountry \| undefined`](../../doc/models/containers/counterparty-business-address-country.md) | Optional | This is a container for any-of cases. |
| `businessStreetAddress1` | [`CounterpartyBusinessStreetAddress1 \| undefined`](../../doc/models/containers/counterparty-business-street-address-1.md) | Optional | This is a container for any-of cases. |
| `businessStreetAddress2` | [`CounterpartyBusinessStreetAddress2 \| undefined`](../../doc/models/containers/counterparty-business-street-address-2.md) | Optional | This is a container for any-of cases. |
| `businessCity` | [`CounterpartyBusinessCity \| undefined`](../../doc/models/containers/counterparty-business-city.md) | Optional | This is a container for any-of cases. |
| `businessState` | [`CounterpartyBusinessState \| undefined`](../../doc/models/containers/counterparty-business-state.md) | Optional | This is a container for any-of cases. |
| `businessLegalEntityIdentifier` | [`CounterpartyBusinessLegalEntityIdentifier \| undefined`](../../doc/models/containers/counterparty-business-legal-entity-identifier.md) | Optional | This is a container for any-of cases. |
| `createdAt` | `string` | Required | Creation timestamp in ISO 8601 format. |
| `updatedAt` | `string` | Required | Last update timestamp in ISO 8601 format. |

## Example (as JSON)

```json
{
  "id": "id2",
  "workspace_id": "workspace_id4",
  "classification": "individual",
  "tenant_id": "String3",
  "individual_first_name": "String7",
  "individual_last_name": "String3",
  "individual_address_country": "String7",
  "individual_date_of_birth": "String9",
  "created_at": "created_at0",
  "updated_at": "updated_at2"
}
```

