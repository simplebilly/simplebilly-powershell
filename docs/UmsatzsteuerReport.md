# UmsatzsteuerReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GeneratedAt** | **String** |  | 
**InputTax** | [**VatDetail[]**](VatDetail.md) |  | 
**OutputTax** | [**VatDetail[]**](VatDetail.md) |  | 
**Period** | **String** |  | 
**TotalInputTax** | **String** |  | 
**TotalOutputTax** | **String** |  | 
**VatPayable** | **String** |  | 
**VatRefund** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$UmsatzsteuerReport = Initialize-PSOpenAPIToolsUmsatzsteuerReport  -GeneratedAt null `
 -InputTax null `
 -OutputTax null `
 -Period null `
 -TotalInputTax null `
 -TotalOutputTax null `
 -VatPayable null `
 -VatRefund null
```

- Convert the resource to JSON
```powershell
$UmsatzsteuerReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

