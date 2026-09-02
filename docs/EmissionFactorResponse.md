# EmissionFactorResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CategoryId** | **String** |  | 
**KgCo2ePerUnit** | **Double** |  | 
**NameDe** | **String** |  | 
**Source** | **String** |  | 
**Unit** | **String** |  | 
**Version** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$EmissionFactorResponse = Initialize-PSOpenAPIToolsEmissionFactorResponse  -CategoryId null `
 -KgCo2ePerUnit null `
 -NameDe null `
 -Source null `
 -Unit null `
 -Version null
```

- Convert the resource to JSON
```powershell
$EmissionFactorResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

