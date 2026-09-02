# KonzernBeteiligung
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CompanyName** | **String** |  | 
**ControlBasis** | **String[]** | Erfüllte Kontroll-Indikatoren (§ 290 Abs. 2 HGB) als deutsche Bezeichnungen. | 
**Controlled** | **Boolean** |  | 
**OwnershipPct** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$KonzernBeteiligung = Initialize-PSOpenAPIToolsKonzernBeteiligung  -CompanyName null `
 -ControlBasis null `
 -Controlled null `
 -OwnershipPct null
```

- Convert the resource to JSON
```powershell
$KonzernBeteiligung | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

