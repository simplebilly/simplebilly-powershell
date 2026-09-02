# JobTitleGap
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EmployeeCount** | **Int32** |  | 
**FemaleMeanHourly** | **String** |  | 
**JobTitle** | **String** |  | 
**MaleMeanHourly** | **String** |  | 
**MeanGapPct** | **Double** |  | 
**MedianGapPct** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$JobTitleGap = Initialize-PSOpenAPIToolsJobTitleGap  -EmployeeCount null `
 -FemaleMeanHourly null `
 -JobTitle null `
 -MaleMeanHourly null `
 -MeanGapPct null `
 -MedianGapPct null
```

- Convert the resource to JSON
```powershell
$JobTitleGap | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

