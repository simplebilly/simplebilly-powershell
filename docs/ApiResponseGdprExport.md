# ApiResponseGdprExport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**VarData** | [**ApiResponseGdprExportData**](ApiResponseGdprExportData.md) |  | [optional] 
**VarError** | **String** |  | [optional] 
**Message** | **String** |  | [optional] 
**Success** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$ApiResponseGdprExport = Initialize-PSOpenAPIToolsApiResponseGdprExport  -VarData null `
 -VarError null `
 -Message null `
 -Success null
```

- Convert the resource to JSON
```powershell
$ApiResponseGdprExport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

