# ContactHistoryResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContactId** | **String** |  | 
**InboundCount** | **Int64** |  | 
**Items** | [**CustomerCommunication[]**](CustomerCommunication.md) |  | 
**OutboundCount** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$ContactHistoryResponse = Initialize-PSOpenAPIToolsContactHistoryResponse  -ContactId null `
 -InboundCount null `
 -Items null `
 -OutboundCount null
```

- Convert the resource to JSON
```powershell
$ContactHistoryResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

