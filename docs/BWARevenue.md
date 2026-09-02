# BWARevenue
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RevenueBreakdown** | [**RevenueItem[]**](RevenueItem.md) |  | 
**TotalRevenue** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$BWARevenue = Initialize-PSOpenAPIToolsBWARevenue  -RevenueBreakdown null `
 -TotalRevenue null
```

- Convert the resource to JSON
```powershell
$BWARevenue | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

