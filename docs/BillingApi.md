# PSOpenAPITools.PSOpenAPITools\Api.BillingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-Plans**](BillingApi.md#Get-Plans) | **GET** /api/v1/plans | All canonical plans (free/starter/business/enterprise) — the single source of truth lives in &#x60;crate::saasy::plans&#x60;, matching marketing.
[**Get-QuotaApi**](BillingApi.md#Get-QuotaApi) | **GET** /api/v1/quota | Effective limits + current usage for the calling tenant.
[**Get-SubscriptionApi**](BillingApi.md#Get-SubscriptionApi) | **GET** /api/v1/subscription | 
[**Get-UsageApi**](BillingApi.md#Get-UsageApi) | **GET** /api/v1/usage | 
[**Invoke-PaddleSubscriptionWebhook**](BillingApi.md#Invoke-PaddleSubscriptionWebhook) | **POST** /api/webhooks/paddle/subscription | Paddle Billing subscription webhook. Verifies the &#x60;Paddle-Signature&#x60; header (HMAC-SHA256 over &#x60;&quot;&quot;{ts}:{raw_body}&quot;&quot;&#x60; with the webhook secret), then updates &#x60;billing_info&#x60; and &#x60;tenants.plan&#x60; for the tenant identified by the subscription &#x60;custom_data&#x60; (JSON &#x60;{&quot;&quot;tenant_id&quot;&quot;: &quot;&quot;...&quot;&quot;}&#x60; or a bare tenant UUID).
[**Send-QuotaApi**](BillingApi.md#Send-QuotaApi) | **PUT** /api/v1/quota | Write the per-tenant quota override (&#x60;admin:settings&#x60;). An empty object clears the override.


<a id="Get-Plans"></a>
# **Get-Plans**
> ApiResponseVecPlan Get-Plans<br>

All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.
try {
    $Result = Get-Plans
} catch {
    Write-Host ("Exception occurred when calling Get-Plans: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseVecPlan**](ApiResponseVecPlan.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-QuotaApi"></a>
# **Get-QuotaApi**
> void Get-QuotaApi<br>

Effective limits + current usage for the calling tenant.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Effective limits + current usage for the calling tenant.
try {
    $Result = Get-QuotaApi
} catch {
    Write-Host ("Exception occurred when calling Get-QuotaApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-SubscriptionApi"></a>
# **Get-SubscriptionApi**
> ApiResponseSubscriptionOverview Get-SubscriptionApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Get-SubscriptionApi
} catch {
    Write-Host ("Exception occurred when calling Get-SubscriptionApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseSubscriptionOverview**](ApiResponseSubscriptionOverview.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-UsageApi"></a>
# **Get-UsageApi**
> void Get-UsageApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Meter] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Meter = "MyMeter" # String |  (optional)

try {
    $Result = Get-UsageApi -Meter $Meter
} catch {
    Write-Host ("Exception occurred when calling Get-UsageApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Meter** | **String**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PaddleSubscriptionWebhook"></a>
# **Invoke-PaddleSubscriptionWebhook**
> void Invoke-PaddleSubscriptionWebhook<br>

Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `""{ts}:{raw_body}""` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{""tenant_id"": ""...""}` or a bare tenant UUID).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `""{ts}:{raw_body}""` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{""tenant_id"": ""...""}` or a bare tenant UUID).
try {
    $Result = Invoke-PaddleSubscriptionWebhook
} catch {
    Write-Host ("Exception occurred when calling Invoke-PaddleSubscriptionWebhook: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Send-QuotaApi"></a>
# **Send-QuotaApi**
> void Send-QuotaApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotaOverride] <PSCustomObject><br>

Write the per-tenant quota override (`admin:settings`). An empty object clears the override.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotaOverrideFeatures = Initialize-QuotaOverrideFeatures -Erp $false -FancyReports $false -TaxAutomations $false
$QuotaOverride = Initialize-QuotaOverride -Features $QuotaOverrideFeatures -MaxConnectors 0 -MaxInvoicesPerMonth 0 -MaxUsers 0 -Metered @{ key_example = 0 } -Plan "MyPlan" # QuotaOverride | 

# Write the per-tenant quota override (`admin:settings`). An empty object clears the override.
try {
    $Result = Send-QuotaApi -QuotaOverride $QuotaOverride
} catch {
    Write-Host ("Exception occurred when calling Send-QuotaApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotaOverride** | [**QuotaOverride**](QuotaOverride.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

