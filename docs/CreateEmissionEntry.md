# CreateEmissionEntry
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityValue** | **String** |  | 
**CategoryId** | **String** |  | 
**Description** | **String** |  | 
**Method** | **String** |  | 
**Scope** | **String** |  | 
**Unit** | **String** |  | 
**Year** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$CreateEmissionEntry = Initialize-PSOpenAPIToolsCreateEmissionEntry  -ActivityValue null `
 -CategoryId null `
 -Description null `
 -Method null `
 -Scope null `
 -Unit null `
 -Year null
```

- Convert the resource to JSON
```powershell
$CreateEmissionEntry | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

