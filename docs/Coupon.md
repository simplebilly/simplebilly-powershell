# Coupon
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **String** |  | 
**Description** | **String** |  | [optional] 
**DiscountType** | [**DiscountType**](DiscountType.md) |  | 
**DiscountValue** | **String** |  | 
**ExpiresAt** | **System.DateTime** |  | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**IsCombineable** | **Boolean** |  | [optional] 
**MaxDiscountAmount** | **String** |  | [optional] 
**MaxUses** | **Int32** |  | [optional] 
**MaxUsesPerCustomer** | **Int32** |  | [optional] 
**MinOrderAmount** | **String** |  | [optional] 
**ProductIds** | [**AnyType**](.md) |  | [optional] 
**StartsAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Coupon = Initialize-PSOpenAPIToolsCoupon  -Code null `
 -Description null `
 -DiscountType null `
 -DiscountValue null `
 -ExpiresAt null `
 -IsActive null `
 -IsCombineable null `
 -MaxDiscountAmount null `
 -MaxUses null `
 -MaxUsesPerCustomer null `
 -MinOrderAmount null `
 -ProductIds null `
 -StartsAt null
```

- Convert the resource to JSON
```powershell
$Coupon | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

