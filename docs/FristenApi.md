# PSOpenAPITools.PSOpenAPITools\Api.FristenApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-FristenApi**](FristenApi.md#Invoke-FristenApi) | **GET** /api/v1/bookkeeping/fristen | 


<a id="Invoke-FristenApi"></a>
# **Invoke-FristenApi**
> FristenErgebnis Invoke-FristenApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Bundesland] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Voranmeldungsrhythmus] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Dauerfristverlaengerung] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EstAktiv] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GewstAktiv] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Monate] <System.Nullable[Int32]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Bundesland = "MyBundesland" # String |  (optional)
$Voranmeldungsrhythmus = "MyVoranmeldungsrhythmus" # String |  (optional)
$Dauerfristverlaengerung = $true # Boolean |  (optional)
$EstAktiv = $true # Boolean |  (optional)
$GewstAktiv = $true # Boolean |  (optional)
$Monate = 56 # Int32 |  (optional)

try {
    $Result = Invoke-FristenApi -Bundesland $Bundesland -Voranmeldungsrhythmus $Voranmeldungsrhythmus -Dauerfristverlaengerung $Dauerfristverlaengerung -EstAktiv $EstAktiv -GewstAktiv $GewstAktiv -Monate $Monate
} catch {
    Write-Host ("Exception occurred when calling Invoke-FristenApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Bundesland** | **String**|  | [optional] 
 **Voranmeldungsrhythmus** | **String**|  | [optional] 
 **Dauerfristverlaengerung** | **Boolean**|  | [optional] 
 **EstAktiv** | **Boolean**|  | [optional] 
 **GewstAktiv** | **Boolean**|  | [optional] 
 **Monate** | **Int32**|  | [optional] 

### Return type

[**FristenErgebnis**](FristenErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

