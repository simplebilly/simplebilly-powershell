# FeatureSettings
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Onlineshop** | **Boolean** | Online shop / storefront module (default: enabled). | 
**ReportBilanz** | **Boolean** | Bilanz (balance sheet) report. | 
**ReportBwa** | **Boolean** | BWA (betriebswirtschaftliche Auswertung). | 
**ReportEuer** | **Boolean** | EÜR (Einnahmen-Überschuss-Rechnung). | 
**ReportGewerbesteuer** | **Boolean** | Gewerbesteuer report. | 
**ReportGuv** | **Boolean** | GuV (profit &amp; loss) report. | 
**ReportKst** | **Boolean** | KSt (Körperschaftsteuer) report. | 
**ReportUstva** | **Boolean** | UStVA (Umsatzsteuervoranmeldung). | 

## Examples

- Prepare the resource
```powershell
$FeatureSettings = Initialize-PSOpenAPIToolsFeatureSettings  -Onlineshop null `
 -ReportBilanz null `
 -ReportBwa null `
 -ReportEuer null `
 -ReportGewerbesteuer null `
 -ReportGuv null `
 -ReportKst null `
 -ReportUstva null
```

- Convert the resource to JSON
```powershell
$FeatureSettings | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

