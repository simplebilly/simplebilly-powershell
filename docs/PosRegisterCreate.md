# PosRegisterCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **String** |  | 
**Status** | [**PosRegisterStatus**](PosRegisterStatus.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PosRegisterCreate = Initialize-PSOpenAPIToolsPosRegisterCreate  -Name null `
 -Status null
```

- Convert the resource to JSON
```powershell
$PosRegisterCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

