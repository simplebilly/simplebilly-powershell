# RateRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Customer** | [**CustomerInfo**](CustomerInfo.md) |  | [optional] 
**Packages** | [**Package[]**](Package.md) |  | 
**Recipient** | [**Address**](Address.md) |  | 
**VarSender** | [**Address**](Address.md) |  | 

## Examples

- Prepare the resource
```powershell
$RateRequest = Initialize-PSOpenAPIToolsRateRequest  -Customer null `
 -Packages null `
 -Recipient null `
 -VarSender null
```

- Convert the resource to JSON
```powershell
$RateRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

