# ContactTimelineResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContactId** | **String** |  | 
**Events** | [**TimelineEvent[]**](TimelineEvent.md) |  | 

## Examples

- Prepare the resource
```powershell
$ContactTimelineResponse = Initialize-PSOpenAPIToolsContactTimelineResponse  -ContactId null `
 -Events null
```

- Convert the resource to JSON
```powershell
$ContactTimelineResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

