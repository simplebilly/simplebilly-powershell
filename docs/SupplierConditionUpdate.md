# SupplierConditionUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **String** | Currency for the minimum order value. | [optional] 
**DeliveryTerms** | **String** | Incoterms, e.g. &quot;&quot;EXW&quot;&quot;, &quot;&quot;DAP&quot;&quot;. | [optional] 
**EarlyPaymentDiscountPercent** | **String** | Early-payment discount percentage (Skonto), e.g. 2.0. | [optional] 
**IsDefault** | **Boolean** | Is this the default condition for the supplier? | [optional] 
**MinimumOrderValue** | **String** | Minimum order value required for this supplier. | [optional] 
**Notes** | **String** |  | [optional] 
**PaymentDueDays** | **Int32** | Number of days within which payment is due. | [optional] 
**PaymentTerms** | **String** | Payment terms, e.g. &quot;&quot;14 Tage, 2% Skonto&quot;&quot;. | [optional] 
**SupplierContactId** | **String** | The supplier this condition applies to (&#x60;contact_id&#x60;). References the supplier entity. | [optional] 
**SupplierName** | **String** | The name of the supplier, denormalized for easy listing. | [optional] 
**VolumeDiscountTiers** | [**AnyType**](.md) | Tiered discounts: JSON array of &#x60;{min_quantity, discount_percent}&#x60;. | [optional] 

## Examples

- Prepare the resource
```powershell
$SupplierConditionUpdate = Initialize-PSOpenAPIToolsSupplierConditionUpdate  -Currency null `
 -DeliveryTerms null `
 -EarlyPaymentDiscountPercent null `
 -IsDefault null `
 -MinimumOrderValue null `
 -Notes null `
 -PaymentDueDays null `
 -PaymentTerms null `
 -SupplierContactId null `
 -SupplierName null `
 -VolumeDiscountTiers null
```

- Convert the resource to JSON
```powershell
$SupplierConditionUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

