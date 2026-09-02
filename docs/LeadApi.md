# PSOpenAPITools.PSOpenAPITools\Api.LeadApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ListLeadsApi**](LeadApi.md#Invoke-ListLeadsApi) | **GET** /api/v1/support/leads | 
[**Update-LeadApi**](LeadApi.md#Update-LeadApi) | **PUT** /api/v1/support/leads/{lead_id} | 


<a id="Invoke-ListLeadsApi"></a>
# **Invoke-ListLeadsApi**
> Lead[] Invoke-ListLeadsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Source] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Status = "MyStatus" # String |  (optional)
$Source = "MySource" # String |  (optional)
$Search = "MySearch" # String |  (optional)
$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)

try {
    $Result = Invoke-ListLeadsApi -Status $Status -Source $Source -Search $Search -Page $Page -PageSize $PageSize
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListLeadsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Status** | **String**|  | [optional] 
 **Source** | **String**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 

### Return type

[**Lead[]**](Lead.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-LeadApi"></a>
# **Update-LeadApi**
> Lead Update-LeadApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-LeadId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-LeadUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$LeadId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$LeadUpdate = Initialize-LeadUpdate -Company "MyCompany" -ConvertedAt (Get-Date) -CreatedAt (Get-Date) -Email "MyEmail" -FirstContactAt (Get-Date) -Name "MyName" -Notes "MyNotes" -Phone "MyPhone" -Score 0 -Source "MySource" -Status "new" -Tags  -TenantId "MyTenantId" -UpdatedAt (Get-Date) # LeadUpdate | 

try {
    $Result = Update-LeadApi -LeadId $LeadId -LeadUpdate $LeadUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-LeadApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **LeadId** | **String**|  | 
 **LeadUpdate** | [**LeadUpdate**](LeadUpdate.md)|  | 

### Return type

[**Lead**](Lead.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

