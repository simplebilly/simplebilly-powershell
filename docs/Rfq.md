# Rfq
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, sku, quantity, requested_unit_price?, quoted_unit_price?}&#x60;. | 
**Notes** | **String** |  | [optional] 
**RequestedDate** | **System.DateTime** |  | 
**ResponseDate** | **System.DateTime** |  | [optional] 
**RfqNumber** | **String** |  | 
**Status** | [**RfqStatus**](RfqStatus.md) | One of: draft | sent | offer_received | rejected | converted | 
**SupplierContactId** | **String** | References the supplier entity. | [optional] 
**SupplierName** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Rfq = Initialize-PSOpenAPIToolsRfq  -Currency null `
 -LineItems null `
 -Notes null `
 -RequestedDate null `
 -ResponseDate null `
 -RfqNumber null `
 -Status null `
 -SupplierContactId null `
 -SupplierName null
```

- Convert the resource to JSON
```powershell
$Rfq | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

