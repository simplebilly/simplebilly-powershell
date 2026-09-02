# CustomerGroupCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **String** |  | [optional] 
**MemberIds** | **String[]** | Contact ids that are members of this group. | [optional] 
**MembershipFilter** | **String** | Rule description for membership, e.g. &quot;&quot;orders &gt; 5 last 12 months&quot;&quot;. | [optional] 
**Name** | **String** | Unique group name, e.g. &quot;&quot;VIP&quot;&quot;, &quot;&quot;Wholesale&quot;&quot;, &quot;&quot;Newsletter&quot;&quot;. | 

## Examples

- Prepare the resource
```powershell
$CustomerGroupCreate = Initialize-PSOpenAPIToolsCustomerGroupCreate  -Description null `
 -MemberIds null `
 -MembershipFilter null `
 -Name null
```

- Convert the resource to JSON
```powershell
$CustomerGroupCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

