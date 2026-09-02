# SalesVolumeItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContactId** | **String** |  | 
**ContactType** | **String** |  | 
**LastPurchaseDate** | **String** |  | [optional] 
**Name** | **String** |  | 
**TotalInvoices** | **Int32** |  | 
**TotalRevenue** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$SalesVolumeItem = Initialize-PSOpenAPIToolsSalesVolumeItem  -ContactId null `
 -ContactType null `
 -LastPurchaseDate null `
 -Name null `
 -TotalInvoices null `
 -TotalRevenue null
```

- Convert the resource to JSON
```powershell
$SalesVolumeItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

