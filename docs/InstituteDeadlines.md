# InstituteDeadlines
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AbschlusspruefungMonths** | **Int32** | HGB § 340k/§ 341k: Abschlussprüfung (5 Monate). | [optional] 
**JahresabschlussBafinMonths** | **Int32** | KWG § 26: Jahresabschluss an die BaFin (3 Monate, nur KWG-Institute). | [optional] 
**OffenlegungMonths** | **Int32** | HGB § 325 Abs. 4: Offenlegung (4 kapitalmarktorientiert / 12 sonst). | 

## Examples

- Prepare the resource
```powershell
$InstituteDeadlines = Initialize-PSOpenAPIToolsInstituteDeadlines  -AbschlusspruefungMonths null `
 -JahresabschlussBafinMonths null `
 -OffenlegungMonths null
```

- Convert the resource to JSON
```powershell
$InstituteDeadlines | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

