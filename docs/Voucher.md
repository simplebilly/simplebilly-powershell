# Voucher
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CategoryId** | **String** |  | [optional] 
**ContactId** | **String** | References the contact entity. | [optional] 
**ContactName** | **String** |  | [optional] 
**Currency** | **String** |  | 
**Description** | **String** |  | [optional] 
**FileAttachments** | [**AnyType**](.md) |  | [optional] 
**LineItems** | [**AnyType**](.md) |  | [optional] 
**Metadata** | [**AnyType**](.md) |  | [optional] 
**Notes** | **String** |  | [optional] 
**OpenAmount** | **String** |  | [optional] 
**PaidDate** | **System.DateTime** |  | [optional] 
**PaymentStatus** | [**PaymentStatus**](PaymentStatus.md) |  | [optional] 
**TaxAmounts** | [**AnyType**](.md) |  | [optional] 
**TaxCondition** | **String** |  | [optional] 
**TotalGrossAmount** | **String** |  | [optional] 
**TotalNetAmount** | **String** |  | [optional] 
**VoucherDate** | **System.DateTime** |  | 
**VoucherNumber** | **String** |  | [optional] 
**VoucherStatus** | [**VoucherStatus**](VoucherStatus.md) |  | 
**VoucherType** | [**VoucherType**](VoucherType.md) |  | 

## Examples

- Prepare the resource
```powershell
$Voucher = Initialize-PSOpenAPIToolsVoucher  -CategoryId null `
 -ContactId null `
 -ContactName null `
 -Currency null `
 -Description null `
 -FileAttachments null `
 -LineItems null `
 -Metadata null `
 -Notes null `
 -OpenAmount null `
 -PaidDate null `
 -PaymentStatus null `
 -TaxAmounts null `
 -TaxCondition null `
 -TotalGrossAmount null `
 -TotalNetAmount null `
 -VoucherDate null `
 -VoucherNumber null `
 -VoucherStatus null `
 -VoucherType null
```

- Convert the resource to JSON
```powershell
$Voucher | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

