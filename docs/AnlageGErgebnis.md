# AnlageGErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GewinnVerlust** | **String** |  | 
**GewstGezahlt** | **String** |  | 
**GewstMessbetragApprox** | **String** |  | 
**GewstPflichtig** | **Boolean** |  | 
**Jahr** | **Int32** |  | 
**KfzHinweise** | [**AnlageGKfzHinweis[]**](AnlageGKfzHinweis.md) |  | 

## Examples

- Prepare the resource
```powershell
$AnlageGErgebnis = Initialize-PSOpenAPIToolsAnlageGErgebnis  -GewinnVerlust null `
 -GewstGezahlt null `
 -GewstMessbetragApprox null `
 -GewstPflichtig null `
 -Jahr null `
 -KfzHinweise null
```

- Convert the resource to JSON
```powershell
$AnlageGErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

