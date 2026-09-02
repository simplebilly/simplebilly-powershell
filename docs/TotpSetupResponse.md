# TotpSetupResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BackupCodes** | **String[]** |  | 
**QrCodeUrl** | **String** |  | 
**Secret** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$TotpSetupResponse = Initialize-PSOpenAPIToolsTotpSetupResponse  -BackupCodes null `
 -QrCodeUrl null `
 -Secret null
```

- Convert the resource to JSON
```powershell
$TotpSetupResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

