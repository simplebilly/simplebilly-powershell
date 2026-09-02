# BilanzItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **String** |  | 
**Konto** | **String** |  | 
**Name** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$BilanzItem = Initialize-PSOpenAPIToolsBilanzItem  -Amount null `
 -Konto null `
 -Name null
```

- Convert the resource to JSON
```powershell
$BilanzItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

