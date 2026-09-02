# PeppolResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Content** | **String** |  | 
**ContentType** | **String** |  | 
**Filename** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PeppolResponse = Initialize-PSOpenAPIToolsPeppolResponse  -Content null `
 -ContentType null `
 -Filename null
```

- Convert the resource to JSON
```powershell
$PeppolResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

