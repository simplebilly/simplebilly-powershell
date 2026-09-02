# PSOpenAPITools.PSOpenAPITools\Api.BudgetsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-BudgetsApi**](BudgetsApi.md#Invoke-BudgetsApi) | **GET** /api/v1/bookkeeping/budgets | 
[**Invoke-UpsertBudgetGoalApi**](BudgetsApi.md#Invoke-UpsertBudgetGoalApi) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} | 


<a id="Invoke-BudgetsApi"></a>
# **Invoke-BudgetsApi**
> BudgetErgebnis Invoke-BudgetsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Month] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 
$Month = 56 # Int32 | 

try {
    $Result = Invoke-BudgetsApi -Year $Year -Month $Month
} catch {
    Write-Host ("Exception occurred when calling Invoke-BudgetsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 
 **Month** | **Int32**|  | 

### Return type

[**BudgetErgebnis**](BudgetErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-UpsertBudgetGoalApi"></a>
# **Invoke-UpsertBudgetGoalApi**
> Budget Invoke-UpsertBudgetGoalApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Category] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-BudgetGoalRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Category = "MyCategory" # String | 
$BudgetGoalRequest = Initialize-BudgetGoalRequest -MonthlyGoal "MyMonthlyGoal" -Year 0 # BudgetGoalRequest | 

try {
    $Result = Invoke-UpsertBudgetGoalApi -Category $Category -BudgetGoalRequest $BudgetGoalRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-UpsertBudgetGoalApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Category** | **String**|  | 
 **BudgetGoalRequest** | [**BudgetGoalRequest**](BudgetGoalRequest.md)|  | 

### Return type

[**Budget**](Budget.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

