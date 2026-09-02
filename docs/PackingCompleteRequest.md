# PackingCompleteRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Notes** | **String** |  | [optional] 
**OrderNumber** | **String** |  | 
**ShipmentId** | **String** |  | [optional] 
**VideoUrl** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PackingCompleteRequest = Initialize-PSOpenAPIToolsPackingCompleteRequest  -Notes null `
 -OrderNumber null `
 -ShipmentId null `
 -VideoUrl null
```

- Convert the resource to JSON
```powershell
$PackingCompleteRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

