# UsageSnapshot
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Connectors** | **Int64** |  | 
**InvoicesThisMonth** | **Int64** |  | 
**OverageSeats** | **Int64** |  | 
**Users** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$UsageSnapshot = Initialize-PSOpenAPIToolsUsageSnapshot  -Connectors null `
 -InvoicesThisMonth null `
 -OverageSeats null `
 -Users null
```

- Convert the resource to JSON
```powershell
$UsageSnapshot | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

