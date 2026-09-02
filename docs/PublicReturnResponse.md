# PublicReturnResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**Items** | [**AnyType**](.md) |  | 
**Notes** | **String** |  | [optional] 
**OrderNumber** | **String** |  | [optional] 
**ReturnNumber** | **String** |  | 
**ReturnOrderId** | **String** |  | 
**Status** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PublicReturnResponse = Initialize-PSOpenAPIToolsPublicReturnResponse  -CreatedAt null `
 -Items null `
 -Notes null `
 -OrderNumber null `
 -ReturnNumber null `
 -ReturnOrderId null `
 -Status null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$PublicReturnResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

