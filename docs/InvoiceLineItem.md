# InvoiceLineItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ArticleNumber** | **String** |  | [optional] 
**Description** | **String** |  | 
**DiscountAmount** | **String** |  | [optional] 
**DiscountPercentage** | **String** |  | [optional] 
**InputVatDeductible** | **Boolean** |  | [optional] 
**InputVatRate** | **String** |  | [optional] 
**IsIntraCommunityAcquisition** | **Boolean** |  | [optional] 
**IsMargin25a** | **Boolean** |  | [optional] 
**LedgerAccount** | **String** |  | [optional] 
**LineTotal** | **String** |  | 
**LineTotalGross** | **String** |  | [optional] 
**Margin25aPurchasePrice** | **String** |  | [optional] 
**MeterPointId** | **String** |  | [optional] 
**Position** | **Int64** |  | 
**PriceComponents** | [**AnyType**](.md) |  | [optional] 
**ProductId** | **String** |  | [optional] 
**ProductSku** | **String** |  | [optional] 
**Quantity** | **String** |  | 
**SupplierArticleNumber** | **String** |  | [optional] 
**TaxRate** | **String** |  | [optional] 
**Unit** | [**AnyType**](.md) |  | 
**UnitPrice** | **String** |  | 
**UsageDataId** | **String** |  | [optional] 
**VatRateNominal** | **String** |  | [optional] 
**VatSpecialCase** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$InvoiceLineItem = Initialize-PSOpenAPIToolsInvoiceLineItem  -ArticleNumber null `
 -Description Electricity Work Price `
 -DiscountAmount null `
 -DiscountPercentage null `
 -InputVatDeductible null `
 -InputVatRate null `
 -IsIntraCommunityAcquisition null `
 -IsMargin25a null `
 -LedgerAccount null `
 -LineTotal 19.9 `
 -LineTotalGross null `
 -Margin25aPurchasePrice null `
 -MeterPointId null `
 -Position null `
 -PriceComponents null `
 -ProductId null `
 -ProductSku null `
 -Quantity 10.0 `
 -SupplierArticleNumber null `
 -TaxRate 19.0 `
 -Unit null `
 -UnitPrice 1.99 `
 -UsageDataId null `
 -VatRateNominal null `
 -VatSpecialCase null
```

- Convert the resource to JSON
```powershell
$InvoiceLineItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

