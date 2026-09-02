# PSOpenAPITools.PSOpenAPITools\Api.AttachmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Add-mentRestore**](AttachmentApi.md#Add-mentRestore) | **POST** /api/v1/attachments/{id}/restore | 
[**New-Attachment**](AttachmentApi.md#New-Attachment) | **POST** /api/v1/attachments | 
[**Invoke-DeleteAttachment**](AttachmentApi.md#Invoke-DeleteAttachment) | **DELETE** /api/v1/attachments/{id} | 
[**Get-Attachment**](AttachmentApi.md#Get-Attachment) | **GET** /api/v1/attachments/{id} | 
[**Invoke-ListAttachments**](AttachmentApi.md#Invoke-ListAttachments) | **GET** /api/v1/attachments/ | 
[**Save-AttachmentOcrText**](AttachmentApi.md#Save-AttachmentOcrText) | **PUT** /api/v1/attachments/{attachment_id}/ocr-text | Persist client-side OCR output for an attachment.


<a id="Add-mentRestore"></a>
# **Add-mentRestore**
> Attachment Add-mentRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Add-mentRestore -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Add-mentRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**Attachment**](Attachment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-Attachment"></a>
# **New-Attachment**
> Attachment New-Attachment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttachmentCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttachmentCreate = Initialize-AttachmentCreate -ContactId "MyContactId" -FileName "MyFileName" -FileSize 0 -MimeType "MyMimeType" -OriginalName "MyOriginalName" -PdfaPath "MyPdfaPath" -Sha256Hash "MySha256Hash" -UploadedBy "MyUploadedBy" # AttachmentCreate | 

try {
    $Result = New-Attachment -AttachmentCreate $AttachmentCreate
} catch {
    Write-Host ("Exception occurred when calling New-Attachment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttachmentCreate** | [**AttachmentCreate**](AttachmentCreate.md)|  | 

### Return type

[**Attachment**](Attachment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteAttachment"></a>
# **Invoke-DeleteAttachment**
> void Invoke-DeleteAttachment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteAttachment -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteAttachment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Get-Attachment"></a>
# **Get-Attachment**
> Attachment Get-Attachment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-Attachment -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-Attachment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**Attachment**](Attachment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListAttachments"></a>
# **Invoke-ListAttachments**
> Attachment[] Invoke-ListAttachments<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ContactId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ContactId = "MyContactId" # String |  (optional)

try {
    $Result = Invoke-ListAttachments -Page $Page -PageSize $PageSize -ContactId $ContactId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListAttachments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **ContactId** | **String**|  | [optional] 

### Return type

[**Attachment[]**](Attachment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Save-AttachmentOcrText"></a>
# **Save-AttachmentOcrText**
> Attachment Save-AttachmentOcrText<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttachmentId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OcrTextRequest] <PSCustomObject><br>

Persist client-side OCR output for an attachment.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttachmentId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$OcrTextRequest = Initialize-OcrTextRequest -OcrText "MyOcrText" # OcrTextRequest | 

# Persist client-side OCR output for an attachment.
try {
    $Result = Save-AttachmentOcrText -AttachmentId $AttachmentId -OcrTextRequest $OcrTextRequest
} catch {
    Write-Host ("Exception occurred when calling Save-AttachmentOcrText: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttachmentId** | **String**|  | 
 **OcrTextRequest** | [**OcrTextRequest**](OcrTextRequest.md)|  | 

### Return type

[**Attachment**](Attachment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

