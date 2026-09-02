# AbsenceCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AbsenceType** | [**AbsenceType**](AbsenceType.md) | One of &quot;&quot;vacation&quot;&quot;, &quot;&quot;sick&quot;&quot;, &quot;&quot;sabbatical&quot;&quot;, &quot;&quot;parental&quot;&quot;, &quot;&quot;other&quot;&quot;. | [optional] 
**ApprovedAt** | **System.DateTime** |  | [optional] 
**ApprovedBy** | **String** | References the user entity. | [optional] 
**EmployeeId** | **String** | References the employee entity. | [optional] 
**EndDate** | **System.DateTime** |  | [optional] 
**Notes** | **String** |  | [optional] 
**StartDate** | **System.DateTime** |  | [optional] 
**Status** | [**AbsenceStatus**](AbsenceStatus.md) | One of &quot;&quot;pending&quot;&quot;, &quot;&quot;approved&quot;&quot;, &quot;&quot;rejected&quot;&quot;, &quot;&quot;cancelled&quot;&quot;. | [optional] 

## Examples

- Prepare the resource
```powershell
$AbsenceCreate = Initialize-PSOpenAPIToolsAbsenceCreate  -AbsenceType null `
 -ApprovedAt null `
 -ApprovedBy null `
 -EmployeeId null `
 -EndDate null `
 -Notes null `
 -StartDate null `
 -Status null
```

- Convert the resource to JSON
```powershell
$AbsenceCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

