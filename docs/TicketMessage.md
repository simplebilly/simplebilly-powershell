# TicketMessage
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AuthorEmail** | **String** |  | [optional] 
**AuthorName** | **String** |  | [optional] 
**Body** | **String** |  | 
**BodyHtml** | **String** |  | [optional] 
**ChannelId** | **String** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | 
**Direction** | [**MessageDirection**](MessageDirection.md) |  | 
**ExternalId** | **String** |  | [optional] 
**IsInternal** | **Boolean** |  | 
**MessageType** | [**MessageType**](MessageType.md) |  | 
**Metadata** | [**AnyType**](.md) |  | 
**TenantId** | **String** |  | 
**TicketId** | **String** | References the ticket entity. | 

## Examples

- Prepare the resource
```powershell
$TicketMessage = Initialize-PSOpenAPIToolsTicketMessage  -AuthorEmail null `
 -AuthorName null `
 -Body null `
 -BodyHtml null `
 -ChannelId null `
 -CreatedAt null `
 -Direction null `
 -ExternalId null `
 -IsInternal null `
 -MessageType null `
 -Metadata null `
 -TenantId null `
 -TicketId null
```

- Convert the resource to JSON
```powershell
$TicketMessage | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

