# PSOpenAPITools.PSOpenAPITools\Api.ProductApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ProductApi**](ProductApi.md#New-ProductApi) | **POST** /api/v1/products | 
[**Invoke-DeleteProductApi**](ProductApi.md#Invoke-DeleteProductApi) | **DELETE** /api/v1/products/{product_id} | 
[**Get-ProductApi**](ProductApi.md#Get-ProductApi) | **GET** /api/v1/products/{product_id} | 
[**Get-ProductStockApi**](ProductApi.md#Get-ProductStockApi) | **GET** /api/v1/products/{product_id}/stock | 
[**Get-ProductsApi**](ProductApi.md#Get-ProductsApi) | **GET** /api/v1/products/ | 
[**Invoke-ListLowStockProductsApi**](ProductApi.md#Invoke-ListLowStockProductsApi) | **GET** /api/v1/products/low-stock | 
[**Invoke-ProductRestore**](ProductApi.md#Invoke-ProductRestore) | **POST** /api/v1/products/{product_id}/restore | 
[**Update-ProductApi**](ProductApi.md#Update-ProductApi) | **PUT** /api/v1/products/{product_id} | 
[**Update-ProductStockApi**](ProductApi.md#Update-ProductStockApi) | **PUT** /api/v1/products/{product_id}/stock | 


<a id="New-ProductApi"></a>
# **New-ProductApi**
> Product New-ProductApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductCreate = Initialize-ProductCreate -Availability "MyAvailability" -Barcode "MyBarcode" -Brand "MyBrand" -CategoryId "MyCategoryId" -Condition "MyCondition" -DefaultLedgerAccount "MyDefaultLedgerAccount" -DefaultPrice "MyDefaultPrice" -DefaultPriceFormulaId "MyDefaultPriceFormulaId" -DefaultTaxRate "MyDefaultTaxRate" -Description "MyDescription" -Gtin "MyGtin" -Height "MyHeight" -ImageLink "MyImageLink" -Images  -IsTaxable $false -Length "MyLength" -Link "MyLink" -MaxStock 0 -MinStock 0 -Mpn "MyMpn" -Name "MyName" -PackageHeight "MyPackageHeight" -PackageLength "MyPackageLength" -PackageWeightUnit "MyPackageWeightUnit" -PackageWeightValue "MyPackageWeightValue" -PackageWidth "MyPackageWidth" -ProductCode "MyProductCode" -ProductType "MyProductType" -PurchasePrice "MyPurchasePrice" -ReorderQuantity 0 -SalePrice "MySalePrice" -ShippingPrice "MyShippingPrice" -ShippingRequiresInsurance $false -Sku "MySku" -StockQuantity 0 -Tags  -TaxPrice "MyTaxPrice" -TrackBatch $false -TrackSerial $false -Unit  -WeightUnit "MyWeightUnit" -WeightValue "MyWeightValue" -Width "MyWidth" # ProductCreate | 

try {
    $Result = New-ProductApi -ProductCreate $ProductCreate
} catch {
    Write-Host ("Exception occurred when calling New-ProductApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductCreate** | [**ProductCreate**](ProductCreate.md)|  | 

### Return type

[**Product**](Product.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteProductApi"></a>
# **Invoke-DeleteProductApi**
> void Invoke-DeleteProductApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteProductApi -ProductId $ProductId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteProductApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProductApi"></a>
# **Get-ProductApi**
> Product Get-ProductApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-ProductApi -ProductId $ProductId
} catch {
    Write-Host ("Exception occurred when calling Get-ProductApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 

### Return type

[**Product**](Product.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProductStockApi"></a>
# **Get-ProductStockApi**
> ProductStock Get-ProductStockApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-ProductStockApi -ProductId $ProductId
} catch {
    Write-Host ("Exception occurred when calling Get-ProductStockApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 

### Return type

[**ProductStock**](ProductStock.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProductsApi"></a>
# **Get-ProductsApi**
> Product[] Get-ProductsApi<br>
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
    $Result = Get-ProductsApi -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-ProductsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**Product[]**](Product.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListLowStockProductsApi"></a>
# **Invoke-ListLowStockProductsApi**
> ProductStock[] Invoke-ListLowStockProductsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Threshold] <System.Nullable[Int64]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Threshold = 789 # Int64 |  (optional)

try {
    $Result = Invoke-ListLowStockProductsApi -Threshold $Threshold
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListLowStockProductsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Threshold** | **Int64**|  | [optional] 

### Return type

[**ProductStock[]**](ProductStock.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ProductRestore"></a>
# **Invoke-ProductRestore**
> Product Invoke-ProductRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-ProductRestore -ProductId $ProductId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ProductRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 

### Return type

[**Product**](Product.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProductApi"></a>
# **Update-ProductApi**
> Product Update-ProductApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ProductUpdate = Initialize-ProductUpdate -Availability "MyAvailability" -Barcode "MyBarcode" -Brand "MyBrand" -CategoryId "MyCategoryId" -Condition "MyCondition" -DefaultLedgerAccount "MyDefaultLedgerAccount" -DefaultPrice "MyDefaultPrice" -DefaultPriceFormulaId "MyDefaultPriceFormulaId" -DefaultTaxRate "MyDefaultTaxRate" -Description "MyDescription" -Gtin "MyGtin" -Height "MyHeight" -ImageLink "MyImageLink" -Images  -IsTaxable $false -Length "MyLength" -Link "MyLink" -MaxStock 0 -MinStock 0 -Mpn "MyMpn" -Name "MyName" -PackageHeight "MyPackageHeight" -PackageLength "MyPackageLength" -PackageWeightUnit "MyPackageWeightUnit" -PackageWeightValue "MyPackageWeightValue" -PackageWidth "MyPackageWidth" -ProductCode "MyProductCode" -ProductType "MyProductType" -PurchasePrice "MyPurchasePrice" -ReorderQuantity 0 -SalePrice "MySalePrice" -ShippingPrice "MyShippingPrice" -ShippingRequiresInsurance $false -Sku "MySku" -StockQuantity 0 -Tags  -TaxPrice "MyTaxPrice" -TrackBatch $false -TrackSerial $false -Unit  -WeightUnit "MyWeightUnit" -WeightValue "MyWeightValue" -Width "MyWidth" # ProductUpdate | 

try {
    $Result = Update-ProductApi -ProductId $ProductId -ProductUpdate $ProductUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ProductApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 
 **ProductUpdate** | [**ProductUpdate**](ProductUpdate.md)|  | 

### Return type

[**Product**](Product.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProductStockApi"></a>
# **Update-ProductStockApi**
> ProductStock Update-ProductStockApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockUpdateRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$StockUpdateRequest = Initialize-StockUpdateRequest -Quantity 0 # StockUpdateRequest | 

try {
    $Result = Update-ProductStockApi -ProductId $ProductId -StockUpdateRequest $StockUpdateRequest
} catch {
    Write-Host ("Exception occurred when calling Update-ProductStockApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 
 **StockUpdateRequest** | [**StockUpdateRequest**](StockUpdateRequest.md)|  | 

### Return type

[**ProductStock**](ProductStock.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

