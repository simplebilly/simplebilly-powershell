# PaymentCondition
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DiscountDays** | **Int32** |  | 
**DiscountPercentage** | **Double** |  | 
**Id** | **String** |  | 
**Name** | **String** |  | 
**PaymentTermDays** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$PaymentCondition = Initialize-PSOpenAPIToolsPaymentCondition  -DiscountDays null `
 -DiscountPercentage null `
 -Id null `
 -Name null `
 -PaymentTermDays null
```

- Convert the resource to JSON
```powershell
$PaymentCondition | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

