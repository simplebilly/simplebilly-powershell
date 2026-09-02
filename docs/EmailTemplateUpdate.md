# EmailTemplateUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **String** | E-mail body with optional placeholders. | [optional] 
**Name** | **String** | Human-readable template name, e.g. &quot;&quot;Follow-up after quote&quot;&quot;. | [optional] 
**Status** | [**EmailTemplateStatus**](EmailTemplateStatus.md) | One of: active | inactive | [optional] 
**Subject** | **String** | E-mail subject line with optional placeholders. | [optional] 
**Variables** | [**AnyType**](.md) | Placeholders used by this template, e.g. &#x60;[&quot;&quot;contact.first_name&quot;&quot;]&#x60;. | [optional] 

## Examples

- Prepare the resource
```powershell
$EmailTemplateUpdate = Initialize-PSOpenAPIToolsEmailTemplateUpdate  -Body null `
 -Name null `
 -Status null `
 -Subject null `
 -Variables null
```

- Convert the resource to JSON
```powershell
$EmailTemplateUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

