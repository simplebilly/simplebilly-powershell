# SmtpConfig
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Encryption** | [**SmtpEncryption**](SmtpEncryption.md) |  | 
**FromAddress** | **String** |  | 
**FromName** | **String** |  | [optional] 
**VarHost** | **String** |  | 
**Password** | **String** |  | 
**Port** | **Int32** |  | 
**TimeoutSeconds** | **Int64** |  | [optional] 
**Username** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$SmtpConfig = Initialize-PSOpenAPIToolsSmtpConfig  -Encryption null `
 -FromAddress null `
 -FromName null `
 -VarHost null `
 -Password null `
 -Port null `
 -TimeoutSeconds null `
 -Username null
```

- Convert the resource to JSON
```powershell
$SmtpConfig | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

