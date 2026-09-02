# ProformaInvoiceCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConvertedAt** | **System.DateTime** |  | [optional] 
**ConvertedToInvoiceId** | **String** | Set when the proforma was converted into a real invoice. References the invoice entity. | [optional] 
**Currency** | [**CurrencyCode**](CurrencyCode.md) |  | 
**CustomerId** | **String** | References the customer entity. | [optional] 
**CustomerSnapshot** | [**AnyType**](.md) | Snapshot of the recipient at issue time (address, VAT id, …). | [optional] 
**IssueDate** | **System.DateTime** |  | 
**LineItems** | [**AnyType**](.md) |  | 
**Notes** | **String** |  | [optional] 
**OrderNumber** | **String** | Reference to the order/quote this proforma belongs to. | [optional] 
**PaymentDueDate** | **System.DateTime** | Optional deadline the real invoice should carry after conversion. | [optional] 
**QuotationId** | **String** | References the quotation entity. | [optional] 
**Status** | [**ProformaInvoiceStatus**](ProformaInvoiceStatus.md) | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. | 
**Subtotal** | **String** |  | 
**TotalAmount** | **String** |  | 
**TotalTax** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ProformaInvoiceCreate = Initialize-PSOpenAPIToolsProformaInvoiceCreate  -ConvertedAt null `
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
$ProformaInvoiceCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

