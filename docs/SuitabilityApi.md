# PSOpenAPITools.PSOpenAPITools\Api.SuitabilityApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ShippingSuitabilityApi**](SuitabilityApi.md#Invoke-ShippingSuitabilityApi) | **POST** /api/v1/shipping/suitability | 


<a id="Invoke-ShippingSuitabilityApi"></a>
# **Invoke-ShippingSuitabilityApi**
> SuitabilityResult Invoke-ShippingSuitabilityApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SuitabilityRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CartItemInput = Initialize-CartItemInput -ProductId "MyProductId" -Quantity 0
$Address = Initialize-Address -City "MyCity" -Company "MyCompany" -Country "MyCountry" -Email "MyEmail" -Name "MyName" -Phone "MyPhone" -Street "MyStreet" -StreetNumber "MyStreetNumber" -Zip "MyZip"
$SuitabilityRequest = Initialize-SuitabilityRequest -CustomerAnnualVolume 0 -Items $CartItemInput -Recipient $Address -VarSender $Address # SuitabilityRequest | 

try {
    $Result = Invoke-ShippingSuitabilityApi -SuitabilityRequest $SuitabilityRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-ShippingSuitabilityApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SuitabilityRequest** | [**SuitabilityRequest**](SuitabilityRequest.md)|  | 

### Return type

[**SuitabilityResult**](SuitabilityResult.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

