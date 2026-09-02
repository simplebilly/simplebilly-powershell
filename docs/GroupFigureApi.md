# PSOpenAPITools.PSOpenAPITools\Api.GroupFigureApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-GroupFigure**](GroupFigureApi.md#New-GroupFigure) | **POST** /api/v1/group-figures | 
[**Invoke-DeleteGroupFigure**](GroupFigureApi.md#Invoke-DeleteGroupFigure) | **DELETE** /api/v1/group-figures/{year} | 
[**Get-GroupFigure**](GroupFigureApi.md#Get-GroupFigure) | **GET** /api/v1/group-figures/{year} | 
[**Get-GroupFigures**](GroupFigureApi.md#Get-GroupFigures) | **GET** /api/v1/group-figures/ | 
[**Update-GroupFigure**](GroupFigureApi.md#Update-GroupFigure) | **PUT** /api/v1/group-figures/{year} | 


<a id="New-GroupFigure"></a>
# **New-GroupFigure**
> GroupFigure New-GroupFigure<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GroupFigureCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GroupFigureCreate = Initialize-GroupFigureCreate -Bilanzsumme "MyBilanzsumme" -ExemptionClaimed $false -Mitarbeiter 0 -NettoUmsatz "MyNettoUmsatz" -ParentName "MyParentName" -ParentSitus "MyParentSitus" # GroupFigureCreate | 

try {
    $Result = New-GroupFigure -GroupFigureCreate $GroupFigureCreate
} catch {
    Write-Host ("Exception occurred when calling New-GroupFigure: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GroupFigureCreate** | [**GroupFigureCreate**](GroupFigureCreate.md)|  | 

### Return type

[**GroupFigure**](GroupFigure.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteGroupFigure"></a>
# **Invoke-DeleteGroupFigure**
> void Invoke-DeleteGroupFigure<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-DeleteGroupFigure -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteGroupFigure: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-GroupFigure"></a>
# **Get-GroupFigure**
> GroupFigure Get-GroupFigure<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Get-GroupFigure -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Get-GroupFigure: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**GroupFigure**](GroupFigure.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-GroupFigures"></a>
# **Get-GroupFigures**
> GroupFigure[] Get-GroupFigures<br>
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
    $Result = Get-GroupFigures -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-GroupFigures: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**GroupFigure[]**](GroupFigure.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-GroupFigure"></a>
# **Update-GroupFigure**
> GroupFigure Update-GroupFigure<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GroupFigureUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 
$GroupFigureUpdate = Initialize-GroupFigureUpdate -Bilanzsumme "MyBilanzsumme" -ExemptionClaimed $false -Mitarbeiter 0 -NettoUmsatz "MyNettoUmsatz" -ParentName "MyParentName" -ParentSitus "MyParentSitus" # GroupFigureUpdate | 

try {
    $Result = Update-GroupFigure -Year $Year -GroupFigureUpdate $GroupFigureUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-GroupFigure: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 
 **GroupFigureUpdate** | [**GroupFigureUpdate**](GroupFigureUpdate.md)|  | 

### Return type

[**GroupFigure**](GroupFigure.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

