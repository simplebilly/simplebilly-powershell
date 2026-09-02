# DatevBookingPreview
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountNumber** | **String** |  | 
**DebitCredit** | **String** |  | 
**DocumentDate** | **String** |  | 
**DocumentText** | **String** |  | 
**NetAmount** | **String** |  | 
**OppositeAccount** | **String** |  | 
**TaxAmount** | **String** |  | [optional] 
**TaxRate** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$DatevBookingPreview = Initialize-PSOpenAPIToolsDatevBookingPreview  -AccountNumber null `
 -DebitCredit null `
 -DocumentDate null `
 -DocumentText null `
 -NetAmount null `
 -OppositeAccount null `
 -TaxAmount null `
 -TaxRate null
```

- Convert the resource to JSON
```powershell
$DatevBookingPreview | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

