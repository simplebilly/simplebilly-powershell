# PlanLimits
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MaxConnectors** | **Int32** |  | 
**MaxInvoicesPerMonth** | **Int64** |  | 
**MaxUsers** | **Int32** |  | 
**Metered** | **System.Collections.Hashtable** |  | [optional] 
**PaidConnectors** | **String[]** | Connectors that are *not* included in this plan (require a higher tier). Empty &#x3D; all connectors included on this plan. | 

## Examples

- Prepare the resource
```powershell
$PlanLimits = Initialize-PSOpenAPIToolsPlanLimits  -MaxConnectors null `
 -MaxInvoicesPerMonth null `
 -MaxUsers null `
 -Metered null `
 -PaidConnectors null
```

- Convert the resource to JSON
```powershell
$PlanLimits | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

