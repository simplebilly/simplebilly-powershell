# Customer
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | [**AnyType**](.md) |  | [optional] 
**ContactPerson** | **String** |  | [optional] 
**Email** | **String** |  | [optional] 
**ExternalOrderNumber** | **String** |  | [optional] 
**Name** | **String** |  | 
**PaymentGracePeriodDays** | **Int32** |  | [optional] 
**Phone** | **String** |  | [optional] 
**VatId** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Customer = Initialize-PSOpenAPIToolsCustomer  -Address null `
 -ContactPerson null `
 -Email null `
 -ExternalOrderNumber null `
 -Name null `
 -PaymentGracePeriodDays null `
 -Phone null `
 -VatId null
```

- Convert the resource to JSON
```powershell
$Customer | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

