# Contact
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountHolder** | **String** |  | [optional] 
**AcquisitionCost** | **String** |  | [optional] 
**AddressSupplement** | **String** |  | [optional] 
**Attention** | **String** |  | [optional] 
**BankName** | **String** |  | [optional] 
**Bic** | **String** |  | [optional] 
**BuyerReference** | **String** |  | [optional] 
**Category** | **String** |  | [optional] 
**CertificateAuthority** | **String** |  | [optional] 
**CertificateNumber** | **String** |  | [optional] 
**CertificateParagraph** | **String** |  | [optional] 
**CertificateValidUntil** | **String** |  | [optional] 
**City** | **String** |  | [optional] 
**CompanyName** | **String** |  | [optional] 
**ContactId** | **String** |  | 
**ContactPersons** | [**AnyType**](.md) |  | 
**ContactType** | **String** |  | 
**Country** | **String** |  | [optional] 
**CreatedAt** | **String** |  | [readonly] 
**CreditLimit** | **String** |  | [optional] 
**CreditorAccountSkr03** | **String** |  | [optional] 
**CreditorAccountSkr04** | **String** |  | [optional] 
**Currency** | **String** |  | [optional] 
**CustomerNumber** | **String** |  | [optional] 
**DebitorAccountSkr03** | **String** |  | [optional] 
**DebitorAccountSkr04** | **String** |  | [optional] 
**DefaultDebitorNumber** | **String** |  | [optional] 
**DeliveryBlock** | **Boolean** |  | [optional] 
**Department** | **String** |  | [optional] 
**DiscountDays** | **Int32** |  | [optional] 
**DiscountPercentage** | **String** |  | [optional] 
**DonationReceiptEligible** | **Boolean** |  | [optional] 
**Email** | **String** |  | [optional] 
**ExternalId** | **String** |  | [optional] 
**Fax** | **String** |  | [optional] 
**Iban** | **String** |  | [optional] 
**Industry** | **String** |  | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**IsMember** | **Boolean** |  | [optional] 
**IsNonprofit** | **Boolean** |  | [optional] 
**LastContactDate** | **String** |  | [optional] 
**LastPurchaseDate** | **String** |  | [optional] 
**LeitwegId** | **String** |  | [optional] 
**LifetimeValue** | **String** |  | [optional] 
**MandateDate** | **String** |  | [optional] 
**MandateReference** | **String** |  | [optional] 
**MarketingConsent** | **Boolean** |  | [optional] 
**MarketingConsentAt** | **String** |  | [optional] 
**MarketingConsentSource** | **String** |  | [optional] 
**Mobile** | **String** |  | [optional] 
**Name** | **String** |  | 
**NextContactDate** | **String** |  | [optional] 
**Notes** | **String** |  | [optional] 
**OpeningBalance** | **String** |  | [optional] 
**OpeningBalanceDate** | **String** |  | [optional] 
**OrderReference** | **String** |  | [optional] 
**PaymentBlock** | **Boolean** |  | [optional] 
**PaymentGracePeriodDays** | **Int32** |  | [optional] 
**PaymentMethods** | **String[]** |  | [optional] 
**PaymentTerms** | **String** |  | [optional] 
**Phone** | **String** |  | [optional] 
**Rating** | **Int32** |  | [optional] 
**SalesRepresentative** | **String** |  | [optional] 
**SocialMedia** | [**AnyType**](.md) |  | 
**Source** | **String** |  | [optional] 
**State** | **String** |  | [optional] 
**Street** | **String** |  | [optional] 
**StreetNumber** | **String** |  | [optional] 
**SupplierNumber** | **String** |  | [optional] 
**Tags** | **String[]** |  | [optional] 
**TaxCountry** | **String** |  | [optional] 
**TaxNumber** | **String** |  | [optional] 
**TaxOffice** | **String** |  | [optional] 
**TotalInvoices** | **Int32** |  | [optional] 
**TotalRevenue** | **String** |  | [optional] 
**UpdatedAt** | **String** |  | [optional] [readonly] 
**VatId** | **String** |  | [optional] 
**VatIdValidated** | **Boolean** |  | [optional] 
**VatIdValidationDate** | **String** |  | [optional] 
**Website** | **String** |  | [optional] 
**Zip** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Contact = Initialize-PSOpenAPIToolsContact  -AccountHolder null `
 -AcquisitionCost null `
 -AddressSupplement null `
 -Attention null `
 -BankName null `
 -Bic null `
 -BuyerReference null `
 -Category null `
 -CertificateAuthority null `
 -CertificateNumber null `
 -CertificateParagraph null `
 -CertificateValidUntil null `
 -City null `
 -CompanyName null `
 -ContactId null `
 -ContactPersons null `
 -ContactType null `
 -Country null `
 -CreatedAt null `
 -CreditLimit null `
 -CreditorAccountSkr03 null `
 -CreditorAccountSkr04 null `
 -Currency null `
 -CustomerNumber null `
 -DebitorAccountSkr03 null `
 -DebitorAccountSkr04 null `
 -DefaultDebitorNumber null `
 -DeliveryBlock null `
 -Department null `
 -DiscountDays null `
 -DiscountPercentage null `
 -DonationReceiptEligible null `
 -Email null `
 -ExternalId null `
 -Fax null `
 -Iban null `
 -Industry null `
 -IsActive null `
 -IsMember null `
 -IsNonprofit null `
 -LastContactDate null `
 -LastPurchaseDate null `
 -LeitwegId null `
 -LifetimeValue null `
 -MandateDate null `
 -MandateReference null `
 -MarketingConsent null `
 -MarketingConsentAt null `
 -MarketingConsentSource null `
 -Mobile null `
 -Name null `
 -NextContactDate null `
 -Notes null `
 -OpeningBalance null `
 -OpeningBalanceDate null `
 -OrderReference null `
 -PaymentBlock null `
 -PaymentGracePeriodDays null `
 -PaymentMethods null `
 -PaymentTerms null `
 -Phone null `
 -Rating null `
 -SalesRepresentative null `
 -SocialMedia null `
 -Source null `
 -State null `
 -Street null `
 -StreetNumber null `
 -SupplierNumber null `
 -Tags null `
 -TaxCountry null `
 -TaxNumber null `
 -TaxOffice null `
 -TotalInvoices null `
 -TotalRevenue null `
 -UpdatedAt null `
 -VatId null `
 -VatIdValidated null `
 -VatIdValidationDate null `
 -Website null `
 -Zip null
```

- Convert the resource to JSON
```powershell
$Contact | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

