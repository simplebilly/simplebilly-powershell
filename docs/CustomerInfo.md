# CustomerInfo
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AnnualVolume** | **Int32** |  | 
**IsRegistered** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$CustomerInfo = Initialize-PSOpenAPIToolsCustomerInfo  -AnnualVolume null `
 -IsRegistered null
```

- Convert the resource to JSON
```powershell
$CustomerInfo | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

