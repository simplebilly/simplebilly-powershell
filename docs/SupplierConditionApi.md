# PSOpenAPITools.PSOpenAPITools\Api.SupplierConditionApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-SupplierCondition**](SupplierConditionApi.md#New-SupplierCondition) | **POST** /api/v1/supplier-conditions | 
[**Invoke-DeleteSupplierCondition**](SupplierConditionApi.md#Invoke-DeleteSupplierCondition) | **DELETE** /api/v1/supplier-conditions/{supplier_condition_id} | 
[**Get-SupplierCondition**](SupplierConditionApi.md#Get-SupplierCondition) | **GET** /api/v1/supplier-conditions/{supplier_condition_id} | 
[**Invoke-ListSupplierConditions**](SupplierConditionApi.md#Invoke-ListSupplierConditions) | **GET** /api/v1/supplier-conditions/ | 
[**Update-SupplierCondition**](SupplierConditionApi.md#Update-SupplierCondition) | **PUT** /api/v1/supplier-conditions/{supplier_condition_id} | 


<a id="New-SupplierCondition"></a>
# **New-SupplierCondition**
> SupplierCondition New-SupplierCondition<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierConditionCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierConditionCreate = Initialize-SupplierConditionCreate -Currency "MyCurrency" -DeliveryTerms "MyDeliveryTerms" -EarlyPaymentDiscountPercent "MyEarlyPaymentDiscountPercent" -IsDefault $false -MinimumOrderValue "MyMinimumOrderValue" -Notes "MyNotes" -PaymentDueDays 0 -PaymentTerms "MyPaymentTerms" -SupplierContactId "MySupplierContactId" -SupplierName "MySupplierName" -VolumeDiscountTiers # SupplierConditionCreate | 

try {
    $Result = New-SupplierCondition -SupplierConditionCreate $SupplierConditionCreate
} catch {
    Write-Host ("Exception occurred when calling New-SupplierCondition: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierConditionCreate** | [**SupplierConditionCreate**](SupplierConditionCreate.md)|  | 

### Return type

[**SupplierCondition**](SupplierCondition.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteSupplierCondition"></a>
# **Invoke-DeleteSupplierCondition**
> void Invoke-DeleteSupplierCondition<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierConditionId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierConditionId = "MySupplierConditionId" # String | 

try {
    $Result = Invoke-DeleteSupplierCondition -SupplierConditionId $SupplierConditionId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteSupplierCondition: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierConditionId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-SupplierCondition"></a>
# **Get-SupplierCondition**
> SupplierCondition Get-SupplierCondition<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierConditionId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierConditionId = "MySupplierConditionId" # String | 

try {
    $Result = Get-SupplierCondition -SupplierConditionId $SupplierConditionId
} catch {
    Write-Host ("Exception occurred when calling Get-SupplierCondition: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierConditionId** | **String**|  | 

### Return type

[**SupplierCondition**](SupplierCondition.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListSupplierConditions"></a>
# **Invoke-ListSupplierConditions**
> SupplierCondition[] Invoke-ListSupplierConditions<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierContactId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$SupplierContactId = "MySupplierContactId" # String |  (optional)
$Search = "MySearch" # String |  (optional)

try {
    $Result = Invoke-ListSupplierConditions -Page $Page -PageSize $PageSize -SupplierContactId $SupplierContactId -Search $Search
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListSupplierConditions: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **SupplierContactId** | **String**|  | [optional] 
 **Search** | **String**|  | [optional] 

### Return type

[**SupplierCondition[]**](SupplierCondition.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-SupplierCondition"></a>
# **Update-SupplierCondition**
> SupplierCondition Update-SupplierCondition<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierConditionId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierConditionUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierConditionId = "MySupplierConditionId" # String | 
$SupplierConditionUpdate = Initialize-SupplierConditionUpdate -Currency "MyCurrency" -DeliveryTerms "MyDeliveryTerms" -EarlyPaymentDiscountPercent "MyEarlyPaymentDiscountPercent" -IsDefault $false -MinimumOrderValue "MyMinimumOrderValue" -Notes "MyNotes" -PaymentDueDays 0 -PaymentTerms "MyPaymentTerms" -SupplierContactId "MySupplierContactId" -SupplierName "MySupplierName" -VolumeDiscountTiers # SupplierConditionUpdate | 

try {
    $Result = Update-SupplierCondition -SupplierConditionId $SupplierConditionId -SupplierConditionUpdate $SupplierConditionUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-SupplierCondition: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierConditionId** | **String**|  | 
 **SupplierConditionUpdate** | [**SupplierConditionUpdate**](SupplierConditionUpdate.md)|  | 

### Return type

[**SupplierCondition**](SupplierCondition.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

