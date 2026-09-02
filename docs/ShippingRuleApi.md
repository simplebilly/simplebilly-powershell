# PSOpenAPITools.PSOpenAPITools\Api.ShippingRuleApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ShippingRule**](ShippingRuleApi.md#New-ShippingRule) | **POST** /api/v1/shipping-rules | 
[**Invoke-DeleteShippingRule**](ShippingRuleApi.md#Invoke-DeleteShippingRule) | **DELETE** /api/v1/shipping-rules/{rule_id} | 
[**Get-ShippingRule**](ShippingRuleApi.md#Get-ShippingRule) | **GET** /api/v1/shipping-rules/{rule_id} | 
[**Invoke-ListShippingRules**](ShippingRuleApi.md#Invoke-ListShippingRules) | **GET** /api/v1/shipping-rules/ | 
[**Update-ShippingRule**](ShippingRuleApi.md#Update-ShippingRule) | **PUT** /api/v1/shipping-rules/{rule_id} | 


<a id="New-ShippingRule"></a>
# **New-ShippingRule**
> ShippingRule New-ShippingRule<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShippingRuleCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ShippingRuleCreate = Initialize-ShippingRuleCreate -Carrier "MyCarrier" -Country "ABW" -DeliveryTime "MyDeliveryTime" -IsActive $false -MaxWeightKg 0 -MinWeightKg 0 -Name "MyName" -Notes "MyNotes" -Price "MyPrice" -Priority 0 # ShippingRuleCreate | 

try {
    $Result = New-ShippingRule -ShippingRuleCreate $ShippingRuleCreate
} catch {
    Write-Host ("Exception occurred when calling New-ShippingRule: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ShippingRuleCreate** | [**ShippingRuleCreate**](ShippingRuleCreate.md)|  | 

### Return type

[**ShippingRule**](ShippingRule.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteShippingRule"></a>
# **Invoke-DeleteShippingRule**
> void Invoke-DeleteShippingRule<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RuleId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RuleId = "MyRuleId" # String | 

try {
    $Result = Invoke-DeleteShippingRule -RuleId $RuleId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteShippingRule: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RuleId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ShippingRule"></a>
# **Get-ShippingRule**
> ShippingRule Get-ShippingRule<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RuleId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RuleId = "MyRuleId" # String | 

try {
    $Result = Get-ShippingRule -RuleId $RuleId
} catch {
    Write-Host ("Exception occurred when calling Get-ShippingRule: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RuleId** | **String**|  | 

### Return type

[**ShippingRule**](ShippingRule.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListShippingRules"></a>
# **Invoke-ListShippingRules**
> ShippingRule[] Invoke-ListShippingRules<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Country] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Country = "MyCountry" # String |  (optional)

try {
    $Result = Invoke-ListShippingRules -Page $Page -PageSize $PageSize -Country $Country
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListShippingRules: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Country** | **String**|  | [optional] 

### Return type

[**ShippingRule[]**](ShippingRule.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ShippingRule"></a>
# **Update-ShippingRule**
> ShippingRule Update-ShippingRule<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RuleId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShippingRuleUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RuleId = "MyRuleId" # String | 
$ShippingRuleUpdate = Initialize-ShippingRuleUpdate -Carrier "MyCarrier" -Country "ABW" -DeliveryTime "MyDeliveryTime" -IsActive $false -MaxWeightKg 0 -MinWeightKg 0 -Name "MyName" -Notes "MyNotes" -Price "MyPrice" -Priority 0 # ShippingRuleUpdate | 

try {
    $Result = Update-ShippingRule -RuleId $RuleId -ShippingRuleUpdate $ShippingRuleUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ShippingRule: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RuleId** | **String**|  | 
 **ShippingRuleUpdate** | [**ShippingRuleUpdate**](ShippingRuleUpdate.md)|  | 

### Return type

[**ShippingRule**](ShippingRule.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

