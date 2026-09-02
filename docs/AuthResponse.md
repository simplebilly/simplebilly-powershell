# AuthResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccessToken** | **String** |  | [optional] 
**Message** | **String** |  | [optional] 
**RefreshToken** | **String** |  | [optional] 
**Success** | **Boolean** |  | 
**User** | [**Model**](Model.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$AuthResponse = Initialize-PSOpenAPIToolsAuthResponse  -AccessToken null `
 -Message null `
 -RefreshToken null `
 -Success null `
 -User null
```

- Convert the resource to JSON
```powershell
$AuthResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

