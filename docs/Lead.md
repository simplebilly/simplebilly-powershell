# Lead
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Company** | **String** |  | [optional] 
**ConvertedAt** | **System.DateTime** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | 
**Email** | **String** |  | [optional] 
**FirstContactAt** | **System.DateTime** |  | 
**Name** | **String** |  | 
**Notes** | **String** |  | [optional] 
**Phone** | **String** |  | [optional] 
**Score** | **Int32** |  | 
**Source** | **String** |  | 
**Status** | [**LeadStatus**](LeadStatus.md) |  | 
**Tags** | [**AnyType**](.md) |  | 
**TenantId** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Lead = Initialize-PSOpenAPIToolsLead  -Company null `
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
$Lead | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

