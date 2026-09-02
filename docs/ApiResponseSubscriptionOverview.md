# ApiResponseSubscriptionOverview
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**VarData** | [**ApiResponseSubscriptionOverviewData**](ApiResponseSubscriptionOverviewData.md) |  | [optional] 
**VarError** | **String** |  | [optional] 
**Message** | **String** |  | [optional] 
**Success** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$ApiResponseSubscriptionOverview = Initialize-PSOpenAPIToolsApiResponseSubscriptionOverview  -VarData null `
 -VarError null `
 -Message null `
 -Success null
```

- Convert the resource to JSON
```powershell
$ApiResponseSubscriptionOverview | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

