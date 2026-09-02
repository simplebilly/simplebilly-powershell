# ContactUpdate
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
**CertificateValidUntil** | **System.DateTime** |  | [optional] 
**City** | **String** |  | [optional] 
**CompanyName** | **String** |  | [optional] 
**ContactPersons** | [**AnyType**](.md) |  | [optional] 
**ContactType** | [**ContactType**](ContactType.md) |  | [optional] 
**Country** | [**CountryCode**](CountryCode.md) |  | [optional] 
**CreditLimit** | **String** |  | [optional] 
**CreditorAccountSkr03** | **String** |  | [optional] 
**CreditorAccountSkr04** | **String** |  | [optional] 
**Currency** | **String** |  | [optional] 
**CustomFields** | [**AnyType**](.md) |  | [optional] 
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
**LastContactDate** | **System.DateTime** |  | [optional] 
**LastPurchaseDate** | **System.DateTime** |  | [optional] 
**LeitwegId** | **String** |  | [optional] 
**LifetimeValue** | **String** |  | [optional] 
**MandateDate** | **System.DateTime** |  | [optional] 
**MandateReference** | **String** |  | [optional] 
**MarketingConsent** | **Boolean** |  | [optional] 
**MarketingConsentAt** | **System.DateTime** |  | [optional] 
**MarketingConsentSource** | **String** |  | [optional] 
**Mobile** | **String** |  | [optional] 
**Name** | **String** |  | [optional] 
**NextContactDate** | **System.DateTime** |  | [optional] 
**Notes** | **String** |  | [optional] 
**OpeningBalance** | **String** |  | [optional] 
**OpeningBalanceDate** | **System.DateTime** |  | [optional] 
**OrderReference** | **String** |  | [optional] 
**PaymentBlock** | **Boolean** |  | [optional] 
**PaymentGracePeriodDays** | **Int32** |  | [optional] 
**PaymentMethods** | **String[]** |  | [optional] 
**PaymentTerms** | **String** |  | [optional] 
**Phone** | **String** |  | [optional] 
**Rating** | **Int32** |  | [optional] 
**SalesRepresentative** | **String** |  | [optional] 
**SepaBatchBooking** | **Boolean** |  | [optional] 
**SepaSequenceType** | [**SepaSequenceType**](SepaSequenceType.md) |  | [optional] 
**SocialMedia** | [**AnyType**](.md) |  | [optional] 
**Source** | **String** |  | [optional] 
**State** | **String** |  | [optional] 
**Street** | **String** |  | [optional] 
**StreetNumber** | **String** |  | [optional] 
**SupplierNumber** | **String** |  | [optional] 
**Tags** | **String[]** |  | [optional] 
**TaxCountry** | [**CountryCode**](CountryCode.md) |  | [optional] 
**TaxNumber** | **String** |  | [optional] 
**TaxOffice** | **String** |  | [optional] 
**TotalInvoices** | **Int32** |  | [optional] 
**TotalRevenue** | **String** |  | [optional] 
**VatId** | **String** |  | [optional] 
**VatIdValidated** | **Boolean** |  | [optional] 
**VatIdValidationDate** | **System.DateTime** |  | [optional] 
**Website** | **String** |  | [optional] 
**Zip** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ContactUpdate = Initialize-PSOpenAPIToolsContactUpdate  -AccountHolder null `
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
 -ContactPersons null `
 -ContactType null `
 -Country null `
 -CreditLimit null `
 -CreditorAccountSkr03 null `
 -CreditorAccountSkr04 null `
 -Currency null `
 -CustomFields null `
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
 -SepaBatchBooking null `
 -SepaSequenceType null `
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
 -VatId null `
 -VatIdValidated null `
 -VatIdValidationDate null `
 -Website null `
 -Zip null
```

- Convert the resource to JSON
```powershell
$ContactUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

