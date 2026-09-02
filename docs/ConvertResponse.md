# ConvertResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InvoiceId** | **String** |  | 
**InvoiceNumber** | **String** |  | 
**ProformaId** | **String** |  | 
**ProformaNumber** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ConvertResponse = Initialize-PSOpenAPIToolsConvertResponse  -InvoiceId null `
 -InvoiceNumber null `
 -ProformaId null `
 -ProformaNumber null
```

- Convert the resource to JSON
```powershell
$ConvertResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

