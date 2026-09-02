# PSOpenAPITools.PSOpenAPITools\Api.GezApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-GezApi**](GezApi.md#Invoke-GezApi) | **GET** /api/v1/bookkeeping/gez | 


<a id="Invoke-GezApi"></a>
# **Invoke-GezApi**
> GezReport Invoke-GezApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Jahr] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Betriebsstaetten] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Kfz] <System.Nullable[Int64]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Hotelzimmer] <System.Nullable[Int64]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Beschaefigte] <System.Nullable[Int64]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Jahr = 56 # Int32 |  (optional)
$Betriebsstaetten = "MyBetriebsstaetten" # String | Liste der Betriebsstätten als JSON, z.B. `[{""name"":""Filiale 1"",""beschaefigte"":12}]`. (optional)
$Kfz = 789 # Int64 | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). (optional)
$Hotelzimmer = 789 # Int64 | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. (optional)
$Beschaefigte = 789 # Int64 | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen). (optional)

try {
    $Result = Invoke-GezApi -Jahr $Jahr -Betriebsstaetten $Betriebsstaetten -Kfz $Kfz -Hotelzimmer $Hotelzimmer -Beschaefigte $Beschaefigte
} catch {
    Write-Host ("Exception occurred when calling Invoke-GezApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Jahr** | **Int32**|  | [optional] 
 **Betriebsstaetten** | **String**| Liste der Betriebsstätten als JSON, z.B. &#x60;[{&quot;&quot;name&quot;&quot;:&quot;&quot;Filiale 1&quot;&quot;,&quot;&quot;beschaefigte&quot;&quot;:12}]&#x60;. | [optional] 
 **Kfz** | **Int64**| Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional] 
 **Hotelzimmer** | **Int64**| Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional] 
 **Beschaefigte** | **Int64**| Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional] 

### Return type

[**GezReport**](GezReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

