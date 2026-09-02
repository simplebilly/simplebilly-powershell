# CouponValidation
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **String** |  | 
**DiscountType** | **String** |  | 
**DiscountValue** | **String** |  | 
**DiscountedAmount** | **String** |  | 
**MaxDiscountAmount** | **String** |  | [optional] 
**Reason** | **String** |  | [optional] 
**Valid** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$CouponValidation = Initialize-PSOpenAPIToolsCouponValidation  -Code null `
 -DiscountType null `
 -DiscountValue null `
 -DiscountedAmount null `
 -MaxDiscountAmount null `
 -Reason null `
 -Valid null
```

- Convert the resource to JSON
```powershell
$CouponValidation | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

