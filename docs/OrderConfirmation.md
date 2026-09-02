# OrderConfirmation
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | [**AnyType**](.md) |  | [optional] 
**ConfirmationNumber** | **String** |  | [optional] 
**ContactId** | **String** | References the contact entity. | [optional] 
**ContactName** | **String** |  | [optional] 
**Currency** | **String** |  | 
**Files** | [**AnyType**](.md) |  | [optional] 
**Introduction** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) |  | [optional] 
**PrecedingSalesVoucherId** | **String** | References the preceding sales voucher entity. | [optional] 
**PrecedingSalesVoucherType** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] 
**Remark** | **String** |  | [optional] 
**Subtotal** | **String** |  | [optional] 
**TaxCondition** | **String** |  | [optional] 
**Title** | **String** |  | [optional] 
**TotalAmount** | **String** |  | [optional] 
**TotalTax** | **String** |  | [optional] 
**VoucherDate** | **System.DateTime** |  | 
**VoucherStatus** | [**VoucherStatus**](VoucherStatus.md) |  | 

## Examples

- Prepare the resource
```powershell
$OrderConfirmation = Initialize-PSOpenAPIToolsOrderConfirmation  -Address null `
 -ConfirmationNumber null `
 -ContactId null `
 -ContactName null `
 -Currency null `
 -Files null `
 -Introduction null `
 -LineItems null `
 -PrecedingSalesVoucherId null `
 -PrecedingSalesVoucherType null `
 -Remark null `
 -Subtotal null `
 -TaxCondition null `
 -Title null `
 -TotalAmount null `
 -TotalTax null `
 -VoucherDate null `
 -VoucherStatus null
```

- Convert the resource to JSON
```powershell
$OrderConfirmation | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

