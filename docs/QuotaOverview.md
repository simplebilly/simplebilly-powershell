# QuotaOverview
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Features** | [**PlanFeatures**](PlanFeatures.md) |  | 
**IsTrialing** | **Boolean** |  | 
**Limits** | [**PlanLimits**](PlanLimits.md) |  | 
**Metered** | [**MeteredUsage[]**](MeteredUsage.md) |  | 
**Plan** | **String** |  | 
**PlanName** | **String** |  | 
**TrialEndsAt** | **System.DateTime** |  | [optional] 
**Usage** | [**UsageSnapshot**](UsageSnapshot.md) |  | 

## Examples

- Prepare the resource
```powershell
$QuotaOverview = Initialize-PSOpenAPIToolsQuotaOverview  -Features null `
 -IsTrialing null `
 -Limits null `
 -Metered null `
 -Plan null `
 -PlanName null `
 -TrialEndsAt null `
 -Usage null
```

- Convert the resource to JSON
```powershell
$QuotaOverview | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

