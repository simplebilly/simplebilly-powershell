# PSOpenAPITools.PSOpenAPITools\Api.GenerateQrcodeApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-QrcodeApi**](GenerateQrcodeApi.md#New-QrcodeApi) | **GET** /api/v1/invoices/{id}/qrcode | 


<a id="New-QrcodeApi"></a>
# **New-QrcodeApi**
> QRCodeResponse New-QrcodeApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Iban] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-HolderName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Bic] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Amount] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Reference] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Purpose] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Iban = "MyIban" # String | 
$Id = "MyId" # String | 
$HolderName = "MyHolderName" # String |  (optional)
$Bic = "MyBic" # String |  (optional)
$Amount = "MyAmount" # String |  (optional)
$Reference = "MyReference" # String |  (optional)
$Purpose = "MyPurpose" # String |  (optional)

try {
    $Result = New-QrcodeApi -Iban $Iban -Id $Id -HolderName $HolderName -Bic $Bic -Amount $Amount -Reference $Reference -Purpose $Purpose
} catch {
    Write-Host ("Exception occurred when calling New-QrcodeApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Iban** | **String**|  | 
 **Id** | **String**|  | 
 **HolderName** | **String**|  | [optional] 
 **Bic** | **String**|  | [optional] 
 **Amount** | **String**|  | [optional] 
 **Reference** | **String**|  | [optional] 
 **Purpose** | **String**|  | [optional] 

### Return type

[**QRCodeResponse**](QRCodeResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

