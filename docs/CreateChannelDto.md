# CreateChannelDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelType** | **String** |  | 
**Config** | [**AnyType**](.md) |  | 
**Name** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$CreateChannelDto = Initialize-PSOpenAPIToolsCreateChannelDto  -ChannelType null `
 -Config null `
 -Name null
```

- Convert the resource to JSON
```powershell
$CreateChannelDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

