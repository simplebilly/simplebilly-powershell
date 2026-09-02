# PrintDeliveryNoteResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **String** |  | 
**PdfUrl** | **String** |  | [optional] 
**Success** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$PrintDeliveryNoteResponse = Initialize-PSOpenAPIToolsPrintDeliveryNoteResponse  -Message null `
 -PdfUrl null `
 -Success null
```

- Convert the resource to JSON
```powershell
$PrintDeliveryNoteResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

