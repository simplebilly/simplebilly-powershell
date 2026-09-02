# PSOpenAPITools.PSOpenAPITools\Api.EmailTemplateApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-EmailTemplate**](EmailTemplateApi.md#New-EmailTemplate) | **POST** /api/v1/email-templates | 
[**Invoke-DeleteEmailTemplate**](EmailTemplateApi.md#Invoke-DeleteEmailTemplate) | **DELETE** /api/v1/email-templates/{email_template_id} | 
[**Get-EmailTemplate**](EmailTemplateApi.md#Get-EmailTemplate) | **GET** /api/v1/email-templates/{email_template_id} | 
[**Invoke-ListEmailTemplates**](EmailTemplateApi.md#Invoke-ListEmailTemplates) | **GET** /api/v1/email-templates/ | 
[**Invoke-RenderEmailTemplate**](EmailTemplateApi.md#Invoke-RenderEmailTemplate) | **POST** /api/v1/email-templates/{email_template_id}/render | 
[**Update-EmailTemplate**](EmailTemplateApi.md#Update-EmailTemplate) | **PUT** /api/v1/email-templates/{email_template_id} | 


<a id="New-EmailTemplate"></a>
# **New-EmailTemplate**
> EmailTemplate New-EmailTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmailTemplateCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmailTemplateCreate = Initialize-EmailTemplateCreate -Body "MyBody" -Name "MyName" -Status "active" -Subject "MySubject" -Variables # EmailTemplateCreate | 

try {
    $Result = New-EmailTemplate -EmailTemplateCreate $EmailTemplateCreate
} catch {
    Write-Host ("Exception occurred when calling New-EmailTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmailTemplateCreate** | [**EmailTemplateCreate**](EmailTemplateCreate.md)|  | 

### Return type

[**EmailTemplate**](EmailTemplate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteEmailTemplate"></a>
# **Invoke-DeleteEmailTemplate**
> void Invoke-DeleteEmailTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmailTemplateId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmailTemplateId = "MyEmailTemplateId" # String | 

try {
    $Result = Invoke-DeleteEmailTemplate -EmailTemplateId $EmailTemplateId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteEmailTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmailTemplateId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-EmailTemplate"></a>
# **Get-EmailTemplate**
> EmailTemplate Get-EmailTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmailTemplateId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmailTemplateId = "MyEmailTemplateId" # String | 

try {
    $Result = Get-EmailTemplate -EmailTemplateId $EmailTemplateId
} catch {
    Write-Host ("Exception occurred when calling Get-EmailTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmailTemplateId** | **String**|  | 

### Return type

[**EmailTemplate**](EmailTemplate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListEmailTemplates"></a>
# **Invoke-ListEmailTemplates**
> EmailTemplate[] Invoke-ListEmailTemplates<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$Search = "MySearch" # String |  (optional)

try {
    $Result = Invoke-ListEmailTemplates -Page $Page -PageSize $PageSize -Status $Status -Search $Search
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListEmailTemplates: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **Search** | **String**|  | [optional] 

### Return type

[**EmailTemplate[]**](EmailTemplate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-RenderEmailTemplate"></a>
# **Invoke-RenderEmailTemplate**
> AnyType Invoke-RenderEmailTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmailTemplateId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmailTemplateId = "MyEmailTemplateId" # String | 
$Body =  # AnyType | 

try {
    $Result = Invoke-RenderEmailTemplate -EmailTemplateId $EmailTemplateId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-RenderEmailTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmailTemplateId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-EmailTemplate"></a>
# **Update-EmailTemplate**
> EmailTemplate Update-EmailTemplate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmailTemplateId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmailTemplateUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmailTemplateId = "MyEmailTemplateId" # String | 
$EmailTemplateUpdate = Initialize-EmailTemplateUpdate -Body "MyBody" -Name "MyName" -Status "active" -Subject "MySubject" -Variables # EmailTemplateUpdate | 

try {
    $Result = Update-EmailTemplate -EmailTemplateId $EmailTemplateId -EmailTemplateUpdate $EmailTemplateUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-EmailTemplate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmailTemplateId** | **String**|  | 
 **EmailTemplateUpdate** | [**EmailTemplateUpdate**](EmailTemplateUpdate.md)|  | 

### Return type

[**EmailTemplate**](EmailTemplate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

