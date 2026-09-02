# OrderStateUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SendStateToShop** | **Boolean** |  | [optional] 
**State** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$OrderStateUpdate = Initialize-PSOpenAPIToolsOrderStateUpdate  -SendStateToShop null `
 -State null
```

- Convert the resource to JSON
```powershell
$OrderStateUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

