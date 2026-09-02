# PaymentGatewayUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Config** | [**AnyType**](.md) |  | [optional] 
**CreatedAt** | **System.DateTime** |  | [optional] 
**DeletedAt** | **System.DateTime** |  | [optional] 
**Enabled** | **Boolean** |  | [optional] 
**GatewayType** | [**GatewayType**](GatewayType.md) |  | [optional] 
**Label** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PaymentGatewayUpdate = Initialize-PSOpenAPIToolsPaymentGatewayUpdate  -Config null `
 -CreatedAt null `
 -DeletedAt null `
 -Enabled null `
 -GatewayType null `
 -Label null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$PaymentGatewayUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

