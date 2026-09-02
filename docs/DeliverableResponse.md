# DeliverableResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvailableStock** | **Int64** |  | 
**DeliverableQuantity** | **Int64** |  | 
**MaxSellable** | **Int64** |  | [optional] 
**ProductId** | **String** |  | 
**ReservedStock** | **Int64** |  | 
**WarehouseId** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$DeliverableResponse = Initialize-PSOpenAPIToolsDeliverableResponse  -AvailableStock null `
 -DeliverableQuantity null `
 -MaxSellable null `
 -ProductId null `
 -ReservedStock null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$DeliverableResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

