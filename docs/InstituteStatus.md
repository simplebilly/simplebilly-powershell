# InstituteStatus
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Checklist** | [**InstituteCheckItem[]**](InstituteCheckItem.md) |  | 
**Deadlines** | [**InstituteDeadlines**](InstituteDeadlines.md) |  | 
**InstituteType** | **String** |  | 
**Kapitalmarktorientiert** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$InstituteStatus = Initialize-PSOpenAPIToolsInstituteStatus  -Checklist null `
 -Deadlines null `
 -InstituteType null `
 -Kapitalmarktorientiert null
```

- Convert the resource to JSON
```powershell
$InstituteStatus | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

