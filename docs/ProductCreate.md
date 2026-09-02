# ProductCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Availability** | **String** |  | [optional] 
**Barcode** | **String** |  | [optional] 
**Brand** | **String** |  | [optional] 
**CategoryId** | **String** |  | [optional] 
**Condition** | **String** |  | [optional] 
**DefaultLedgerAccount** | **String** |  | [optional] 
**DefaultPrice** | **String** |  | [optional] 
**DefaultPriceFormulaId** | **String** | References the price formula entity. | [optional] 
**DefaultTaxRate** | **String** |  | [optional] 
**Description** | **String** |  | [optional] 
**Gtin** | **String** |  | [optional] 
**Height** | **String** |  | [optional] 
**ImageLink** | **String** |  | [optional] 
**Images** | [**AnyType**](.md) |  | [optional] 
**IsTaxable** | **Boolean** |  | [optional] 
**Length** | **String** |  | [optional] 
**Link** | **String** |  | [optional] 
**MaxStock** | **Int64** | Target stock level used by reorder proposals. | [optional] 
**MinStock** | **Int64** | Reorder point — when stock falls below this, a reorder is suggested. | [optional] 
**Mpn** | **String** |  | [optional] 
**Name** | **String** |  | 
**PackageHeight** | **String** |  | [optional] 
**PackageLength** | **String** |  | [optional] 
**PackageWeightUnit** | **String** |  | [optional] 
**PackageWeightValue** | **String** |  | [optional] 
**PackageWidth** | **String** |  | [optional] 
**ProductCode** | **String** |  | 
**ProductType** | **String** |  | [optional] 
**PurchasePrice** | **String** |  | [optional] 
**ReorderQuantity** | **Int64** | Suggested purchase quantity when a reorder proposal is created. | [optional] 
**SalePrice** | **String** |  | [optional] 
**ShippingPrice** | **String** |  | [optional] 
**ShippingRequiresInsurance** | **Boolean** |  | [optional] 
**Sku** | **String** |  | 
**StockQuantity** | **Int64** |  | [optional] 
**Tags** | [**AnyType**](.md) |  | [optional] 
**TaxPrice** | **String** |  | [optional] 
**TrackBatch** | **Boolean** | Whether this product requires batch (Chargennummer) tracking. | [optional] 
**TrackSerial** | **Boolean** | Whether this product requires serial-number tracking. | [optional] 
**Unit** | [**AnyType**](.md) |  | [optional] 
**WeightUnit** | **String** |  | [optional] 
**WeightValue** | **String** |  | [optional] 
**Width** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ProductCreate = Initialize-PSOpenAPIToolsProductCreate  -Availability null `
 -Barcode null `
 -Brand null `
 -CategoryId null `
 -Condition null `
 -DefaultLedgerAccount null `
 -DefaultPrice null `
 -DefaultPriceFormulaId null `
 -DefaultTaxRate null `
 -Description null `
 -Gtin null `
 -Height null `
 -ImageLink null `
 -Images null `
 -IsTaxable null `
 -Length null `
 -Link null `
 -MaxStock null `
 -MinStock null `
 -Mpn null `
 -Name null `
 -PackageHeight null `
 -PackageLength null `
 -PackageWeightUnit null `
 -PackageWeightValue null `
 -PackageWidth null `
 -ProductCode null `
 -ProductType null `
 -PurchasePrice null `
 -ReorderQuantity null `
 -SalePrice null `
 -ShippingPrice null `
 -ShippingRequiresInsurance null `
 -Sku null `
 -StockQuantity null `
 -Tags null `
 -TaxPrice null `
 -TrackBatch null `
 -TrackSerial null `
 -Unit null `
 -WeightUnit null `
 -WeightValue null `
 -Width null
```

- Convert the resource to JSON
```powershell
$ProductCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

