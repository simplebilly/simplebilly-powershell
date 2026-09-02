# MarketplaceWebhookEvent
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ConnectionId** | **String** | References the marketplace connection entity. | 
**EventBody** | [**AnyType**](.md) |  | [optional] 
**EventType** | **String** |  | 
**Headers** | [**AnyType**](.md) |  | [optional] 
**Platform** | **String** |  | 
**Processed** | **Boolean** |  | [optional] 
**ProcessingError** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$MarketplaceWebhookEvent = Initialize-PSOpenAPIToolsMarketplaceWebhookEvent  -ConnectionId null `
 -EventBody null `
 -EventType null `
 -Headers null `
 -Platform null `
 -Processed null `
 -ProcessingError null
```

- Convert the resource to JSON
```powershell
$MarketplaceWebhookEvent | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

