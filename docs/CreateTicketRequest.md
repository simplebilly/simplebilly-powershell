# CreateTicketRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ChannelId** | **String** |  | [optional] 
**ChannelType** | **String** |  | [optional] 
**CustomerEmail** | **String** |  | [optional] 
**CustomerId** | **String** |  | [optional] 
**CustomerName** | **String** |  | [optional] 
**ExternalId** | **String** |  | [optional] 
**MessageBody** | **String** |  | 
**OrderRef** | **String** |  | [optional] 
**Subject** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$CreateTicketRequest = Initialize-PSOpenAPIToolsCreateTicketRequest  -ChannelId null `
 -ChannelType null `
 -CustomerEmail null `
 -CustomerId null `
 -CustomerName null `
 -ExternalId null `
 -MessageBody null `
 -OrderRef null `
 -Subject null
```

- Convert the resource to JSON
```powershell
$CreateTicketRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

