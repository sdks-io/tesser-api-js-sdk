
# Create Counterparty Request

## Structure

`CreateCounterpartyRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `classification` | [`ClassificationEnum`](../../doc/models/classification-enum.md) | Required | Classification: 'individual' or 'business'. |
| `tenantId` | [`CreateCounterpartyRequestTenantId \| undefined`](../../doc/models/containers/create-counterparty-request-tenant-id.md) | Optional | This is a container for any-of cases. |
| `individualFirstName` | [`CreateCounterpartyRequestIndividualFirstName \| undefined`](../../doc/models/containers/create-counterparty-request-individual-first-name.md) | Optional | This is a container for any-of cases. |
| `individualLastName` | [`CreateCounterpartyRequestIndividualLastName \| undefined`](../../doc/models/containers/create-counterparty-request-individual-last-name.md) | Optional | This is a container for any-of cases. |
| `individualAddressCountry` | [`CreateCounterpartyRequestIndividualAddressCountry \| undefined`](../../doc/models/containers/create-counterparty-request-individual-address-country.md) | Optional | This is a container for any-of cases. |
| `individualDateOfBirth` | [`CreateCounterpartyRequestIndividualDateOfBirth \| undefined`](../../doc/models/containers/create-counterparty-request-individual-date-of-birth.md) | Optional | This is a container for any-of cases. |
| `individualNationalIdentificationNumber` | [`CreateCounterpartyRequestIndividualNationalIdentificationNumber \| undefined`](../../doc/models/containers/create-counterparty-request-individual-national-identification-number.md) | Optional | This is a container for any-of cases. |
| `individualStreetAddress1` | [`CreateCounterpartyRequestIndividualStreetAddress1 \| undefined`](../../doc/models/containers/create-counterparty-request-individual-street-address-1.md) | Optional | This is a container for any-of cases. |
| `individualStreetAddress2` | [`CreateCounterpartyRequestIndividualStreetAddress2 \| undefined`](../../doc/models/containers/create-counterparty-request-individual-street-address-2.md) | Optional | This is a container for any-of cases. |
| `individualCity` | [`CreateCounterpartyRequestIndividualCity \| undefined`](../../doc/models/containers/create-counterparty-request-individual-city.md) | Optional | This is a container for any-of cases. |
| `individualState` | [`CreateCounterpartyRequestIndividualState \| undefined`](../../doc/models/containers/create-counterparty-request-individual-state.md) | Optional | This is a container for any-of cases. |
| `individualPostalCode` | [`CreateCounterpartyRequestIndividualPostalCode \| undefined`](../../doc/models/containers/create-counterparty-request-individual-postal-code.md) | Optional | This is a container for any-of cases. |
| `businessLegalName` | [`CreateCounterpartyRequestBusinessLegalName \| undefined`](../../doc/models/containers/create-counterparty-request-business-legal-name.md) | Optional | This is a container for any-of cases. |
| `businessDba` | [`CreateCounterpartyRequestBusinessDba \| undefined`](../../doc/models/containers/create-counterparty-request-business-dba.md) | Optional | This is a container for any-of cases. |
| `businessAddressCountry` | [`CreateCounterpartyRequestBusinessAddressCountry \| undefined`](../../doc/models/containers/create-counterparty-request-business-address-country.md) | Optional | This is a container for any-of cases. |
| `businessStreetAddress1` | [`CreateCounterpartyRequestBusinessStreetAddress1 \| undefined`](../../doc/models/containers/create-counterparty-request-business-street-address-1.md) | Optional | This is a container for any-of cases. |
| `businessStreetAddress2` | [`CreateCounterpartyRequestBusinessStreetAddress2 \| undefined`](../../doc/models/containers/create-counterparty-request-business-street-address-2.md) | Optional | This is a container for any-of cases. |
| `businessCity` | [`CreateCounterpartyRequestBusinessCity \| undefined`](../../doc/models/containers/create-counterparty-request-business-city.md) | Optional | This is a container for any-of cases. |
| `businessState` | [`CreateCounterpartyRequestBusinessState \| undefined`](../../doc/models/containers/create-counterparty-request-business-state.md) | Optional | This is a container for any-of cases. |
| `businessLegalEntityIdentifier` | [`CreateCounterpartyRequestBusinessLegalEntityIdentifier \| undefined`](../../doc/models/containers/create-counterparty-request-business-legal-entity-identifier.md) | Optional | This is a container for any-of cases. |

## Example (as JSON)

```json
{
  "classification": "individual",
  "tenant_id": "0000073e-0000-0000-0000-000000000000",
  "individual_first_name": "String3",
  "individual_last_name": "String7",
  "individual_address_country": "String3",
  "individual_date_of_birth": "String7"
}
```

