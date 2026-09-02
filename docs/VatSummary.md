# VatSummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InputTaxItems** | [**VatItem[]**](VatItem.md) |  | 
**OutputTaxItems** | [**VatItem[]**](VatItem.md) |  | 
**TotalInputTax** | **String** |  | 
**TotalOutputTax** | **String** |  | 
**VatDue** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$VatSummary = Initialize-PSOpenAPIToolsVatSummary  -InputTaxItems null `
 -OutputTaxItems null `
 -TotalInputTax null `
 -TotalOutputTax null `
 -VatDue null
```

- Convert the resource to JSON
```powershell
$VatSummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

