# SendMessageDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **String** |  | 
**IsInternal** | **Boolean** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$SendMessageDto = Initialize-PSOpenAPIToolsSendMessageDto  -Body null `
 -IsInternal null
```

- Convert the resource to JSON
```powershell
$SendMessageDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

