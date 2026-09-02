# Payment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **String** |  | [optional] 
**Attachment** | [**AnyType**](.md) |  | [optional] 
**Currency** | **String** |  | [optional] 
**CustomerId** | **String** | References the customer entity. | [optional] 
**Description** | **String** |  | [optional] 
**Metadata** | [**AnyType**](.md) |  | [optional] 
**Method** | [**PaymentMethod**](PaymentMethod.md) |  | [optional] 
**PaymentDate** | **System.DateTime** |  | [optional] 
**Reference** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Payment = Initialize-PSOpenAPIToolsPayment  -Amount null `
 -Attachment null `
 -Currency null `
 -CustomerId null `
 -Description null `
 -Metadata null `
 -Method null `
 -PaymentDate null `
 -Reference null
```

- Convert the resource to JSON
```powershell
$Payment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

