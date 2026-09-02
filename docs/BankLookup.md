# BankLookup
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BankName** | **String** |  | [optional] 
**Bic** | **String** |  | [optional] 
**Iban** | **String** |  | 
**Nextgenpsd2Url** | **String** |  | [optional] 
**Psd2Supported** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$BankLookup = Initialize-PSOpenAPIToolsBankLookup  -BankName null `
 -Bic null `
 -Iban null `
 -Nextgenpsd2Url null `
 -Psd2Supported null
```

- Convert the resource to JSON
```powershell
$BankLookup | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

