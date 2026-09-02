# PSOpenAPITools.PSOpenAPITools\Api.ParticipationApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Participation**](ParticipationApi.md#New-Participation) | **POST** /api/v1/participations | 
[**Invoke-DeleteParticipation**](ParticipationApi.md#Invoke-DeleteParticipation) | **DELETE** /api/v1/participations/{id} | 
[**Get-Participation**](ParticipationApi.md#Get-Participation) | **GET** /api/v1/participations/{id} | 
[**Get-Participations**](ParticipationApi.md#Get-Participations) | **GET** /api/v1/participations/ | 
[**Update-Participation**](ParticipationApi.md#Update-Participation) | **PUT** /api/v1/participations/{id} | 


<a id="New-Participation"></a>
# **New-Participation**
> Participation New-Participation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ParticipationCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ParticipationCreate = Initialize-ParticipationCreate -AcquiredAt (Get-Date) -BoardAppointment $false -CompanyName "MyCompanyName" -ControlAgreement $false -LegalForm "MyLegalForm" -OwnershipPct "MyOwnershipPct" -PurposeVehicle $false -VotingMajority $false # ParticipationCreate | 

try {
    $Result = New-Participation -ParticipationCreate $ParticipationCreate
} catch {
    Write-Host ("Exception occurred when calling New-Participation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ParticipationCreate** | [**ParticipationCreate**](ParticipationCreate.md)|  | 

### Return type

[**Participation**](Participation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteParticipation"></a>
# **Invoke-DeleteParticipation**
> void Invoke-DeleteParticipation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteParticipation -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteParticipation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Get-Participation"></a>
# **Get-Participation**
> Participation Get-Participation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-Participation -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-Participation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**Participation**](Participation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Participations"></a>
# **Get-Participations**
> Participation[] Get-Participations<br>
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
    $Result = Get-Participations -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-Participations: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**Participation[]**](Participation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Participation"></a>
# **Update-Participation**
> Participation Update-Participation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ParticipationUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ParticipationUpdate = Initialize-ParticipationUpdate -AcquiredAt (Get-Date) -BoardAppointment $false -CompanyName "MyCompanyName" -ControlAgreement $false -LegalForm "MyLegalForm" -OwnershipPct "MyOwnershipPct" -PurposeVehicle $false -VotingMajority $false # ParticipationUpdate | 

try {
    $Result = Update-Participation -Id $Id -ParticipationUpdate $ParticipationUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-Participation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **ParticipationUpdate** | [**ParticipationUpdate**](ParticipationUpdate.md)|  | 

### Return type

[**Participation**](Participation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

