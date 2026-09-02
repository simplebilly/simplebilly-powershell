# PSOpenAPITools.PSOpenAPITools\Api.ReorderProposalApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ApplyReorderProposal**](ReorderProposalApi.md#Invoke-ApplyReorderProposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order.
[**Get-ReorderProposal**](ReorderProposalApi.md#Get-ReorderProposal) | **GET** /api/v1/reorder-proposals | 


<a id="Invoke-ApplyReorderProposal"></a>
# **Invoke-ApplyReorderProposal**
> AnyType Invoke-ApplyReorderProposal<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConfiguredOnly] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConfiguredOnly = $true # Boolean | Only include products with a reorder point configured (`min_stock`). (optional)
$WarehouseId = "MyWarehouseId" # String | Limit to a single warehouse id. (optional)

# Convert a reorder proposal into a draft purchase order.
try {
    $Result = Invoke-ApplyReorderProposal -ConfiguredOnly $ConfiguredOnly -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ApplyReorderProposal: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConfiguredOnly** | **Boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] 
 **WarehouseId** | **String**| Limit to a single warehouse id. | [optional] 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ReorderProposal"></a>
# **Get-ReorderProposal**
> ReorderProposalResponse Get-ReorderProposal<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConfiguredOnly] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConfiguredOnly = $true # Boolean | Only include products with a reorder point configured (`min_stock`). (optional)
$WarehouseId = "MyWarehouseId" # String | Limit to a single warehouse id. (optional)

try {
    $Result = Get-ReorderProposal -ConfiguredOnly $ConfiguredOnly -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Get-ReorderProposal: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConfiguredOnly** | **Boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] 
 **WarehouseId** | **String**| Limit to a single warehouse id. | [optional] 

### Return type

[**ReorderProposalResponse**](ReorderProposalResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

