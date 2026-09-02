# MarketplaceConnection
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Config** | [**AnyType**](.md) |  | 
**ConnectionId** | **String** |  | 
**ConnectorType** | [**ConnectorType**](ConnectorType.md) |  | 
**CreatedAt** | **System.DateTime** |  | 
**IsActive** | **Boolean** |  | 
**Label** | **String** |  | 
**LastSyncAt** | **System.DateTime** |  | [optional] 
**Platform** | **String** |  | 
**PlatformUserId** | **String** |  | [optional] 
**Scopes** | **String** |  | [optional] 
**ShopDomain** | **String** |  | [optional] 
**ShopName** | **String** |  | [optional] 
**SyncStatus** | **String** |  | [optional] 
**TenantId** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$MarketplaceConnection = Initialize-PSOpenAPIToolsMarketplaceConnection  -Config null `
 -ConnectionId null `
 -ConnectorType null `
 -CreatedAt null `
 -IsActive null `
 -Label null `
 -LastSyncAt null `
 -Platform null `
 -PlatformUserId null `
 -Scopes null `
 -ShopDomain null `
 -ShopName null `
 -SyncStatus null `
 -TenantId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$MarketplaceConnection | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

