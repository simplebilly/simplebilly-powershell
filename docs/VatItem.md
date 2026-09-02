# VatItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NetAmount** | **String** |  | 
**TaxAmount** | **String** |  | 
**TaxRate** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$VatItem = Initialize-PSOpenAPIToolsVatItem  -NetAmount null `
 -TaxAmount null `
 -TaxRate null
```

- Convert the resource to JSON
```powershell
$VatItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

