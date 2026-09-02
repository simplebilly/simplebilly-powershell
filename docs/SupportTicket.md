# SupportTicket
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignedTo** | **String** |  | [optional] 
**ChannelId** | **String** |  | [optional] 
**ChannelType** | [**SupportChannelType**](SupportChannelType.md) |  | [optional] 
**ClosedAt** | **System.DateTime** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | 
**CustomerEmail** | **String** |  | [optional] 
**CustomerId** | **String** | References the customer entity. | [optional] 
**CustomerName** | **String** |  | [optional] 
**ExternalId** | **String** |  | [optional] 
**FirstMessageAt** | **System.DateTime** |  | 
**LastMessageAt** | **System.DateTime** |  | 
**LeadId** | **String** | References the lead entity. | [optional] 
**MessageCount** | **Int32** |  | 
**OrderRef** | **String** |  | [optional] 
**Priority** | [**TicketPriority**](TicketPriority.md) |  | 
**Resolution** | **String** |  | [optional] 
**Status** | [**SupportTicketStatus**](SupportTicketStatus.md) |  | 
**Subject** | **String** |  | 
**Tags** | [**AnyType**](.md) |  | 
**TenantId** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$SupportTicket = Initialize-PSOpenAPIToolsSupportTicket  -AssignedTo null `
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
$SupportTicket | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

