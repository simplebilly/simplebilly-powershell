# LaborCostRow
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Cost** | **String** |  | 
**EmployeeId** | **String** |  | [optional] 
**GroupKey** | **String** |  | 
**Hours** | **String** |  | 
**Name** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$LaborCostRow = Initialize-PSOpenAPIToolsLaborCostRow  -Cost null `
 -EmployeeId null `
 -GroupKey null `
 -Hours null `
 -Name null
```

- Convert the resource to JSON
```powershell
$LaborCostRow | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

