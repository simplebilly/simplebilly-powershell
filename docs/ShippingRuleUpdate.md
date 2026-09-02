# ShippingRuleUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Carrier** | **String** | Provider that auto-filled this rule (e.g. &quot;&quot;ups&quot;&quot;), if any. | [optional] 
**Country** | [**CountryCode**](CountryCode.md) | None &#x3D; applies to all countries. | [optional] 
**DeliveryTime** | **String** | Delivery time text, e.g. &quot;&quot;1-3&quot;&quot;. | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**MaxWeightKg** | **Double** |  | [optional] 
**MinWeightKg** | **Double** |  | [optional] 
**Name** | **String** | Delivery-method label, e.g. &quot;&quot;Standardversand&quot;&quot;. | [optional] 
**Notes** | **String** |  | [optional] 
**Price** | **String** | Shipping cost in the shop&#39;s currency. | [optional] 
**Priority** | **Int32** | Lower wins when multiple rules match. | [optional] 

## Examples

- Prepare the resource
```powershell
$ShippingRuleUpdate = Initialize-PSOpenAPIToolsShippingRuleUpdate  -Carrier null `
 -Country null `
 -DeliveryTime null `
 -IsActive null `
 -MaxWeightKg null `
 -MinWeightKg null `
 -Name null `
 -Notes null `
 -Price null `
 -Priority null
```

- Convert the resource to JSON
```powershell
$ShippingRuleUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

