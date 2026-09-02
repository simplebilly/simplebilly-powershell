# AnlageSErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GewinnVerlust** | **String** |  | 
**Jahr** | **Int32** |  | 
**KfzHinweise** | [**AnlageSKfzHinweis[]**](AnlageSKfzHinweis.md) |  | 

## Examples

- Prepare the resource
```powershell
$AnlageSErgebnis = Initialize-PSOpenAPIToolsAnlageSErgebnis  -GewinnVerlust null `
 -Jahr null `
 -KfzHinweise null
```

- Convert the resource to JSON
```powershell
$AnlageSErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

