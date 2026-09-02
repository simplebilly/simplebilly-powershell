# AllocatePaymentRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **Double** |  | 
**InvoiceId** | **String** |  | 
**PaymentId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$AllocatePaymentRequest = Initialize-PSOpenAPIToolsAllocatePaymentRequest  -Amount null `
 -InvoiceId null `
 -PaymentId null
```

- Convert the resource to JSON
```powershell
$AllocatePaymentRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

