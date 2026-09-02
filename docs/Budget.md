# Budget
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Category** | **String** | Posting category key (matches &#x60;category&#x60; on journal entries). | 
**MonthlyGoal** | **String** | Monthly goal amount (gross). 0 means &quot;&quot;no goal set&quot;&quot;. | 
**UpdatedAt** | **System.DateTime** |  | [optional] 
**Year** | **Int32** | Budget year the goal applies to. | 

## Examples

- Prepare the resource
```powershell
$Budget = Initialize-PSOpenAPIToolsBudget  -Category null `
 -MonthlyGoal null `
 -UpdatedAt null `
 -Year null
```

- Convert the resource to JSON
```powershell
$Budget | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

