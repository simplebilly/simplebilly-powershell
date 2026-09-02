# UpdateChannelDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Config** | [**AnyType**](.md) |  | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**Name** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$UpdateChannelDto = Initialize-PSOpenAPIToolsUpdateChannelDto  -Config null `
 -IsActive null `
 -Name null
```

- Convert the resource to JSON
```powershell
$UpdateChannelDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

