# UpdateRolePayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Role** | **String** |  | 
**SyncPermissions** | **Boolean** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$UpdateRolePayload = Initialize-PSOpenAPIToolsUpdateRolePayload  -Role null `
 -SyncPermissions null
```

- Convert the resource to JSON
```powershell
$UpdateRolePayload | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

