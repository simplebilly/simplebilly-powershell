# CustomerCommunicationUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **String** | The message body, call summary or note text. | [optional] 
**Channel** | [**CommunicationChannel**](CommunicationChannel.md) |  | [optional] 
**ContactId** | **String** | The contact (customer/supplier) this communication belongs to. References the contact entity. | [optional] 
**Counterparty** | **String** | Email/phone of the counterparty, if applicable. | [optional] 
**Direction** | [**CommunicationDirection**](CommunicationDirection.md) |  | [optional] 
**OccurredAt** | **System.DateTime** | When the communication happened (defaults to now on create). | [optional] 
**Subject** | **String** |  | [optional] 
**Tags** | [**AnyType**](.md) | Free-form tags, e.g. &#x60;[&quot;&quot;follow-up-required&quot;&quot;]&#x60;. | [optional] 

## Examples

- Prepare the resource
```powershell
$CustomerCommunicationUpdate = Initialize-PSOpenAPIToolsCustomerCommunicationUpdate  -Body null `
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
$CustomerCommunicationUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

