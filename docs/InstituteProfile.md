# InstituteProfile
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InstituteType** | [**InstituteType**](InstituteType.md) | Institutsart: &quot;&quot;kein&quot;&quot; | &quot;&quot;kreditinstitut&quot;&quot; | &quot;&quot;finanzdienstleistungsinstitut&quot;&quot; | &quot;&quot;finanzunternehmen&quot;&quot; | &quot;&quot;versicherung&quot;&quot;. | [optional] 
**Kapitalmarktorientiert** | **Boolean** | Kapitalmarktorientierung (§ 325 Abs. 4 HGB): Offenlegungsfrist 4 statt 12 Monate. | [optional] 

## Examples

- Prepare the resource
```powershell
$InstituteProfile = Initialize-PSOpenAPIToolsInstituteProfile  -InstituteType null `
 -Kapitalmarktorientiert null
```

- Convert the resource to JSON
```powershell
$InstituteProfile | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

