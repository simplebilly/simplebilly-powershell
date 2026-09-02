# ChangePasswordRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CurrentPassword** | **String** |  | 
**NewPassword** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ChangePasswordRequest = Initialize-PSOpenAPIToolsChangePasswordRequest  -CurrentPassword null `
 -NewPassword null
```

- Convert the resource to JSON
```powershell
$ChangePasswordRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

