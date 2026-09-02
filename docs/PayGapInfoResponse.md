# PayGapInfoResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EmployeeId** | **String** |  | 
**FirstName** | **String** |  | 
**Gender** | **String** |  | [optional] 
**GroupMedianHourly** | **Double** |  | [optional] 
**GroupMedianMonthly** | **Double** |  | [optional] 
**GroupSize** | **Int32** |  | 
**JobTitle** | **String** |  | 
**LastName** | **String** |  | 
**OverallMedianHourly** | **Double** |  | [optional] 
**OwnHourlyGross** | **Double** |  | [optional] 
**OwnMonthlyGross** | **Double** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PayGapInfoResponse = Initialize-PSOpenAPIToolsPayGapInfoResponse  -EmployeeId null `
 -FirstName null `
 -Gender null `
 -GroupMedianHourly null `
 -GroupMedianMonthly null `
 -GroupSize null `
 -JobTitle null `
 -LastName null `
 -OverallMedianHourly null `
 -OwnHourlyGross null `
 -OwnMonthlyGross null
```

- Convert the resource to JSON
```powershell
$PayGapInfoResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

