# DpaStatus
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Accepted** | **Boolean** |  | 
**AcceptedAt** | **String** |  | [optional] 
**AcceptedBy** | **String** |  | [optional] 
**Version** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$DpaStatus = Initialize-PSOpenAPIToolsDpaStatus  -Accepted null `
 -AcceptedAt null `
 -AcceptedBy null `
 -Version null
```

- Convert the resource to JSON
```powershell
$DpaStatus | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

