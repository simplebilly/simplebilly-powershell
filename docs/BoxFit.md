# BoxFit
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**HeightCm** | **Double** |  | 
**ItemCount** | **Int32** |  | 
**LengthCm** | **Double** |  | 
**VolumeCm3** | **Double** |  | 
**WidthCm** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$BoxFit = Initialize-PSOpenAPIToolsBoxFit  -HeightCm null `
 -ItemCount null `
 -LengthCm null `
 -VolumeCm3 null `
 -WidthCm null
```

- Convert the resource to JSON
```powershell
$BoxFit | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

