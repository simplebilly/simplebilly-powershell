# InvoiceCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Attachments** | [**AnyType**](.md) |  | [optional] 
**BillingPeriodEnd** | **System.DateTime** |  | [optional] 
**BillingPeriodStart** | **System.DateTime** |  | [optional] 
**CancellationDate** | **System.DateTime** |  | [optional] 
**CancellationInvoiceId** | **String** | References the invoice entity. | [optional] 
**CancellationReason** | **String** |  | [optional] 
**ContractId** | **String** | References the contract entity. | [optional] 
**Currency** | [**CurrencyCode**](CurrencyCode.md) |  | 
**CustomerId** | **String** | References the customer entity. | [optional] 
**DiscountAmount** | **String** |  | [optional] 
**DiscountDays** | **Int32** |  | [optional] 
**DiscountPercentage** | **String** |  | [optional] 
**DocumentType** | [**DocumentType**](DocumentType.md) |  | [optional] 
**DunningLevel** | **Int32** |  | [optional] 
**InputVatAmount** | **String** |  | [optional] 
**InputVatDeductible** | **Boolean** |  | [optional] 
**InputVatPercentage** | **String** |  | [optional] 
**IntroductionText** | **String** |  | [optional] 
**InvoiceType** | [**InvoiceType**](InvoiceType.md) |  | 
**IsCancelled** | **Boolean** |  | [optional] 
**IsDraft** | **Boolean** |  | [optional] 
**IsEuAcquisition** | **Boolean** |  | [optional] 
**IsEuDelivery** | **Boolean** |  | [optional] 
**IsIntraCommunityAcquisition** | **Boolean** |  | [optional] 
**IsReverseCharge** | **Boolean** |  | [optional] 
**IssueDate** | **System.DateTime** |  | 
**LedgerAccount** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) |  | 
**Margin25a** | **Boolean** |  | [optional] 
**Margin25aGross** | **String** |  | [optional] 
**Margin25aPurchasePrice** | **String** |  | [optional] 
**Notes** | **String** |  | [optional] 
**OrderNumber** | **String** |  | [optional] 
**OriginalPdfPath** | **String** |  | [optional] 
**PaidAmount** | **String** |  | [optional] 
**PaymentDueDate** | **System.DateTime** |  | [optional] 
**PaymentStatus** | [**PaymentStatus**](PaymentStatus.md) |  | [optional] 
**PaymentTermsText** | **String** |  | [optional] 
**PrecedingSalesVoucherId** | **String** | References the preceding sales voucher entity. | [optional] 
**PrecedingSalesVoucherType** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] 
**ReceiptConfirmationAvailable** | **Boolean** |  | [optional] 
**RelatedInvoiceId** | **String** | References the invoice entity. | [optional] 
**RelationshipType** | **String** |  | [optional] 
**SenderSnapshot** | [**AnyType**](.md) |  | [optional] 
**SentAt** | **System.DateTime** |  | [optional] 
**ServicePeriodEnd** | **System.DateTime** |  | [optional] 
**ServicePeriodStart** | **System.DateTime** |  | [optional] 
**Status** | [**InvoiceStatus**](InvoiceStatus.md) |  | 
**Subtotal** | **String** |  | 
**SupplierId** | **String** | References the supplier entity. | [optional] 
**TaxExemptionReason** | **String** |  | [optional] 
**TotalAmount** | **String** |  | 
**TotalTax** | **String** |  | 
**VatCountry** | [**CountryCode**](CountryCode.md) |  | [optional] 
**VatSpecialCase** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$InvoiceCreate = Initialize-PSOpenAPIToolsInvoiceCreate  -Attachments null `
 -BillingPeriodEnd null `
 -BillingPeriodStart null `
 -CancellationDate null `
 -CancellationInvoiceId null `
 -CancellationReason null `
 -ContractId null `
 -Currency null `
 -CustomerId null `
 -DiscountAmount null `
 -DiscountDays null `
 -DiscountPercentage null `
 -DocumentType null `
 -DunningLevel null `
 -InputVatAmount null `
 -InputVatDeductible null `
 -InputVatPercentage null `
 -IntroductionText null `
 -InvoiceType null `
 -IsCancelled null `
 -IsDraft null `
 -IsEuAcquisition null `
 -IsEuDelivery null `
 -IsIntraCommunityAcquisition null `
 -IsReverseCharge null `
 -IssueDate null `
 -LedgerAccount null `
 -LineItems null `
 -Margin25a null `
 -Margin25aGross null `
 -Margin25aPurchasePrice null `
 -Notes null `
 -OrderNumber null `
 -OriginalPdfPath null `
 -PaidAmount null `
 -PaymentDueDate null `
 -PaymentStatus null `
 -PaymentTermsText null `
 -PrecedingSalesVoucherId null `
 -PrecedingSalesVoucherType null `
 -ReceiptConfirmationAvailable null `
 -RelatedInvoiceId null `
 -RelationshipType null `
 -SenderSnapshot null `
 -SentAt null `
 -ServicePeriodEnd null `
 -ServicePeriodStart null `
 -Status null `
 -Subtotal null `
 -SupplierId null `
 -TaxExemptionReason null `
 -TotalAmount null `
 -TotalTax null `
 -VatCountry null `
 -VatSpecialCase null
```

- Convert the resource to JSON
```powershell
$InvoiceCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

