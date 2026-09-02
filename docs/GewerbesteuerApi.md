# PSOpenAPITools.PSOpenAPITools\Api.GewerbesteuerApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-GewerbesteuerApi**](GewerbesteuerApi.md#Invoke-GewerbesteuerApi) | **GET** /api/v1/bookkeeping/gewerbesteuer | 


<a id="Invoke-GewerbesteuerApi"></a>
# **Invoke-GewerbesteuerApi**
> GewerbesteuerErgebnis Invoke-GewerbesteuerApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Hebesatz] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Gewerbeertrag] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Country] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Gemeindeschluessel] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 
$Hebesatz = "MyHebesatz" # String |  (optional)
$Gewerbeertrag = "MyGewerbeertrag" # String |  (optional)
$Country = "MyCountry" # String |  (optional)
$Gemeindeschluessel = "MyGemeindeschluessel" # String |  (optional)

try {
    $Result = Invoke-GewerbesteuerApi -Year $Year -Hebesatz $Hebesatz -Gewerbeertrag $Gewerbeertrag -Country $Country -Gemeindeschluessel $Gemeindeschluessel
} catch {
    Write-Host ("Exception occurred when calling Invoke-GewerbesteuerApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 
 **Hebesatz** | **String**|  | [optional] 
 **Gewerbeertrag** | **String**|  | [optional] 
 **Country** | **String**|  | [optional] 
 **Gemeindeschluessel** | **String**|  | [optional] 

### Return type

[**GewerbesteuerErgebnis**](GewerbesteuerErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

