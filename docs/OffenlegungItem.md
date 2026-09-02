# OffenlegungItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Exists** | **Boolean** | Ob die zugrunde liegenden Daten im System vorhanden sind. | 
**Name** | **String** | Bezeichnung des Offenlegungsbestandteils (§ 325 Abs. 1 HGB). | 
**Source** | **String** | Woher der Bestandteil stammt bzw. fehlt. | 

## Examples

- Prepare the resource
```powershell
$OffenlegungItem = Initialize-PSOpenAPIToolsOffenlegungItem  -Exists null `
 -Name null `
 -Source null
```

- Convert the resource to JSON
```powershell
$OffenlegungItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

