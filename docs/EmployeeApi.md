# PSOpenAPITools.PSOpenAPITools\Api.EmployeeApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Employee**](EmployeeApi.md#New-Employee) | **POST** /api/v1/employees | 
[**Invoke-DeleteEmployee**](EmployeeApi.md#Invoke-DeleteEmployee) | **DELETE** /api/v1/employees/{id} | 
[**Invoke-EmployeeRestore**](EmployeeApi.md#Invoke-EmployeeRestore) | **POST** /api/v1/employees/{id}/restore | 
[**Get-Employee**](EmployeeApi.md#Get-Employee) | **GET** /api/v1/employees/{id} | 
[**Get-EmployeePayrollSummary**](EmployeeApi.md#Get-EmployeePayrollSummary) | **GET** /api/v1/employees/{id}/payroll-summary | 
[**Get-Employees**](EmployeeApi.md#Get-Employees) | **GET** /api/v1/employees/ | 
[**Update-Employee**](EmployeeApi.md#Update-Employee) | **PUT** /api/v1/employees/{id} | 


<a id="New-Employee"></a>
# **New-Employee**
> Employee New-Employee<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmployeeCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmployeeCreate = Initialize-EmployeeCreate -Address "MyAddress" -BackupEmployeeId "MyBackupEmployeeId" -Bic "MyBic" -City "MyCity" -Country "ABW" -DateOfBirth (Get-Date) -DepartmentId "MyDepartmentId" -Email "MyEmail" -FirstName "MyFirstName" -Gender "male" -HireDate (Get-Date) -HourlyCost "MyHourlyCost" -Iban "MyIban" -JobTitle "MyJobTitle" -LastLogin (Get-Date) -LastName "MyLastName" -LastUpdated (Get-Date) -MonthlySalary "MyMonthlySalary" -Phone "MyPhone" -State "MyState" -Status "active" -UserId "MyUserId" -WeeklyHours "MyWeeklyHours" -Zip "MyZip" # EmployeeCreate | 

try {
    $Result = New-Employee -EmployeeCreate $EmployeeCreate
} catch {
    Write-Host ("Exception occurred when calling New-Employee: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmployeeCreate** | [**EmployeeCreate**](EmployeeCreate.md)|  | 

### Return type

[**Employee**](Employee.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteEmployee"></a>
# **Invoke-DeleteEmployee**
> void Invoke-DeleteEmployee<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteEmployee -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteEmployee: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EmployeeRestore"></a>
# **Invoke-EmployeeRestore**
> Employee Invoke-EmployeeRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-EmployeeRestore -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-EmployeeRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**Employee**](Employee.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Employee"></a>
# **Get-Employee**
> Employee Get-Employee<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-Employee -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-Employee: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**Employee**](Employee.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-EmployeePayrollSummary"></a>
# **Get-EmployeePayrollSummary**
> PayrollSummary Get-EmployeePayrollSummary<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <System.Nullable[Int32]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$Year = 56 # Int32 | Fiscal year for the breakdown; defaults to the current year. (optional)

try {
    $Result = Get-EmployeePayrollSummary -Id $Id -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Get-EmployeePayrollSummary: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **Year** | **Int32**| Fiscal year for the breakdown; defaults to the current year. | [optional] 

### Return type

[**PayrollSummary**](PayrollSummary.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Employees"></a>
# **Get-Employees**
> Employee[] Get-Employees<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IncludeDeleted] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 1 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$IncludeDeleted = $true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

try {
    $Result = Get-Employees -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-Employees: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **IncludeDeleted** | **Boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**Employee[]**](Employee.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Employee"></a>
# **Update-Employee**
> Employee Update-Employee<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmployeeUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$EmployeeUpdate = Initialize-EmployeeUpdate -Address "MyAddress" -BackupEmployeeId "MyBackupEmployeeId" -Bic "MyBic" -City "MyCity" -Country "ABW" -DateOfBirth (Get-Date) -DepartmentId "MyDepartmentId" -Email "MyEmail" -FirstName "MyFirstName" -Gender "male" -HireDate (Get-Date) -HourlyCost "MyHourlyCost" -Iban "MyIban" -JobTitle "MyJobTitle" -LastLogin (Get-Date) -LastName "MyLastName" -LastUpdated (Get-Date) -MonthlySalary "MyMonthlySalary" -Phone "MyPhone" -State "MyState" -Status "active" -UserId "MyUserId" -WeeklyHours "MyWeeklyHours" -Zip "MyZip" # EmployeeUpdate | 

try {
    $Result = Update-Employee -Id $Id -EmployeeUpdate $EmployeeUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-Employee: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **EmployeeUpdate** | [**EmployeeUpdate**](EmployeeUpdate.md)|  | 

### Return type

[**Employee**](Employee.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

