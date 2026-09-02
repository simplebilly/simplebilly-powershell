# ApiResponseSubscriptionOverviewData
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CurrentPeriodEnd** | **System.DateTime** |  | [optional] 
**Features** | [**PlanFeatures**](PlanFeatures.md) |  | 
**IsTrialing** | **Boolean** |  | 
**Limits** | [**PlanLimits**](PlanLimits.md) |  | 
**ManageUrl** | **String** |  | [optional] 
**Plan** | **String** | Resolved plan id (free/starter/business/enterprise, or a custom override id). | 
**PlanName** | **String** |  | 
**PriceEur** | **Double** | Monthly price in EUR; &#x60;-1.0&#x60; &#x3D; custom pricing (enterprise). | 
**Quantity** | **Int32** |  | [optional] 
**Status** | **String** |  | [optional] 
**SubscriptionId** | **String** |  | [optional] 
**TrialEndsAt** | **System.DateTime** |  | [optional] 
**Usage** | [**UsageSnapshot**](UsageSnapshot.md) |  | 

## Examples

- Prepare the resource
```powershell
$ApiResponseSubscriptionOverviewData = Initialize-PSOpenAPIToolsApiResponseSubscriptionOverviewData  -CurrentPeriodEnd null `
 -Features null `
 -IsTrialing null `
 -Limits null `
 -ManageUrl null `
 -Plan null `
 -PlanName null `
 -PriceEur null `
 -Quantity null `
 -Status null `
 -SubscriptionId null `
 -TrialEndsAt null `
 -Usage null
```

- Convert the resource to JSON
```powershell
$ApiResponseSubscriptionOverviewData | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

