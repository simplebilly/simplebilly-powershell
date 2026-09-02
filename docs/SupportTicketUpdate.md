# SupportTicketUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignedTo** | **String** |  | [optional] 
**ChannelId** | **String** |  | [optional] 
**ChannelType** | [**SupportChannelType**](SupportChannelType.md) |  | [optional] 
**ClosedAt** | **System.DateTime** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | [optional] 
**CustomerEmail** | **String** |  | [optional] 
**CustomerId** | **String** | References the customer entity. | [optional] 
**CustomerName** | **String** |  | [optional] 
**ExternalId** | **String** |  | [optional] 
**FirstMessageAt** | **System.DateTime** |  | [optional] 
**LastMessageAt** | **System.DateTime** |  | [optional] 
**LeadId** | **String** | References the lead entity. | [optional] 
**MessageCount** | **Int32** |  | [optional] 
**OrderRef** | **String** |  | [optional] 
**Priority** | [**TicketPriority**](TicketPriority.md) |  | [optional] 
**Resolution** | **String** |  | [optional] 
**Status** | [**SupportTicketStatus**](SupportTicketStatus.md) |  | [optional] 
**Subject** | **String** |  | [optional] 
**Tags** | [**AnyType**](.md) |  | [optional] 
**TenantId** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$SupportTicketUpdate = Initialize-PSOpenAPIToolsSupportTicketUpdate  -AssignedTo null `
 -ChannelId null `
 -ChannelType null `
 -ClosedAt null `
 -CreatedAt null `
 -CustomerEmail null `
 -CustomerId null `
 -CustomerName null `
 -ExternalId null `
 -FirstMessageAt null `
 -LastMessageAt null `
 -LeadId null `
 -MessageCount null `
 -OrderRef null `
 -Priority null `
 -Resolution null `
 -Status null `
 -Subject null `
 -Tags null `
 -TenantId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$SupportTicketUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

