# DataQuality
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityLines** | **Int32** |  | 
**ActivitySharePct** | **Double** |  | 
**SpendLines** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$DataQuality = Initialize-PSOpenAPIToolsDataQuality  -ActivityLines null `
 -ActivitySharePct null `
 -SpendLines null
```

- Convert the resource to JSON
```powershell
$DataQuality | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

