# QuotationCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | [**AnyType**](.md) |  | [optional] 
**ContactId** | **String** | References the contact entity. | [optional] 
**ContactName** | **String** |  | [optional] 
**Currency** | **String** |  | 
**ExpirationDate** | **System.DateTime** |  | [optional] 
**Files** | [**AnyType**](.md) |  | [optional] 
**Introduction** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) |  | [optional] 
**PrecedingSalesVoucherId** | **String** | References the preceding sales voucher entity. | [optional] 
**PrecedingSalesVoucherType** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] 
**QuotationNumber** | **String** |  | [optional] 
**Remark** | **String** |  | [optional] 
**TaxCondition** | **String** |  | [optional] 
**Title** | **String** |  | [optional] 
**VoucherDate** | **System.DateTime** |  | 
**VoucherStatus** | [**VoucherStatus**](VoucherStatus.md) |  | 

## Examples

- Prepare the resource
```powershell
$QuotationCreate = Initialize-PSOpenAPIToolsQuotationCreate  -Address null `
 -ContactId null `
 -ContactName null `
 -Currency null `
 -ExpirationDate null `
 -Files null `
 -Introduction null `
 -LineItems null `
 -PrecedingSalesVoucherId null `
 -PrecedingSalesVoucherType null `
 -QuotationNumber null `
 -Remark null `
 -TaxCondition null `
 -Title null `
 -VoucherDate null `
 -VoucherStatus null
```

- Convert the resource to JSON
```powershell
$QuotationCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

