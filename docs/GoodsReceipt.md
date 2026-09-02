# GoodsReceipt
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GrNumber** | **String** |  | 
**LineItems** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, quantity, batch_number?, expiry_date?, bin_location?}&#x60;. | 
**Notes** | **String** |  | [optional] 
**PurchaseOrderId** | **String** | References the purchase order entity. | [optional] 
**ReceiptDate** | **System.DateTime** |  | 
**SupplierContactId** | **String** | References the supplier entity. | [optional] 
**SupplierName** | **String** |  | [optional] 
**WarehouseId** | **String** | References the warehouse entity. | 

## Examples

- Prepare the resource
```powershell
$GoodsReceipt = Initialize-PSOpenAPIToolsGoodsReceipt  -GrNumber null `
 -LineItems null `
 -Notes null `
 -PurchaseOrderId null `
 -ReceiptDate null `
 -SupplierContactId null `
 -SupplierName null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$GoodsReceipt | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

