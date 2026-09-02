# PaymentGateway
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Config** | [**AnyType**](.md) |  | 
**CreatedAt** | **System.DateTime** |  | 
**DeletedAt** | **System.DateTime** |  | [optional] 
**Enabled** | **Boolean** |  | 
**GatewayId** | **String** |  | 
**GatewayType** | [**GatewayType**](GatewayType.md) |  | 
**Label** | **String** |  | 
**TenantId** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PaymentGateway = Initialize-PSOpenAPIToolsPaymentGateway  -Config null `
 -CreatedAt null `
 -DeletedAt null `
 -Enabled null `
 -GatewayId null `
 -GatewayType null `
 -Label null `
 -TenantId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$PaymentGateway | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

