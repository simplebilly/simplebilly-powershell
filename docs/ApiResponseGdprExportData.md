# ApiResponseGdprExportData
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityLog** | [**GdprActivity[]**](GdprActivity.md) |  | 
**ApiKeys** | [**GdprApiKey[]**](GdprApiKey.md) | Key identifiers and names only — never a usable credential. | 
**Billing** | [**GdprBillingInfo[]**](GdprBillingInfo.md) |  | 
**ExportedAt** | **System.DateTime** |  | 
**GeneratedByAi** | **Boolean** | Honesty field: this document is a plain data dump, never AI-generated. | 
**Notifications** | [**GdprNotification[]**](GdprNotification.md) |  | 
**RefreshTokens** | [**GdprRefreshToken[]**](GdprRefreshToken.md) | Session records: metadata only, never the token hash. | 
**Tenants** | [**GdprTenant[]**](GdprTenant.md) |  | 
**UsageEvents** | [**GdprUsageEvent[]**](GdprUsageEvent.md) |  | 
**User** | [**GdprUser**](GdprUser.md) |  | 

## Examples

- Prepare the resource
```powershell
$ApiResponseGdprExportData = Initialize-PSOpenAPIToolsApiResponseGdprExportData  -ActivityLog null `
 -ApiKeys null `
 -Billing null `
 -ExportedAt null `
 -GeneratedByAi null `
 -Notifications null `
 -RefreshTokens null `
 -Tenants null `
 -UsageEvents null `
 -User null
```

- Convert the resource to JSON
```powershell
$ApiResponseGdprExportData | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

