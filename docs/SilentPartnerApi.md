# PSOpenAPITools.PSOpenAPITools\Api.SilentPartnerApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-SilentPartner**](SilentPartnerApi.md#New-SilentPartner) | **POST** /api/v1/silent-partners | 
[**Invoke-DeleteSilentPartner**](SilentPartnerApi.md#Invoke-DeleteSilentPartner) | **DELETE** /api/v1/silent-partners/{id} | 
[**Get-SilentPartner**](SilentPartnerApi.md#Get-SilentPartner) | **GET** /api/v1/silent-partners/{id} | 
[**Get-SilentPartners**](SilentPartnerApi.md#Get-SilentPartners) | **GET** /api/v1/silent-partners/ | 
[**Update-SilentPartner**](SilentPartnerApi.md#Update-SilentPartner) | **PUT** /api/v1/silent-partners/{id} | 


<a id="New-SilentPartner"></a>
# **New-SilentPartner**
> SilentPartner New-SilentPartner<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SilentPartnerCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SilentPartnerCreate = Initialize-SilentPartnerCreate -ContractDate (Get-Date) -Einlage "MyEinlage" -GewinnquotePct "MyGewinnquotePct" -Gewinnvortrag "MyGewinnvortrag" -InstrumentType "typisch" -KestPflichtig $false -Name "MyName" -Notes "MyNotes" -VerlustVerrechnungskonto "MyVerlustVerrechnungskonto" -Verlustbeteiligung $false # SilentPartnerCreate | 

try {
    $Result = New-SilentPartner -SilentPartnerCreate $SilentPartnerCreate
} catch {
    Write-Host ("Exception occurred when calling New-SilentPartner: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SilentPartnerCreate** | [**SilentPartnerCreate**](SilentPartnerCreate.md)|  | 

### Return type

[**SilentPartner**](SilentPartner.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteSilentPartner"></a>
# **Invoke-DeleteSilentPartner**
> void Invoke-DeleteSilentPartner<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteSilentPartner -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteSilentPartner: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-SilentPartner"></a>
# **Get-SilentPartner**
> SilentPartner Get-SilentPartner<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-SilentPartner -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-SilentPartner: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**SilentPartner**](SilentPartner.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-SilentPartners"></a>
# **Get-SilentPartners**
> SilentPartner[] Get-SilentPartners<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IncludeDeleted] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 1 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$IncludeDeleted = $true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

try {
    $Result = Get-SilentPartners -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-SilentPartners: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **IncludeDeleted** | **Boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**SilentPartner[]**](SilentPartner.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-SilentPartner"></a>
# **Update-SilentPartner**
> SilentPartner Update-SilentPartner<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SilentPartnerUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$SilentPartnerUpdate = Initialize-SilentPartnerUpdate -ContractDate (Get-Date) -Einlage "MyEinlage" -GewinnquotePct "MyGewinnquotePct" -Gewinnvortrag "MyGewinnvortrag" -InstrumentType "typisch" -KestPflichtig $false -Name "MyName" -Notes "MyNotes" -VerlustVerrechnungskonto "MyVerlustVerrechnungskonto" -Verlustbeteiligung $false # SilentPartnerUpdate | 

try {
    $Result = Update-SilentPartner -Id $Id -SilentPartnerUpdate $SilentPartnerUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-SilentPartner: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **SilentPartnerUpdate** | [**SilentPartnerUpdate**](SilentPartnerUpdate.md)|  | 

### Return type

[**SilentPartner**](SilentPartner.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

