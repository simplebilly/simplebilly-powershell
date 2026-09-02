# DunningResult
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InvoicesProcessed** | **Int32** |  | 
**Message** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$DunningResult = Initialize-PSOpenAPIToolsDunningResult  -InvoicesProcessed null `
 -Message null
```

- Convert the resource to JSON
```powershell
$DunningResult | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

