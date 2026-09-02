# PSOpenAPITools.PSOpenAPITools\Api.AttachmentVersionApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-AttachmentVersion**](AttachmentVersionApi.md#New-AttachmentVersion) | **POST** /api/v1/attachments/{attachment_id}/versions | 
[**Invoke-ListAttachmentVersions**](AttachmentVersionApi.md#Invoke-ListAttachmentVersions) | **GET** /api/v1/attachments/{attachment_id}/versions | 
[**Restore-AttachmentVersion**](AttachmentVersionApi.md#Restore-AttachmentVersion) | **POST** /api/v1/attachments/{attachment_id}/versions/{version_id}/restore | 


<a id="New-AttachmentVersion"></a>
# **New-AttachmentVersion**
> AttachmentVersion New-AttachmentVersion<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttachmentId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-NewVersionRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttachmentId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$NewVersionRequest = Initialize-NewVersionRequest -FileName "MyFileName" -FileSize 0 -MimeType "MyMimeType" -OriginalName "MyOriginalName" -Sha256Hash "MySha256Hash" # NewVersionRequest | 

try {
    $Result = New-AttachmentVersion -AttachmentId $AttachmentId -NewVersionRequest $NewVersionRequest
} catch {
    Write-Host ("Exception occurred when calling New-AttachmentVersion: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttachmentId** | **String**|  | 
 **NewVersionRequest** | [**NewVersionRequest**](NewVersionRequest.md)|  | 

### Return type

[**AttachmentVersion**](AttachmentVersion.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListAttachmentVersions"></a>
# **Invoke-ListAttachmentVersions**
> AttachmentVersion[] Invoke-ListAttachmentVersions<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttachmentId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttachmentId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-ListAttachmentVersions -AttachmentId $AttachmentId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListAttachmentVersions: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttachmentId** | **String**|  | 

### Return type

[**AttachmentVersion[]**](AttachmentVersion.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Restore-AttachmentVersion"></a>
# **Restore-AttachmentVersion**
> Attachment Restore-AttachmentVersion<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttachmentId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VersionId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttachmentId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$VersionId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Restore-AttachmentVersion -AttachmentId $AttachmentId -VersionId $VersionId
} catch {
    Write-Host ("Exception occurred when calling Restore-AttachmentVersion: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttachmentId** | **String**|  | 
 **VersionId** | **String**|  | 

### Return type

[**Attachment**](Attachment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

