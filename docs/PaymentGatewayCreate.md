# PaymentGatewayCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Config** | [**AnyType**](.md) |  | 
**CreatedAt** | **System.DateTime** |  | 
**DeletedAt** | **System.DateTime** |  | [optional] 
**Enabled** | **Boolean** |  | 
**GatewayType** | [**GatewayType**](GatewayType.md) |  | 
**Label** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PaymentGatewayCreate = Initialize-PSOpenAPIToolsPaymentGatewayCreate  -Config null `
 -CreatedAt null `
 -DeletedAt null `
 -Enabled null `
 -GatewayType null `
 -Label null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$PaymentGatewayCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

