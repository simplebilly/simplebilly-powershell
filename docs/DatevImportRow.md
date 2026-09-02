# DatevImportRow
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Account** | **String** |  | 
**Amount** | **String** |  | 
**BaseAmount** | **String** |  | 
**BaseCurrency** | **String** |  | 
**BookingText** | **String** |  | 
**BuKey** | **String** |  | 
**CostCenter1** | **String** |  | 
**CostCenter2** | **String** |  | 
**Currency** | **String** |  | 
**DebitCredit** | **String** |  | 
**Discount** | **String** |  | 
**DocumentDate** | **String** |  | 
**DocumentField2** | **String** |  | 
**DocumentNumber** | **String** |  | 
**EuCountryVatId** | **String** |  | 
**EuTaxRate** | **String** |  | 
**ExchangeRate** | **String** |  | 
**OppositeAccount** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$DatevImportRow = Initialize-PSOpenAPIToolsDatevImportRow  -Account null `
 -Amount null `
 -BaseAmount null `
 -BaseCurrency null `
 -BookingText null `
 -BuKey null `
 -CostCenter1 null `
 -CostCenter2 null `
 -Currency null `
 -DebitCredit null `
 -Discount null `
 -DocumentDate null `
 -DocumentField2 null `
 -DocumentNumber null `
 -EuCountryVatId null `
 -EuTaxRate null `
 -ExchangeRate null `
 -OppositeAccount null
```

- Convert the resource to JSON
```powershell
$DatevImportRow | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

