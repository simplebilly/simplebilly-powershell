# TeamCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **String** |  | [optional] 
**Name** | **String** |  | 
**ParentTeamId** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$TeamCreate = Initialize-PSOpenAPIToolsTeamCreate  -Description null `
 -Name null `
 -ParentTeamId null
```

- Convert the resource to JSON
```powershell
$TeamCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

