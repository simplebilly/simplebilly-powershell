# PayrollMonth
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gross** | **String** |  | 
**Month** | **Int32** |  | 
**Net** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PayrollMonth = Initialize-PSOpenAPIToolsPayrollMonth  -Gross null `
 -Month null `
 -Net null
```

- Convert the resource to JSON
```powershell
$PayrollMonth | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

