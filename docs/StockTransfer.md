# StockTransfer
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LineItems** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, quantity, batch_number?}&#x60;. | 
**Notes** | **String** |  | [optional] 
**SourceWarehouseId** | **String** | References the warehouse entity. | 
**Status** | [**StockTransferStatus**](StockTransferStatus.md) | One of: draft | completed | cancelled | 
**TargetWarehouseId** | **String** | References the warehouse entity. | 
**TransferDate** | **System.DateTime** |  | 
**TransferNumber** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$StockTransfer = Initialize-PSOpenAPIToolsStockTransfer  -LineItems null `
 -Notes null `
 -SourceWarehouseId null `
 -Status null `
 -TargetWarehouseId null `
 -TransferDate null `
 -TransferNumber null
```

- Convert the resource to JSON
```powershell
$StockTransfer | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

