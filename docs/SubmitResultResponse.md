# SubmitResultResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CertificateId** | **String** |  | [optional] 
**CompletionId** | **String** |  | 
**PassScore** | **Int32** |  | 
**Passed** | **Boolean** |  | 
**Score** | **Int32** |  | 
**ValidUntil** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$SubmitResultResponse = Initialize-PSOpenAPIToolsSubmitResultResponse  -CertificateId null `
 -CompletionId null `
 -PassScore null `
 -Passed null `
 -Score null `
 -ValidUntil null
```

- Convert the resource to JSON
```powershell
$SubmitResultResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

