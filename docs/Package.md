# Package
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **String** |  | [optional] 
**HeightCm** | **Double** |  | [optional] 
**LengthCm** | **Double** |  | [optional] 
**Reference** | **String** |  | [optional] 
**WeightKg** | **Double** |  | 
**WidthCm** | **Double** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Package = Initialize-PSOpenAPIToolsPackage  -Description null `
 -HeightCm null `
 -LengthCm null `
 -Reference null `
 -WeightKg null `
 -WidthCm null
```

- Convert the resource to JSON
```powershell
$Package | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

