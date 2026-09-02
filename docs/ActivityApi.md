# PSOpenAPITools.PSOpenAPITools\Api.ActivityApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Activity**](ActivityApi.md#New-Activity) | **POST** /api/v1/activities | 
[**Invoke-DeleteActivity**](ActivityApi.md#Invoke-DeleteActivity) | **DELETE** /api/v1/activities/{activity_id} | 
[**Get-Activity**](ActivityApi.md#Get-Activity) | **GET** /api/v1/activities/{activity_id} | 
[**Invoke-ListActivities**](ActivityApi.md#Invoke-ListActivities) | **GET** /api/v1/activities/ | 
[**Update-Activity**](ActivityApi.md#Update-Activity) | **PUT** /api/v1/activities/{activity_id} | 
[**Update-ActivityStatus**](ActivityApi.md#Update-ActivityStatus) | **PUT** /api/v1/activities/{activity_id}/status | 


<a id="New-Activity"></a>
# **New-Activity**
> Activity New-Activity<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Activity] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Activity = Initialize-Activity -ActivityType "call" -AssignedTo "MyAssignedTo" -ContactId "MyContactId" -Description "MyDescription" -DueDate (Get-Date) -ReminderDate (Get-Date) -Status "open" -Subject "MySubject" # Activity | 

try {
    $Result = New-Activity -Activity $Activity
} catch {
    Write-Host ("Exception occurred when calling New-Activity: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Activity** | [**Activity**](Activity.md)|  | 

### Return type

[**Activity**](Activity.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteActivity"></a>
# **Invoke-DeleteActivity**
> void Invoke-DeleteActivity<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ActivityId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ActivityId = "MyActivityId" # String | 

try {
    $Result = Invoke-DeleteActivity -ActivityId $ActivityId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteActivity: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ActivityId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Activity"></a>
# **Get-Activity**
> Activity Get-Activity<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ActivityId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ActivityId = "MyActivityId" # String | 

try {
    $Result = Get-Activity -ActivityId $ActivityId
} catch {
    Write-Host ("Exception occurred when calling Get-Activity: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ActivityId** | **String**|  | 

### Return type

[**Activity**](Activity.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListActivities"></a>
# **Invoke-ListActivities**
> Activity[] Invoke-ListActivities<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ContactId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ActivityType] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AssignedTo] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OverdueOnly] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ContactId = "MyContactId" # String |  (optional)
$ActivityType = "MyActivityType" # String |  (optional)
$Status = "MyStatus" # String |  (optional)
$AssignedTo = "MyAssignedTo" # String |  (optional)
$OverdueOnly = $true # Boolean | Only show overdue follow-ups. (optional)

try {
    $Result = Invoke-ListActivities -Page $Page -PageSize $PageSize -ContactId $ContactId -ActivityType $ActivityType -Status $Status -AssignedTo $AssignedTo -OverdueOnly $OverdueOnly
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListActivities: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **ContactId** | **String**|  | [optional] 
 **ActivityType** | **String**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **AssignedTo** | **String**|  | [optional] 
 **OverdueOnly** | **Boolean**| Only show overdue follow-ups. | [optional] 

### Return type

[**Activity[]**](Activity.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Activity"></a>
# **Update-Activity**
> Activity Update-Activity<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ActivityId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ActivityId = "MyActivityId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-Activity -ActivityId $ActivityId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-Activity: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ActivityId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**Activity**](Activity.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ActivityStatus"></a>
# **Update-ActivityStatus**
> Activity Update-ActivityStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ActivityId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ActivityStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ActivityId = "MyActivityId" # String | 
$ActivityStatusUpdate = Initialize-ActivityStatusUpdate -Status "MyStatus" # ActivityStatusUpdate | 

try {
    $Result = Update-ActivityStatus -ActivityId $ActivityId -ActivityStatusUpdate $ActivityStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ActivityStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ActivityId** | **String**|  | 
 **ActivityStatusUpdate** | [**ActivityStatusUpdate**](ActivityStatusUpdate.md)|  | 

### Return type

[**Activity**](Activity.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

