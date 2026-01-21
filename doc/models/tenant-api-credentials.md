
# Tenant Api Credentials

## Structure

`TenantApiCredentials`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientId` | `string` | Required | Auth0 M2M Client ID |
| `clientSecret` | `string` | Required | Auth0 M2M Client Secret (only shown once!) |
| `tokenEndpoint` | `string` | Required | Auth0 token endpoint URL |
| `audience` | `string` | Required | API audience for token requests |

## Example (as JSON)

```json
{
  "client_id": "client_id8",
  "client_secret": "client_secret4",
  "token_endpoint": "token_endpoint8",
  "audience": "audience2"
}
```

