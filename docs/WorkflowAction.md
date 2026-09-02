# WorkflowAction
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActionType** | **String** |  | 
**Body** | **String** |  | [optional] 
**Subject** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$WorkflowAction = Initialize-PSOpenAPIToolsWorkflowAction  -ActionType null `
 -Body null `
 -Subject null
```

- Convert the resource to JSON
```powershell
$WorkflowAction | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

