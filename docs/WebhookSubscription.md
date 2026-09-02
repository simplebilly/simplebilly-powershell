# WebhookSubscription
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventType** | **String** | Event type to react to (e.g. &quot;&quot;order.created&quot;&quot;); &quot;&quot;*&quot;&quot; &#x3D; all events. | 
**IsActive** | **Boolean** |  | [optional] 
**Name** | **String** | Human label (e.g. &quot;&quot;Warehouse app&quot;&quot;). | 
**Secret** | **String** | Shared secret for HMAC-SHA256 signature, sent as X-Signature. | 
**Url** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$WebhookSubscription = Initialize-PSOpenAPIToolsWebhookSubscription  -EventType null `
 -IsActive null `
 -Name null `
 -Secret null `
 -Url null
```

- Convert the resource to JSON
```powershell
$WebhookSubscription | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

