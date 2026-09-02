# PSOpenAPITools.PSOpenAPITools\Api.LegalDocumentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-LegalDocuments**](LegalDocumentApi.md#Get-LegalDocuments) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
[**Reset-LegalDocuments**](LegalDocumentApi.md#Reset-LegalDocuments) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
[**Invoke-UpsertLegalDocuments**](LegalDocumentApi.md#Invoke-UpsertLegalDocuments) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list.


<a id="Get-LegalDocuments"></a>
# **Get-LegalDocuments**
> LegalDocument[] Get-LegalDocuments<br>

List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
try {
    $Result = Get-LegalDocuments
} catch {
    Write-Host ("Exception occurred when calling Get-LegalDocuments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**LegalDocument[]**](LegalDocument.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Reset-LegalDocuments"></a>
# **Reset-LegalDocuments**
> LegalDocument[] Reset-LegalDocuments<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-LegalDocumentReset] <PSCustomObject><br>

Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$LegalDocumentReset = Initialize-LegalDocumentReset -DocType "MyDocType" -Lang "MyLang" # LegalDocumentReset | 

# Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
try {
    $Result = Reset-LegalDocuments -LegalDocumentReset $LegalDocumentReset
} catch {
    Write-Host ("Exception occurred when calling Reset-LegalDocuments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **LegalDocumentReset** | [**LegalDocumentReset**](LegalDocumentReset.md)|  | 

### Return type

[**LegalDocument[]**](LegalDocument.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-UpsertLegalDocuments"></a>
# **Invoke-UpsertLegalDocuments**
> LegalDocument[] Invoke-UpsertLegalDocuments<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-LegalDocumentUpsert] <PSCustomObject[]><br>

Upsert legal documents per (doc_type, lang). Returns the full tenant list.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$LegalDocumentUpsert = Initialize-LegalDocumentUpsert -Content "MyContent" -DocType "MyDocType" -Lang "MyLang" -Title "MyTitle" # LegalDocumentUpsert[] | 

# Upsert legal documents per (doc_type, lang). Returns the full tenant list.
try {
    $Result = Invoke-UpsertLegalDocuments -LegalDocumentUpsert $LegalDocumentUpsert
} catch {
    Write-Host ("Exception occurred when calling Invoke-UpsertLegalDocuments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **LegalDocumentUpsert** | [**LegalDocumentUpsert[]**](LegalDocumentUpsert.md)|  | 

### Return type

[**LegalDocument[]**](LegalDocument.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

