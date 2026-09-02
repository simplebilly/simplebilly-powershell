# ResetPasswordRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NewPassword** | **String** |  | 
**Token** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ResetPasswordRequest = Initialize-PSOpenAPIToolsResetPasswordRequest  -NewPassword null `
 -Token null
```

- Convert the resource to JSON
```powershell
$ResetPasswordRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

