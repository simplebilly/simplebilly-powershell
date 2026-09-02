# BudgetGoalRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MonthlyGoal** | **String** | Monthly goal amount (gross). 0 means &quot;&quot;no goal&quot;&quot; (fallback to default). | 
**Year** | **Int32** | Budget year the goal applies to. | 

## Examples

- Prepare the resource
```powershell
$BudgetGoalRequest = Initialize-PSOpenAPIToolsBudgetGoalRequest  -MonthlyGoal null `
 -Year null
```

- Convert the resource to JSON
```powershell
$BudgetGoalRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

