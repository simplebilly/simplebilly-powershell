# Team
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**Description** | **String** |  | [optional] 
**Id** | **String** |  | 
**Name** | **String** |  | 
**ParentTeamId** | **String** |  | [optional] 
**TenantId** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | 

## Examples

- Prepare the resource
```powershell
$Team = Initialize-PSOpenAPIToolsTeam  -CreatedAt null `
 -Description null `
 -Id null `
 -Name null `
 -ParentTeamId null `
 -TenantId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$Team | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

