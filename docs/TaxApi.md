# PSOpenAPITools.PSOpenAPITools\Api.TaxApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-TaxRate**](TaxApi.md#New-TaxRate) | **POST** /api/v1/tax-rates | Create a tax rate (&#x60;admin:settings&#x60;).
[**Invoke-DeleteTaxRate**](TaxApi.md#Invoke-DeleteTaxRate) | **DELETE** /api/v1/tax-rates/{id} | Delete a tax rate by id (&#x60;admin:settings&#x60;).
[**Invoke-ListTaxRates**](TaxApi.md#Invoke-ListTaxRates) | **GET** /api/v1/tax-rates | List the calling tenant&#39;s tax rates.
[**Update-TaxRate**](TaxApi.md#Update-TaxRate) | **PUT** /api/v1/tax-rates/{id} | Update a tax rate by id (&#x60;admin:settings&#x60;). Replaces all body fields.


<a id="New-TaxRate"></a>
# **New-TaxRate**
> void New-TaxRate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TaxRateCreate] <PSCustomObject><br>

Create a tax rate (`admin:settings`).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TaxRateCreate = Initialize-TaxRateCreate -CountryCode "MyCountryCode" -EffectiveFrom (Get-Date) -IsDefault $false -Name "MyName" -RatePercent 0 # TaxRateCreate | 

# Create a tax rate (`admin:settings`).
try {
    $Result = New-TaxRate -TaxRateCreate $TaxRateCreate
} catch {
    Write-Host ("Exception occurred when calling New-TaxRate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TaxRateCreate** | [**TaxRateCreate**](TaxRateCreate.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteTaxRate"></a>
# **Invoke-DeleteTaxRate**
> void Invoke-DeleteTaxRate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>

Delete a tax rate by id (`admin:settings`).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

# Delete a tax rate by id (`admin:settings`).
try {
    $Result = Invoke-DeleteTaxRate -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteTaxRate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListTaxRates"></a>
# **Invoke-ListTaxRates**
> void Invoke-ListTaxRates<br>

List the calling tenant's tax rates.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List the calling tenant's tax rates.
try {
    $Result = Invoke-ListTaxRates
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListTaxRates: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-TaxRate"></a>
# **Update-TaxRate**
> void Update-TaxRate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TaxRateCreate] <PSCustomObject><br>

Update a tax rate by id (`admin:settings`). Replaces all body fields.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$TaxRateCreate = Initialize-TaxRateCreate -CountryCode "MyCountryCode" -EffectiveFrom (Get-Date) -IsDefault $false -Name "MyName" -RatePercent 0 # TaxRateCreate | 

# Update a tax rate by id (`admin:settings`). Replaces all body fields.
try {
    $Result = Update-TaxRate -Id $Id -TaxRateCreate $TaxRateCreate
} catch {
    Write-Host ("Exception occurred when calling Update-TaxRate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **TaxRateCreate** | [**TaxRateCreate**](TaxRateCreate.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

