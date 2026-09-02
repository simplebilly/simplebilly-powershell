# PSOpenAPITools.PSOpenAPITools\Api.ShippingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-CredentialsApi**](ShippingApi.md#Get-CredentialsApi) | **GET** /api/v1/shipping/credentials | 
[**Get-RatesApi**](ShippingApi.md#Get-RatesApi) | **POST** /api/v1/shipping/rates | 
[**Invoke-ListProvidersApi**](ShippingApi.md#Invoke-ListProvidersApi) | **GET** /api/v1/shipping/providers | 
[**Save-CredentialsApi**](ShippingApi.md#Save-CredentialsApi) | **PUT** /api/v1/shipping/credentials | 


<a id="Get-CredentialsApi"></a>
# **Get-CredentialsApi**
> ShippingCredentials Get-CredentialsApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Get-CredentialsApi
} catch {
    Write-Host ("Exception occurred when calling Get-CredentialsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ShippingCredentials**](ShippingCredentials.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-RatesApi"></a>
# **Get-RatesApi**
> RateResponse Get-RatesApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RateRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerInfo = Initialize-CustomerInfo -AnnualVolume 0 -IsRegistered $false
$Package = Initialize-Package -Description "MyDescription" -HeightCm 0 -LengthCm 0 -Reference "MyReference" -WeightKg 0 -WidthCm 0
$Address = Initialize-Address -City "MyCity" -Company "MyCompany" -Country "MyCountry" -Email "MyEmail" -Name "MyName" -Phone "MyPhone" -Street "MyStreet" -StreetNumber "MyStreetNumber" -Zip "MyZip"
$RateRequest = Initialize-RateRequest -Customer $CustomerInfo -Packages $Package -Recipient $Address -VarSender $Address # RateRequest | 

try {
    $Result = Get-RatesApi -RateRequest $RateRequest
} catch {
    Write-Host ("Exception occurred when calling Get-RatesApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RateRequest** | [**RateRequest**](RateRequest.md)|  | 

### Return type

[**RateResponse**](RateResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListProvidersApi"></a>
# **Invoke-ListProvidersApi**
> ProviderInfo[] Invoke-ListProvidersApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListProvidersApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListProvidersApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ProviderInfo[]**](ProviderInfo.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Save-CredentialsApi"></a>
# **Save-CredentialsApi**
> ShippingCredentials Save-CredentialsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShippingCredentials] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DhlCredentials = Initialize-DhlCredentials -ApiKey "MyApiKey" -ClientId "MyClientId" -ClientSecret "MyClientSecret"
$UpsCredentials = Initialize-UpsCredentials -ClientId "MyClientId" -ClientSecret "MyClientSecret" -ShipperNumber "MyShipperNumber"
$ShippingCredentials = Initialize-ShippingCredentials -Dhl $DhlCredentials -Ups $UpsCredentials # ShippingCredentials | 

try {
    $Result = Save-CredentialsApi -ShippingCredentials $ShippingCredentials
} catch {
    Write-Host ("Exception occurred when calling Save-CredentialsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ShippingCredentials** | [**ShippingCredentials**](ShippingCredentials.md)|  | 

### Return type

[**ShippingCredentials**](ShippingCredentials.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

