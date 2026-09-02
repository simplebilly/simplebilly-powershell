# CartItemInput
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductId** | **String** |  | 
**Quantity** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$CartItemInput = Initialize-PSOpenAPIToolsCartItemInput  -ProductId null `
 -Quantity null
```

- Convert the resource to JSON
```powershell
$CartItemInput | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

