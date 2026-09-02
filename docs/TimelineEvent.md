# TimelineEvent
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **String** | RFC3339 UTC timestamp for sorting. | 
**Detail** | **String** |  | [optional] 
**Id** | **String** | Source record id (stringified). | 
**Status** | **String** |  | [optional] 
**Title** | **String** |  | 
**Type** | **String** | Source module: communication | quotation | order | invoice | attachment. | 

## Examples

- Prepare the resource
```powershell
$TimelineEvent = Initialize-PSOpenAPIToolsTimelineEvent  -Date null `
 -Detail null `
 -Id null `
 -Status null `
 -Title null `
 -Type null
```

- Convert the resource to JSON
```powershell
$TimelineEvent | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

