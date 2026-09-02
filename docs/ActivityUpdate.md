# ActivityUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActivityType** | [**ActivityType**](ActivityType.md) | One of: call | email | meeting | task | note | [optional] 
**AssignedTo** | **String** | User responsible (&#x60;employee.employee_id&#x60;). | [optional] 
**ContactId** | **String** | Contact this activity belongs to (&#x60;contact.contact_id&#x60;). References the contact entity. | [optional] 
**Description** | **String** |  | [optional] 
**DueDate** | **System.DateTime** | Follow-up / Wiedervorlage date. Open activities with a due date in the past are overdue. | [optional] 
**ReminderDate** | **System.DateTime** | When to remind about the follow-up. | [optional] 
**Status** | [**ActivityStatus**](ActivityStatus.md) | One of: open | done | cancelled | [optional] 
**Subject** | **String** | Short subject line. | [optional] 

## Examples

- Prepare the resource
```powershell
$ActivityUpdate = Initialize-PSOpenAPIToolsActivityUpdate  -ActivityType null `
 -AssignedTo null `
 -ContactId null `
 -Description null `
 -DueDate null `
 -ReminderDate null `
 -Status null `
 -Subject null
```

- Convert the resource to JSON
```powershell
$ActivityUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

