# PSOpenAPITools.PSOpenAPITools\Api.PosApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-PosBilling**](PosApi.md#Invoke-PosBilling) | **GET** /api/pos/billing | 
[**Invoke-PosCreateOrder**](PosApi.md#Invoke-PosCreateOrder) | **POST** /api/pos/orders | 
[**Invoke-PosCreateRegister**](PosApi.md#Invoke-PosCreateRegister) | **POST** /api/pos/registers | 
[**Invoke-PosCreateTable**](PosApi.md#Invoke-PosCreateTable) | **POST** /api/pos/tables | 
[**Invoke-PosDisableRegister**](PosApi.md#Invoke-PosDisableRegister) | **POST** /api/pos/registers/{id}/disable | 
[**Invoke-PosFreeTable**](PosApi.md#Invoke-PosFreeTable) | **POST** /api/pos/tables/{id}/free | 
[**Invoke-PosKasseClosing**](PosApi.md#Invoke-PosKasseClosing) | **POST** /api/pos/kasse/closing | 
[**Invoke-PosKasseEntries**](PosApi.md#Invoke-PosKasseEntries) | **GET** /api/pos/kasse/entries | 
[**Invoke-PosKasseExport**](PosApi.md#Invoke-PosKasseExport) | **GET** /api/pos/kasse/export | 
[**Invoke-PosKassePayInOut**](PosApi.md#Invoke-PosKassePayInOut) | **POST** /api/pos/kasse/pay-in-out | 
[**Invoke-PosListOrders**](PosApi.md#Invoke-PosListOrders) | **GET** /api/pos/orders | 
[**Invoke-PosListProducts**](PosApi.md#Invoke-PosListProducts) | **GET** /api/pos/products | 
[**Invoke-PosListRegisters**](PosApi.md#Invoke-PosListRegisters) | **GET** /api/pos/registers | 
[**Invoke-PosListTables**](PosApi.md#Invoke-PosListTables) | **GET** /api/pos/tables | 
[**Invoke-PosOrderPrint**](PosApi.md#Invoke-PosOrderPrint) | **GET** /api/pos/orders/{order_number}/print | 
[**Invoke-PosOrderReceipt**](PosApi.md#Invoke-PosOrderReceipt) | **GET** /api/pos/orders/{order_number}/receipt | 
[**Invoke-PosPayOrder**](PosApi.md#Invoke-PosPayOrder) | **POST** /api/pos/orders/{order_number}/pay | 
[**Invoke-PosSumupCheckout**](PosApi.md#Invoke-PosSumupCheckout) | **POST** /api/pos/sumup/checkout | 


<a id="Invoke-PosBilling"></a>
# **Invoke-PosBilling**
> AnyType Invoke-PosBilling<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-PosBilling
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosBilling: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosCreateOrder"></a>
# **Invoke-PosCreateOrder**
> AnyType Invoke-PosCreateOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = Invoke-PosCreateOrder -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosCreateOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosCreateRegister"></a>
# **Invoke-PosCreateRegister**
> PosRegister Invoke-PosCreateRegister<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PosRegisterCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PosRegisterCreate = Initialize-PosRegisterCreate -Name "MyName" -Status "active" # PosRegisterCreate | 

try {
    $Result = Invoke-PosCreateRegister -PosRegisterCreate $PosRegisterCreate
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosCreateRegister: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PosRegisterCreate** | [**PosRegisterCreate**](PosRegisterCreate.md)|  | 

### Return type

[**PosRegister**](PosRegister.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosCreateTable"></a>
# **Invoke-PosCreateTable**
> PosTable Invoke-PosCreateTable<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PosTableCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PosTableCreate = Initialize-PosTableCreate -CurrentOrderNumber "MyCurrentOrderNumber" -Name "MyName" -Status "free" # PosTableCreate | 

try {
    $Result = Invoke-PosCreateTable -PosTableCreate $PosTableCreate
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosCreateTable: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PosTableCreate** | [**PosTableCreate**](PosTableCreate.md)|  | 

### Return type

[**PosTable**](PosTable.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosDisableRegister"></a>
# **Invoke-PosDisableRegister**
> PosRegister Invoke-PosDisableRegister<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PosDisableRegister -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosDisableRegister: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**PosRegister**](PosRegister.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosFreeTable"></a>
# **Invoke-PosFreeTable**
> PosTable Invoke-PosFreeTable<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PosFreeTable -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosFreeTable: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**PosTable**](PosTable.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosKasseClosing"></a>
# **Invoke-PosKasseClosing**
> AnyType Invoke-PosKasseClosing<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = Invoke-PosKasseClosing -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosKasseClosing: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosKasseEntries"></a>
# **Invoke-PosKasseEntries**
> AnyType Invoke-PosKasseEntries<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-PosKasseEntries
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosKasseEntries: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosKasseExport"></a>
# **Invoke-PosKasseExport**
> AnyType Invoke-PosKasseExport<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-PosKasseExport
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosKasseExport: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosKassePayInOut"></a>
# **Invoke-PosKassePayInOut**
> AnyType Invoke-PosKassePayInOut<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = Invoke-PosKassePayInOut -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosKassePayInOut: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosListOrders"></a>
# **Invoke-PosListOrders**
> AnyType Invoke-PosListOrders<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Status = "MyStatus" # String | Filter by order status (optional)

try {
    $Result = Invoke-PosListOrders -Status $Status
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosListOrders: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Status** | **String**| Filter by order status | [optional] 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosListProducts"></a>
# **Invoke-PosListProducts**
> AnyType Invoke-PosListProducts<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Q] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Q = "MyQ" # String | Product search (optional)

try {
    $Result = Invoke-PosListProducts -Q $Q
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosListProducts: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Q** | **String**| Product search | [optional] 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosListRegisters"></a>
# **Invoke-PosListRegisters**
> PosRegister[] Invoke-PosListRegisters<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-PosListRegisters
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosListRegisters: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PosRegister[]**](PosRegister.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosListTables"></a>
# **Invoke-PosListTables**
> PosTable[] Invoke-PosListTables<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-PosListTables
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosListTables: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PosTable[]**](PosTable.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosOrderPrint"></a>
# **Invoke-PosOrderPrint**
> AnyType Invoke-PosOrderPrint<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 

try {
    $Result = Invoke-PosOrderPrint -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosOrderPrint: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosOrderReceipt"></a>
# **Invoke-PosOrderReceipt**
> AnyType Invoke-PosOrderReceipt<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 

try {
    $Result = Invoke-PosOrderReceipt -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosOrderReceipt: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosPayOrder"></a>
# **Invoke-PosPayOrder**
> AnyType Invoke-PosPayOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 
$Body =  # AnyType | 

try {
    $Result = Invoke-PosPayOrder -OrderNumber $OrderNumber -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosPayOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PosSumupCheckout"></a>
# **Invoke-PosSumupCheckout**
> AnyType Invoke-PosSumupCheckout<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = Invoke-PosSumupCheckout -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-PosSumupCheckout: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

