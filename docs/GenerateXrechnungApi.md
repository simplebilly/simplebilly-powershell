# PSOpenAPITools.PSOpenAPITools\Api.GenerateXrechnungApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-XrechnungApi**](GenerateXrechnungApi.md#New-XrechnungApi) | **GET** /api/v1/invoices/{id}/xrechnung | 


<a id="New-XrechnungApi"></a>
# **New-XrechnungApi**
> XRechnungResponse New-XrechnungApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierStreet] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierCity] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierZip] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierCountry] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierVatId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 
$SupplierName = "MySupplierName" # String |  (optional)
$SupplierStreet = "MySupplierStreet" # String |  (optional)
$SupplierCity = "MySupplierCity" # String |  (optional)
$SupplierZip = "MySupplierZip" # String |  (optional)
$SupplierCountry = "MySupplierCountry" # String |  (optional)
$SupplierVatId = "MySupplierVatId" # String |  (optional)

try {
    $Result = New-XrechnungApi -Id $Id -SupplierName $SupplierName -SupplierStreet $SupplierStreet -SupplierCity $SupplierCity -SupplierZip $SupplierZip -SupplierCountry $SupplierCountry -SupplierVatId $SupplierVatId
} catch {
    Write-Host ("Exception occurred when calling New-XrechnungApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **SupplierName** | **String**|  | [optional] 
 **SupplierStreet** | **String**|  | [optional] 
 **SupplierCity** | **String**|  | [optional] 
 **SupplierZip** | **String**|  | [optional] 
 **SupplierCountry** | **String**|  | [optional] 
 **SupplierVatId** | **String**|  | [optional] 

### Return type

[**XRechnungResponse**](XRechnungResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

