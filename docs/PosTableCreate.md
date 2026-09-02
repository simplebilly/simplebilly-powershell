# PosTableCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CurrentOrderNumber** | **String** |  | [optional] 
**Name** | **String** |  | 
**Status** | [**PosTableStatus**](PosTableStatus.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PosTableCreate = Initialize-PSOpenAPIToolsPosTableCreate  -CurrentOrderNumber null `
 -Name null `
 -Status null
```

- Convert the resource to JSON
```powershell
$PosTableCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

