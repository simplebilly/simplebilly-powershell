# EmitEventRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventType** | **String** |  | 
**Payload** | [**AnyType**](.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$EmitEventRequest = Initialize-PSOpenAPIToolsEmitEventRequest  -EventType null `
 -Payload null
```

- Convert the resource to JSON
```powershell
$EmitEventRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

