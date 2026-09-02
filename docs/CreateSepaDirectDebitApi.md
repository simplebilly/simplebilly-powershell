# PSOpenAPITools.PSOpenAPITools\Api.CreateSepaDirectDebitApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-SepaDirectDebitApi**](CreateSepaDirectDebitApi.md#New-SepaDirectDebitApi) | **POST** /api/v1/bookkeeping/sepa-direct-debit | 


<a id="New-SepaDirectDebitApi"></a>
# **New-SepaDirectDebitApi**
> SepaDirectDebitResponse New-SepaDirectDebitApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreditorName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreditorIban] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreditorId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-MandateId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-MandateDate] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DebtorName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DebtorIban] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Amount] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CollectionDate] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreditorBic] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DebtorBic] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Description] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CreditorName = "MyCreditorName" # String | 
$CreditorIban = "MyCreditorIban" # String | 
$CreditorId = "MyCreditorId" # String | 
$MandateId = "MyMandateId" # String | 
$MandateDate = "MyMandateDate" # String | 
$DebtorName = "MyDebtorName" # String | 
$DebtorIban = "MyDebtorIban" # String | 
$Amount = "MyAmount" # String | 
$CollectionDate = "MyCollectionDate" # String | 
$CreditorBic = "MyCreditorBic" # String |  (optional)
$DebtorBic = "MyDebtorBic" # String |  (optional)
$Description = "MyDescription" # String |  (optional)

try {
    $Result = New-SepaDirectDebitApi -CreditorName $CreditorName -CreditorIban $CreditorIban -CreditorId $CreditorId -MandateId $MandateId -MandateDate $MandateDate -DebtorName $DebtorName -DebtorIban $DebtorIban -Amount $Amount -CollectionDate $CollectionDate -CreditorBic $CreditorBic -DebtorBic $DebtorBic -Description $Description
} catch {
    Write-Host ("Exception occurred when calling New-SepaDirectDebitApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreditorName** | **String**|  | 
 **CreditorIban** | **String**|  | 
 **CreditorId** | **String**|  | 
 **MandateId** | **String**|  | 
 **MandateDate** | **String**|  | 
 **DebtorName** | **String**|  | 
 **DebtorIban** | **String**|  | 
 **Amount** | **String**|  | 
 **CollectionDate** | **String**|  | 
 **CreditorBic** | **String**|  | [optional] 
 **DebtorBic** | **String**|  | [optional] 
 **Description** | **String**|  | [optional] 

### Return type

[**SepaDirectDebitResponse**](SepaDirectDebitResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

