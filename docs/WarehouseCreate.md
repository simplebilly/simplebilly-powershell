# WarehouseCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AddressCity** | **String** |  | [optional] 
**AddressCountry** | [**CountryCode**](CountryCode.md) |  | [optional] 
**AddressStreet** | **String** |  | [optional] 
**AddressZip** | **String** |  | [optional] 
**BinLocations** | [**AnyType**](.md) | JSON array of bin locations, e.g. &#x60;[&quot;&quot;A-01-01&quot;&quot;, &quot;&quot;A-01-02&quot;&quot;]&#x60;. | [optional] 
**Code** | **String** |  | 
**IsActive** | **Boolean** |  | [optional] 
**IsDefault** | **Boolean** |  | [optional] 
**Name** | **String** |  | 
**Notes** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$WarehouseCreate = Initialize-PSOpenAPIToolsWarehouseCreate  -AddressCity null `
 -AddressCountry null `
 -AddressStreet null `
 -AddressZip null `
 -BinLocations null `
 -Code null `
 -IsActive null `
 -IsDefault null `
 -Name null `
 -Notes null
```

- Convert the resource to JSON
```powershell
$WarehouseCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

