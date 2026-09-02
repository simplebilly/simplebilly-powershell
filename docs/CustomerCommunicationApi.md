# PSOpenAPITools.PSOpenAPITools\Api.CustomerCommunicationApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Communication**](CustomerCommunicationApi.md#New-Communication) | **POST** /api/v1/communications | 
[**Invoke-CustomercommunicationRestore**](CustomerCommunicationApi.md#Invoke-CustomercommunicationRestore) | **POST** /api/v1/communications/{communication_id}/restore | 
[**Invoke-DeleteCommunication**](CustomerCommunicationApi.md#Invoke-DeleteCommunication) | **DELETE** /api/v1/communications/{communication_id} | 
[**Get-Communication**](CustomerCommunicationApi.md#Get-Communication) | **GET** /api/v1/communications/{communication_id} | 
[**Get-ContactHistory**](CustomerCommunicationApi.md#Get-ContactHistory) | **GET** /api/v1/contacts/{contact_id}/communications | 
[**Invoke-ListCommunications**](CustomerCommunicationApi.md#Invoke-ListCommunications) | **GET** /api/v1/communications/ | 
[**Update-Communication**](CustomerCommunicationApi.md#Update-Communication) | **PUT** /api/v1/communications/{communication_id} | 


<a id="New-Communication"></a>
# **New-Communication**
> CustomerCommunication New-Communication<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerCommunicationCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerCommunicationCreate = Initialize-CustomerCommunicationCreate -Body "MyBody" -Channel "email" -ContactId "MyContactId" -Counterparty "MyCounterparty" -Direction "inbound" -OccurredAt (Get-Date) -Subject "MySubject" -Tags # CustomerCommunicationCreate | 

try {
    $Result = New-Communication -CustomerCommunicationCreate $CustomerCommunicationCreate
} catch {
    Write-Host ("Exception occurred when calling New-Communication: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerCommunicationCreate** | [**CustomerCommunicationCreate**](CustomerCommunicationCreate.md)|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-CustomercommunicationRestore"></a>
# **Invoke-CustomercommunicationRestore**
> CustomerCommunication Invoke-CustomercommunicationRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CommunicationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CommunicationId = "MyCommunicationId" # String | 

try {
    $Result = Invoke-CustomercommunicationRestore -CommunicationId $CommunicationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-CustomercommunicationRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CommunicationId** | **String**|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteCommunication"></a>
# **Invoke-DeleteCommunication**
> void Invoke-DeleteCommunication<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CommunicationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CommunicationId = "MyCommunicationId" # String | 

try {
    $Result = Invoke-DeleteCommunication -CommunicationId $CommunicationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteCommunication: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CommunicationId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Communication"></a>
# **Get-Communication**
> CustomerCommunication Get-Communication<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CommunicationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CommunicationId = "MyCommunicationId" # String | 

try {
    $Result = Get-Communication -CommunicationId $CommunicationId
} catch {
    Write-Host ("Exception occurred when calling Get-Communication: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CommunicationId** | **String**|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ContactHistory"></a>
# **Get-ContactHistory**
> ContactHistoryResponse Get-ContactHistory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ContactId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ContactId = "MyContactId" # String | 

try {
    $Result = Get-ContactHistory -ContactId $ContactId
} catch {
    Write-Host ("Exception occurred when calling Get-ContactHistory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ContactId** | **String**|  | 

### Return type

[**ContactHistoryResponse**](ContactHistoryResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListCommunications"></a>
# **Invoke-ListCommunications**
> CustomerCommunication[] Invoke-ListCommunications<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ContactId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Channel] <PSCustomObject><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Direction] <PSCustomObject><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-From] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-To] <System.Nullable[System.DateTime]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ContactId = "MyContactId" # String | Filter history to a single contact. (optional)
$Channel = "email" # CommunicationChannel |  (optional)
$Direction = "inbound" # CommunicationDirection |  (optional)
$From = (Get-Date) # System.DateTime | Only include communications after this ISO date (inclusive). (optional)
$To = (Get-Date) # System.DateTime | Only include communications before this ISO date (inclusive). (optional)

try {
    $Result = Invoke-ListCommunications -Page $Page -PageSize $PageSize -ContactId $ContactId -Channel $Channel -Direction $Direction -From $From -To $To
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListCommunications: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **ContactId** | **String**| Filter history to a single contact. | [optional] 
 **Channel** | [**CommunicationChannel**](CommunicationChannel.md)|  | [optional] 
 **Direction** | [**CommunicationDirection**](CommunicationDirection.md)|  | [optional] 
 **From** | **System.DateTime**| Only include communications after this ISO date (inclusive). | [optional] 
 **To** | **System.DateTime**| Only include communications before this ISO date (inclusive). | [optional] 

### Return type

[**CustomerCommunication[]**](CustomerCommunication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Communication"></a>
# **Update-Communication**
> CustomerCommunication Update-Communication<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CommunicationId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerCommunicationUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CommunicationId = "MyCommunicationId" # String | 
$CustomerCommunicationUpdate = Initialize-CustomerCommunicationUpdate -Body "MyBody" -Channel "email" -ContactId "MyContactId" -Counterparty "MyCounterparty" -Direction "inbound" -OccurredAt (Get-Date) -Subject "MySubject" -Tags # CustomerCommunicationUpdate | 

try {
    $Result = Update-Communication -CommunicationId $CommunicationId -CustomerCommunicationUpdate $CustomerCommunicationUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-Communication: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CommunicationId** | **String**|  | 
 **CustomerCommunicationUpdate** | [**CustomerCommunicationUpdate**](CustomerCommunicationUpdate.md)|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

