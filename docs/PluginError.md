# PluginError
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BadRequest** | [**SystemCollectionsHashtable[]**](SystemCollectionsHashtable.md) |  | 
**NotFound** | [**SystemCollectionsHashtable[]**](SystemCollectionsHashtable.md) |  | 
**Unauthorized** | [**SystemCollectionsHashtable[]**](SystemCollectionsHashtable.md) |  | 
**InternalError** | [**SystemCollectionsHashtable[]**](SystemCollectionsHashtable.md) |  | 
**DatabaseError** | [**SystemCollectionsHashtable[]**](SystemCollectionsHashtable.md) |  | 
**ValidationError** | [**SystemCollectionsHashtable[]**](SystemCollectionsHashtable.md) |  | 
**NotImplemented** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PluginError = Initialize-PSOpenAPIToolsPluginError  -BadRequest null `
 -NotFound null `
 -Unauthorized null `
 -InternalError null `
 -DatabaseError null `
 -ValidationError null `
 -NotImplemented null
```

- Convert the resource to JSON
```powershell
$PluginError | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

