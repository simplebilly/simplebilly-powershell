# EmailTemplate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Body** | **String** | E-mail body with optional placeholders. | 
**Name** | **String** | Human-readable template name, e.g. &quot;&quot;Follow-up after quote&quot;&quot;. | 
**Status** | [**EmailTemplateStatus**](EmailTemplateStatus.md) | One of: active | inactive | 
**Subject** | **String** | E-mail subject line with optional placeholders. | 
**Variables** | [**AnyType**](.md) | Placeholders used by this template, e.g. &#x60;[&quot;&quot;contact.first_name&quot;&quot;]&#x60;. | [optional] 

## Examples

- Prepare the resource
```powershell
$EmailTemplate = Initialize-PSOpenAPIToolsEmailTemplate  -Body null `
 -Name null `
 -Status null `
 -Subject null `
 -Variables null
```

- Convert the resource to JSON
```powershell
$EmailTemplate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

