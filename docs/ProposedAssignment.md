# ProposedAssignment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AmountPaid** | **String** |  | 
**Confidence** | **Double** |  | 
**CustomerId** | **String** |  | [optional] 
**InvoiceId** | **String** |  | 
**InvoiceNumber** | **String** |  | 
**OpenAmount** | **String** |  | 
**PaymentDate** | **String** |  | 
**PaymentId** | **String** |  | 
**Reason** | **String** |  | 
**Reference** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ProposedAssignment = Initialize-PSOpenAPIToolsProposedAssignment  -AmountPaid null `
 -Confidence null `
 -CustomerId null `
 -InvoiceId null `
 -InvoiceNumber null `
 -OpenAmount null `
 -PaymentDate null `
 -PaymentId null `
 -Reason null `
 -Reference null
```

- Convert the resource to JSON
```powershell
$ProposedAssignment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

