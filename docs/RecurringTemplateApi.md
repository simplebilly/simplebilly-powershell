# PSOpenAPITools.PSOpenAPITools\Api.RecurringTemplateApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-RecurringTemplate**](RecurringTemplateApi.md#New-RecurringTemplate) | **POST** /api/v1/recurring-templates | 
[**Invoke-DeleteRecurringTemplate**](RecurringTemplateApi.md#Invoke-DeleteRecurringTemplate) | **DELETE** /api/v1/recurring-templates/{template_id} | 
[**Get-RecurringTemplate**](RecurringTemplateApi.md#Get-RecurringTemplate) | **GET** /api/v1/recurring-templates/{template_id} | 
[**Invoke-ListRecurringTemplates**](RecurringTemplateApi.md#Invoke-ListRecurringTemplates) | **GET** /api/v1/recurring-templates/ | 


<a id="New-RecurringTemplate"></a>
# **New-RecurringTemplate**
> RecurringTemplate New-RecurringTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = New-RecurringTemplate -Body $Body
} catch {
    Write-Host ("Exception occurred when calling New-RecurringTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**RecurringTemplate**](RecurringTemplate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteRecurringTemplate"></a>
# **Invoke-DeleteRecurringTemplate**
> void Invoke-DeleteRecurringTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TemplateId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TemplateId = "MyTemplateId" # String | 

try {
    $Result = Invoke-DeleteRecurringTemplate -TemplateId $TemplateId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteRecurringTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TemplateId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-RecurringTemplate"></a>
# **Get-RecurringTemplate**
> RecurringTemplate Get-RecurringTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TemplateId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TemplateId = "MyTemplateId" # String | 

try {
    $Result = Get-RecurringTemplate -TemplateId $TemplateId
} catch {
    Write-Host ("Exception occurred when calling Get-RecurringTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TemplateId** | **String**|  | 

### Return type

[**RecurringTemplate**](RecurringTemplate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListRecurringTemplates"></a>
# **Invoke-ListRecurringTemplates**
> RecurringTemplate[] Invoke-ListRecurringTemplates<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListRecurringTemplates
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListRecurringTemplates: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**RecurringTemplate[]**](RecurringTemplate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

