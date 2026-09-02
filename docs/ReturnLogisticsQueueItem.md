# ReturnLogisticsQueueItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AgeDays** | **Int64** | Days since creation, oldest first. | 
**CreatedAt** | **System.DateTime** |  | 
**CustomerName** | **String** |  | [optional] 
**LineItems** | [**AnyType**](.md) |  | 
**OrderNumber** | **String** |  | [optional] 
**ReturnNumber** | **String** |  | 
**ReturnOrderId** | **String** |  | 
**Status** | **String** |  | 
**WarehouseId** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ReturnLogisticsQueueItem = Initialize-PSOpenAPIToolsReturnLogisticsQueueItem  -AgeDays null `
 -CreatedAt null `
 -CustomerName null `
 -LineItems null `
 -OrderNumber null `
 -ReturnNumber null `
 -ReturnOrderId null `
 -Status null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$ReturnLogisticsQueueItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

