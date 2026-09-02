# DownPaymentInvoice
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContactId** | **String** |  | [optional] 
**ContactName** | **String** |  | [optional] 
**CreatedAt** | **String** |  | [readonly] 
**Currency** | **String** |  | 
**Id** | **String** |  | 
**Notes** | **String** |  | [optional] 
**PaidAmount** | **String** |  | 
**TotalAmount** | **String** |  | 
**VoucherDate** | **System.DateTime** |  | 
**VoucherNumber** | **String** |  | [optional] 
**VoucherStatus** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$DownPaymentInvoice = Initialize-PSOpenAPIToolsDownPaymentInvoice  -ContactId null `
 -ContactName null `
 -CreatedAt null `
 -Currency null `
 -Id null `
 -Notes null `
 -PaidAmount null `
 -TotalAmount null `
 -VoucherDate null `
 -VoucherNumber null `
 -VoucherStatus null
```

- Convert the resource to JSON
```powershell
$DownPaymentInvoice | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

