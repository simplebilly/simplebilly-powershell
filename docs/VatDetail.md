# VatDetail
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Count** | **Int64** |  | 
**NetAmount** | **String** |  | 
**TaxAmount** | **String** |  | 
**TaxRate** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$VatDetail = Initialize-PSOpenAPIToolsVatDetail  -Count null `
 -NetAmount null `
 -TaxAmount null `
 -TaxRate null
```

- Convert the resource to JSON
```powershell
$VatDetail | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

