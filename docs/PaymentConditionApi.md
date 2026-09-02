# PSOpenAPITools.PSOpenAPITools\Api.PaymentConditionApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ListPaymentConditionsApi**](PaymentConditionApi.md#Invoke-ListPaymentConditionsApi) | **GET** /api/v1/payment-conditions | 


<a id="Invoke-ListPaymentConditionsApi"></a>
# **Invoke-ListPaymentConditionsApi**
> PaymentCondition[] Invoke-ListPaymentConditionsApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListPaymentConditionsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPaymentConditionsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PaymentCondition[]**](PaymentCondition.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

