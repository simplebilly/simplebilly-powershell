# ReturnLogisticsSummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ByStatus** | [**AnyType**](.md) | Number of return orders per status. | 
**ByWarehouse** | [**ReturnWarehouseSummary[]**](ReturnWarehouseSummary.md) | Per-warehouse aggregation. | 
**ItemsRestocked** | **Int64** | Sum of &#x60;restock: true&#x60; line-item quantities. | 
**ItemsScrapped** | **Int64** | Sum of &#x60;restock: false&#x60; line-item quantities (scrapped/disposed). | 
**TotalItems** | **Int64** | Sum of all line-item quantities across returns. | 
**TotalReturns** | **Int64** | Total number of return orders (excluding soft-deleted). | 

## Examples

- Prepare the resource
```powershell
$ReturnLogisticsSummary = Initialize-PSOpenAPIToolsReturnLogisticsSummary  -ByStatus null `
 -ByWarehouse null `
 -ItemsRestocked null `
 -ItemsScrapped null `
 -TotalItems null `
 -TotalReturns null
```

- Convert the resource to JSON
```powershell
$ReturnLogisticsSummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

