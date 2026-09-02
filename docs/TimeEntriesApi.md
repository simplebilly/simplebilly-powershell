# PSOpenAPITools.PSOpenAPITools\Api.TimeEntriesApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ClockInTimeEntry**](TimeEntriesApi.md#Invoke-ClockInTimeEntry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile).
[**Invoke-ClockOutTimeEntry**](TimeEntriesApi.md#Invoke-ClockOutTimeEntry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.
[**Get-LaborCosts**](TimeEntriesApi.md#Get-LaborCosts) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.
[**Invoke-ListTimeEntries**](TimeEntriesApi.md#Invoke-ListTimeEntries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters.


<a id="Invoke-ClockInTimeEntry"></a>
# **Invoke-ClockInTimeEntry**
> TimeEntryDto Invoke-ClockInTimeEntry<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TimeEntryClockIn] <PSCustomObject><br>

Clock in for the authenticated user (resolved via their employee profile).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TimeEntryClockIn = Initialize-TimeEntryClockIn -Notes "MyNotes" # TimeEntryClockIn | 

# Clock in for the authenticated user (resolved via their employee profile).
try {
    $Result = Invoke-ClockInTimeEntry -TimeEntryClockIn $TimeEntryClockIn
} catch {
    Write-Host ("Exception occurred when calling Invoke-ClockInTimeEntry: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TimeEntryClockIn** | [**TimeEntryClockIn**](TimeEntryClockIn.md)|  | 

### Return type

[**TimeEntryDto**](TimeEntryDto.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ClockOutTimeEntry"></a>
# **Invoke-ClockOutTimeEntry**
> TimeEntryDto Invoke-ClockOutTimeEntry<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TimeEntryClockOut] <PSCustomObject><br>

Clock out an entry: the entry's owner, or anyone with `time_entries:write`.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$TimeEntryClockOut = Initialize-TimeEntryClockOut -ClockOut (Get-Date) -Hours "MyHours" # TimeEntryClockOut | 

# Clock out an entry: the entry's owner, or anyone with `time_entries:write`.
try {
    $Result = Invoke-ClockOutTimeEntry -Id $Id -TimeEntryClockOut $TimeEntryClockOut
} catch {
    Write-Host ("Exception occurred when calling Invoke-ClockOutTimeEntry: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **TimeEntryClockOut** | [**TimeEntryClockOut**](TimeEntryClockOut.md)|  | 

### Return type

[**TimeEntryDto**](TimeEntryDto.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-LaborCosts"></a>
# **Get-LaborCosts**
> LaborCostRow[] Get-LaborCosts<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-From] <System.DateTime><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-To] <System.DateTime><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GroupBy] <String><br>

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$From = (Get-Date) # System.DateTime | 
$To = (Get-Date) # System.DateTime | 
$GroupBy = "MyGroupBy" # String | One of ""employee"", ""order"" or ""day"".

# Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.
try {
    $Result = Get-LaborCosts -From $From -To $To -GroupBy $GroupBy
} catch {
    Write-Host ("Exception occurred when calling Get-LaborCosts: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **From** | **System.DateTime**|  | 
 **To** | **System.DateTime**|  | 
 **GroupBy** | **String**| One of &quot;&quot;employee&quot;&quot;, &quot;&quot;order&quot;&quot; or &quot;&quot;day&quot;&quot;. | 

### Return type

[**LaborCostRow[]**](LaborCostRow.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListTimeEntries"></a>
# **Invoke-ListTimeEntries**
> TimeEntryDto[] Invoke-ListTimeEntries<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-From] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-To] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Active] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmployeeId] <String><br>

List time entries with optional date-range / active / employee filters.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$From = (Get-Date) # System.DateTime |  (optional)
$To = (Get-Date) # System.DateTime |  (optional)
$Active = $true # Boolean | Only currently running shifts (clock_in set, clock_out null). (optional)
$EmployeeId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)

# List time entries with optional date-range / active / employee filters.
try {
    $Result = Invoke-ListTimeEntries -From $From -To $To -Active $Active -EmployeeId $EmployeeId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListTimeEntries: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **From** | **System.DateTime**|  | [optional] 
 **To** | **System.DateTime**|  | [optional] 
 **Active** | **Boolean**| Only currently running shifts (clock_in set, clock_out null). | [optional] 
 **EmployeeId** | **String**|  | [optional] 

### Return type

[**TimeEntryDto[]**](TimeEntryDto.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

