# PrintLabelResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LabelUrl** | **String** |  | [optional] 
**Message** | **String** |  | 
**Sscc** | **String** |  | [optional] 
**Success** | **Boolean** |  | 
**TrackingNumber** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PrintLabelResponse = Initialize-PSOpenAPIToolsPrintLabelResponse  -LabelUrl null `
 -Message null `
 -Sscc null `
 -Success null `
 -TrackingNumber null
```

- Convert the resource to JSON
```powershell
$PrintLabelResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

