# ApiResponseString
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**VarData** | **String** |  | [optional] 
**VarError** | **String** |  | [optional] 
**Message** | **String** |  | [optional] 
**Success** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$ApiResponseString = Initialize-PSOpenAPIToolsApiResponseString  -VarData null `
 -VarError null `
 -Message null `
 -Success null
```

- Convert the resource to JSON
```powershell
$ApiResponseString | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

