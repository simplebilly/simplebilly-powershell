# QRCodeResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContentType** | **String** |  | 
**QrCodeBase64** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$QRCodeResponse = Initialize-PSOpenAPIToolsQRCodeResponse  -ContentType null `
 -QrCodeBase64 null
```

- Convert the resource to JSON
```powershell
$QRCodeResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

