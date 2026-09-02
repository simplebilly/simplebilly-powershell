# ReturnOrder
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerContactId** | **String** | References the contact entity. | [optional] 
**CustomerName** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, quantity, condition, restock, batch_number?}&#x60;. | [optional] 
**Notes** | **String** |  | [optional] 
**OrderId** | **String** | References the order entity. | [optional] 
**OrderNumber** | **String** |  | [optional] 
**ReturnNumber** | **String** |  | 
**ReturnReason** | **String** |  | [optional] 
**Status** | [**ReturnOrderStatus**](ReturnOrderStatus.md) | One of: requested | received | inspected | restocked | closed | 
**WarehouseId** | **String** | Warehouse into which restockable items are returned. References the warehouse entity. | [optional] 

## Examples

- Prepare the resource
```powershell
$ReturnOrder = Initialize-PSOpenAPIToolsReturnOrder  -CustomerContactId null `
 -CustomerName null `
 -LineItems null `
 -Notes null `
 -OrderId null `
 -OrderNumber null `
 -ReturnNumber null `
 -ReturnReason null `
 -Status null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$ReturnOrder | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

