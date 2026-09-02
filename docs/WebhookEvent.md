# WebhookEvent
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Attempts** | **Int32** |  | [optional] 
**Channel** | **String** | source for inbound, target URL for outbound. | [optional] 
**Direction** | [**WebhookDirection**](WebhookDirection.md) | inbound | outbound | 
**EventType** | **String** |  | 
**LastError** | **String** |  | [optional] 
**Payload** | [**AnyType**](.md) |  | [optional] 
**Status** | [**WebhookEventStatus**](WebhookEventStatus.md) | accepted | delivered | failed | [optional] 

## Examples

- Prepare the resource
```powershell
$WebhookEvent = Initialize-PSOpenAPIToolsWebhookEvent  -Attempts null `
 -Channel null `
 -Direction null `
 -EventType null `
 -LastError null `
 -Payload null `
 -Status null
```

- Convert the resource to JSON
```powershell
$WebhookEvent | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

