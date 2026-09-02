# SupportChannel
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelType** | [**SupportChannelType**](SupportChannelType.md) |  | 
**Config** | [**AnyType**](.md) |  | 
**CreatedAt** | **System.DateTime** |  | 
**IsActive** | **Boolean** |  | 
**Name** | **String** |  | 
**TenantId** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$SupportChannel = Initialize-PSOpenAPIToolsSupportChannel  -ChannelType null `
 -Config null `
 -CreatedAt null `
 -IsActive null `
 -Name null `
 -TenantId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$SupportChannel | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

