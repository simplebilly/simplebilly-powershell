# AccountOverview
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Account** | **String** |  | 
**AccountName** | **String** |  | 
**Balance** | **String** |  | 
**CreditTotal** | **String** |  | 
**DebitTotal** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$AccountOverview = Initialize-PSOpenAPIToolsAccountOverview  -Account null `
 -AccountName null `
 -Balance null `
 -CreditTotal null `
 -DebitTotal null
```

- Convert the resource to JSON
```powershell
$AccountOverview | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

