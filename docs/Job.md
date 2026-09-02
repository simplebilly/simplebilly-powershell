# Job
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Attempts** | **Int32** |  | [optional] 
**JobType** | **String** | Discriminator the worker dispatches on (e.g. &quot;&quot;webhook.deliver&quot;&quot;). | 
**MaxAttempts** | **Int32** |  | 
**Payload** | [**AnyType**](.md) |  | [optional] 
**RunAt** | **System.DateTime** | Earliest execution time; None &#x3D; run now. | [optional] 
**Status** | [**JobStatus**](JobStatus.md) | pending | running | done | failed | 

## Examples

- Prepare the resource
```powershell
$Job = Initialize-PSOpenAPIToolsJob  -Attempts null `
 -JobType null `
 -MaxAttempts null `
 -Payload null `
 -RunAt null `
 -Status null
```

- Convert the resource to JSON
```powershell
$Job | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

