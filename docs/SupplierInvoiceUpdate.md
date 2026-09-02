# SupplierInvoiceUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **String** |  | [optional] 
**GoodsReceiptId** | **String** | References the goods receipt entity. | [optional] 
**InvoiceDate** | **System.DateTime** |  | [optional] 
**InvoiceNumber** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, quantity, unitPriceNet, taxRate}&#x60;. | [optional] 
**Notes** | **String** |  | [optional] 
**PurchaseOrderId** | **String** | References the purchase order entity. | [optional] 
**Status** | [**SupplierInvoiceStatus**](SupplierInvoiceStatus.md) | One of: draft | matched | has_variances | posted | cancelled | [optional] 
**SupplierContactId** | **String** | References the supplier entity. | [optional] 
**SupplierName** | **String** |  | [optional] 
**TotalGrossAmount** | **String** |  | [optional] 
**TotalNetAmount** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$SupplierInvoiceUpdate = Initialize-PSOpenAPIToolsSupplierInvoiceUpdate  -Currency null `
 -GoodsReceiptId null `
 -InvoiceDate null `
 -InvoiceNumber null `
 -LineItems null `
 -Notes null `
 -PurchaseOrderId null `
 -Status null `
 -SupplierContactId null `
 -SupplierName null `
 -TotalGrossAmount null `
 -TotalNetAmount null
```

- Convert the resource to JSON
```powershell
$SupplierInvoiceUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

