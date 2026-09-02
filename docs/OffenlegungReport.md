# OffenlegungReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Deadline** | **System.DateTime** | Fristende (Abschlussstichtag + Frist). | 
**DeadlineMonths** | **Int32** | Offenlegungsfrist in Monaten (§ 325 Abs. 4 HGB). | 
**Items** | [**OffenlegungItem[]**](OffenlegungItem.md) |  | 
**Kapitalmarktorientiert** | **Boolean** | Annahme über die Kapitalmarktorientierung. | 
**Note** | **String** |  | 
**Year** | **Int32** | Berichtsjahr (laufendes Kalenderjahr). | 

## Examples

- Prepare the resource
```powershell
$OffenlegungReport = Initialize-PSOpenAPIToolsOffenlegungReport  -Deadline null `
 -DeadlineMonths null `
 -Items null `
 -Kapitalmarktorientiert null `
 -Note null `
 -Year null
```

- Convert the resource to JSON
```powershell
$OffenlegungReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

