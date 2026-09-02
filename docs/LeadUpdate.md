# LeadUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Company** | **String** |  | [optional] 
**ConvertedAt** | **System.DateTime** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | [optional] 
**Email** | **String** |  | [optional] 
**FirstContactAt** | **System.DateTime** |  | [optional] 
**Name** | **String** |  | [optional] 
**Notes** | **String** |  | [optional] 
**Phone** | **String** |  | [optional] 
**Score** | **Int32** |  | [optional] 
**Source** | **String** |  | [optional] 
**Status** | [**LeadStatus**](LeadStatus.md) |  | [optional] 
**Tags** | [**AnyType**](.md) |  | [optional] 
**TenantId** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$LeadUpdate = Initialize-PSOpenAPIToolsLeadUpdate  -Company null `
 -ConvertedAt null `
 -CreatedAt null `
 -Email null `
 -FirstContactAt null `
 -Name null `
 -Notes null `
 -Phone null `
 -Score null `
 -Source null `
 -Status null `
 -Tags null `
 -TenantId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$LeadUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

