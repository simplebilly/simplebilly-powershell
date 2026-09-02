# ComplianceTraining
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Assignable** | **Boolean** | Whether HR can assign this training as required for employees. | [optional] 
**Code** | **String** | Stable code used by plugins and frontend players (e.g. &quot;&quot;data_privacy&quot;&quot;). | [optional] 
**CreatedAt** | **System.DateTime** |  | [optional] 
**DeletedAt** | **System.DateTime** |  | [optional] 
**Description** | **String** |  | [optional] 
**Id** | **String** |  | [optional] 
**PassScore** | **Int32** | Minimum score (0–100) required to pass. | [optional] 
**PluginPlatform** | **String** | Marketplace plugin platform id when source &#x3D; Plugin. | [optional] 
**Source** | [**TrainingSource**](TrainingSource.md) |  | [optional] 
**TenantId** | **String** |  | [optional] 
**Title** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | [optional] 
**ValidityMonths** | **Int32** | Certificate validity in months; null &#x3D; no expiry. | [optional] 

## Examples

- Prepare the resource
```powershell
$ComplianceTraining = Initialize-PSOpenAPIToolsComplianceTraining  -Assignable null `
 -Code null `
 -CreatedAt null `
 -DeletedAt null `
 -Description null `
 -Id null `
 -PassScore null `
 -PluginPlatform null `
 -Source null `
 -TenantId null `
 -Title null `
 -UpdatedAt null `
 -ValidityMonths null
```

- Convert the resource to JSON
```powershell
$ComplianceTraining | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

