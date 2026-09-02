# CustomerCommunicationCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **String** | The message body, call summary or note text. | [optional] 
**Channel** | [**CommunicationChannel**](CommunicationChannel.md) |  | 
**ContactId** | **String** | The contact (customer/supplier) this communication belongs to. References the contact entity. | 
**Counterparty** | **String** | Email/phone of the counterparty, if applicable. | [optional] 
**Direction** | [**CommunicationDirection**](CommunicationDirection.md) |  | 
**OccurredAt** | **System.DateTime** | When the communication happened (defaults to now on create). | [optional] 
**Subject** | **String** |  | [optional] 
**Tags** | [**AnyType**](.md) | Free-form tags, e.g. &#x60;[&quot;&quot;follow-up-required&quot;&quot;]&#x60;. | [optional] 

## Examples

- Prepare the resource
```powershell
$CustomerCommunicationCreate = Initialize-PSOpenAPIToolsCustomerCommunicationCreate  -Body null `
 -Channel null `
 -ContactId null `
 -Counterparty null `
 -Direction null `
 -OccurredAt null `
 -Subject null `
 -Tags null
```

- Convert the resource to JSON
```powershell
$CustomerCommunicationCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

