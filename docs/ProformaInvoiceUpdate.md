# ProformaInvoiceUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConvertedAt** | **System.DateTime** |  | [optional] 
**ConvertedToInvoiceId** | **String** | Set when the proforma was converted into a real invoice. References the invoice entity. | [optional] 
**Currency** | [**CurrencyCode**](CurrencyCode.md) |  | [optional] 
**CustomerId** | **String** | References the customer entity. | [optional] 
**CustomerSnapshot** | [**AnyType**](.md) | Snapshot of the recipient at issue time (address, VAT id, …). | [optional] 
**IssueDate** | **System.DateTime** |  | [optional] 
**LineItems** | [**AnyType**](.md) |  | [optional] 
**Notes** | **String** |  | [optional] 
**OrderNumber** | **String** | Reference to the order/quote this proforma belongs to. | [optional] 
**PaymentDueDate** | **System.DateTime** | Optional deadline the real invoice should carry after conversion. | [optional] 
**QuotationId** | **String** | References the quotation entity. | [optional] 
**Status** | [**ProformaInvoiceStatus**](ProformaInvoiceStatus.md) | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. | [optional] 
**Subtotal** | **String** |  | [optional] 
**TotalAmount** | **String** |  | [optional] 
**TotalTax** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ProformaInvoiceUpdate = Initialize-PSOpenAPIToolsProformaInvoiceUpdate  -ConvertedAt null `
 -ConvertedToInvoiceId null `
 -Currency null `
 -CustomerId null `
 -CustomerSnapshot null `
 -IssueDate null `
 -LineItems null `
 -Notes null `
 -OrderNumber null `
 -PaymentDueDate null `
 -QuotationId null `
 -Status null `
 -Subtotal null `
 -TotalAmount null `
 -TotalTax null
```

- Convert the resource to JSON
```powershell
$ProformaInvoiceUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

