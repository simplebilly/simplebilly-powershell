# BudgetKategorie
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Budget** | **String** |  | 
**Differenz** | **String** |  | 
**Goal** | **String** | User-set monthly goal for the category, if any. | [optional] 
**Ist** | **String** |  | 
**Kategorie** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$BudgetKategorie = Initialize-PSOpenAPIToolsBudgetKategorie  -Budget null `
 -Differenz null `
 -Goal null `
 -Ist null `
 -Kategorie null
```

- Convert the resource to JSON
```powershell
$BudgetKategorie | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

