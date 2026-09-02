# PSOpenAPITools.PSOpenAPITools\Api.CustomerGroupApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Add-GroupMembers**](CustomerGroupApi.md#Add-GroupMembers) | **POST** /api/v1/customer-groups/{customer_group_id}/members | 
[**New-CustomerGroup**](CustomerGroupApi.md#New-CustomerGroup) | **POST** /api/v1/customer-groups | 
[**Invoke-DeleteCustomerGroup**](CustomerGroupApi.md#Invoke-DeleteCustomerGroup) | **DELETE** /api/v1/customer-groups/{customer_group_id} | 
[**Get-CustomerGroup**](CustomerGroupApi.md#Get-CustomerGroup) | **GET** /api/v1/customer-groups/{customer_group_id} | 
[**Invoke-ListCustomerGroups**](CustomerGroupApi.md#Invoke-ListCustomerGroups) | **GET** /api/v1/customer-groups/ | 
[**Update-CustomerGroup**](CustomerGroupApi.md#Update-CustomerGroup) | **PUT** /api/v1/customer-groups/{customer_group_id} | 


<a id="Add-GroupMembers"></a>
# **Add-GroupMembers**
> CustomerGroup Add-GroupMembers<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerGroupId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerGroupId = "MyCustomerGroupId" # String | 
$Body =  # AnyType | 

try {
    $Result = Add-GroupMembers -CustomerGroupId $CustomerGroupId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Add-GroupMembers: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerGroupId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-CustomerGroup"></a>
# **New-CustomerGroup**
> CustomerGroup New-CustomerGroup<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerGroupCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerGroupCreate = Initialize-CustomerGroupCreate -Description "MyDescription" -MemberIds "MyMemberIds" -MembershipFilter "MyMembershipFilter" -Name "MyName" # CustomerGroupCreate | 

try {
    $Result = New-CustomerGroup -CustomerGroupCreate $CustomerGroupCreate
} catch {
    Write-Host ("Exception occurred when calling New-CustomerGroup: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerGroupCreate** | [**CustomerGroupCreate**](CustomerGroupCreate.md)|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteCustomerGroup"></a>
# **Invoke-DeleteCustomerGroup**
> void Invoke-DeleteCustomerGroup<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerGroupId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerGroupId = "MyCustomerGroupId" # String | 

try {
    $Result = Invoke-DeleteCustomerGroup -CustomerGroupId $CustomerGroupId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteCustomerGroup: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerGroupId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-CustomerGroup"></a>
# **Get-CustomerGroup**
> CustomerGroup Get-CustomerGroup<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerGroupId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerGroupId = "MyCustomerGroupId" # String | 

try {
    $Result = Get-CustomerGroup -CustomerGroupId $CustomerGroupId
} catch {
    Write-Host ("Exception occurred when calling Get-CustomerGroup: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerGroupId** | **String**|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListCustomerGroups"></a>
# **Invoke-ListCustomerGroups**
> CustomerGroup[] Invoke-ListCustomerGroups<br>
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
    $Result = Invoke-ListCustomerGroups -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListCustomerGroups: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**CustomerGroup[]**](CustomerGroup.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-CustomerGroup"></a>
# **Update-CustomerGroup**
> CustomerGroup Update-CustomerGroup<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerGroupId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerGroupUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerGroupId = "MyCustomerGroupId" # String | 
$CustomerGroupUpdate = Initialize-CustomerGroupUpdate -Description "MyDescription" -MemberIds "MyMemberIds" -MembershipFilter "MyMembershipFilter" -Name "MyName" # CustomerGroupUpdate | 

try {
    $Result = Update-CustomerGroup -CustomerGroupId $CustomerGroupId -CustomerGroupUpdate $CustomerGroupUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-CustomerGroup: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerGroupId** | **String**|  | 
 **CustomerGroupUpdate** | [**CustomerGroupUpdate**](CustomerGroupUpdate.md)|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

