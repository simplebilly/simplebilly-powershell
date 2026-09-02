# OpenItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AmountDue** | **String** |  | 
**AmountPaid** | **String** |  | 
**CustomerId** | **String** |  | [optional] 
**DaysOverdue** | **Int64** |  | [optional] 
**DueDate** | **String** |  | [optional] 
**InvoiceId** | **String** |  | 
**InvoiceNumber** | **String** |  | 
**IssueDate** | **String** |  | 
**OpenAmount** | **String** |  | 
**ReminderLevel** | [**ReminderLevel**](ReminderLevel.md) |  | 

## Examples

- Prepare the resource
```powershell
$OpenItem = Initialize-PSOpenAPIToolsOpenItem  -AmountDue null `
 -AmountPaid null `
 -CustomerId null `
 -DaysOverdue null `
 -DueDate null `
 -InvoiceId null `
 -InvoiceNumber null `
 -IssueDate null `
 -OpenAmount null `
 -ReminderLevel null
```

- Convert the resource to JSON
```powershell
$OpenItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

