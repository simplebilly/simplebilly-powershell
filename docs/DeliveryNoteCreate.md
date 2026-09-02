# DeliveryNoteCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | [**AnyType**](.md) |  | [optional] 
**ContactId** | **String** | References the contact entity. | [optional] 
**ContactName** | **String** |  | [optional] 
**Currency** | **String** |  | 
**DeliveryDate** | **System.DateTime** |  | [optional] 
**DeliveryNoteNumber** | **String** |  | [optional] 
**Files** | [**AnyType**](.md) |  | [optional] 
**Introduction** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) |  | [optional] 
**PrecedingSalesVoucherId** | **String** | References the preceding sales voucher entity. | [optional] 
**PrecedingSalesVoucherType** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] 
**Remark** | **String** |  | [optional] 
**ShippingDate** | **System.DateTime** |  | [optional] 
**ShippingMethod** | **String** |  | [optional] 
**Title** | **String** |  | [optional] 
**VoucherDate** | **System.DateTime** |  | 
**VoucherStatus** | [**VoucherStatus**](VoucherStatus.md) |  | 

## Examples

- Prepare the resource
```powershell
$DeliveryNoteCreate = Initialize-PSOpenAPIToolsDeliveryNoteCreate  -Address null `
 -ContactId null `
 -ContactName null `
 -Currency null `
 -DeliveryDate null `
 -DeliveryNoteNumber null `
 -Files null `
 -Introduction null `
 -LineItems null `
 -PrecedingSalesVoucherId null `
 -PrecedingSalesVoucherType null `
 -Remark null `
 -ShippingDate null `
 -ShippingMethod null `
 -Title null `
 -VoucherDate null `
 -VoucherStatus null
```

- Convert the resource to JSON
```powershell
$DeliveryNoteCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

