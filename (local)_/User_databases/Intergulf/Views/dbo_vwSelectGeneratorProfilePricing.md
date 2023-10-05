#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectGeneratorProfilePricing

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectGeneratorProfilePricing]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:35:34 PM Wednesday, February 27, 2019 |
| Last Modified | 3:35:34 PM Wednesday, February 27, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | numeric(18,0) | 9 |
| Name | varchar(100) | 100 |
| Address | varchar(3000) | 3000 |
| City | varchar(50) | 50 |
| State | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| BillingName | varchar(100) | 100 |
| BillingAddress | varchar(3000) | 3000 |
| BillingCity | varchar(50) | 50 |
| BillingState | varchar(50) | 50 |
| BillingZip | varchar(50) | 50 |
| Contact | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| Fax | varchar(50) | 50 |
| Email | varchar(50) | 50 |
| RegistrationNo | varchar(50) | 50 |
| EpaIdNo | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| Classification | varchar(50) | 50 |
| Facility | varchar(50) | 50 |
| Mid | bigint | 8 |
| MName | varchar(100) | 100 |
| MAddress | varchar(3000) | 3000 |
| MCity | varchar(50) | 50 |
| MState | varchar(50) | 50 |
| MZip | varchar(50) | 50 |
| EId | bigint | 8 |
| EName | varchar(50) | 50 |
| EPhone | varchar(50) | 50 |
| PTHour | numeric(18,2) | 9 |
| PTLoad | numeric(18,2) | 9 |
| PTGallon | numeric(18,2) | 9 |
| PTHourMin | numeric(18,2) | 9 |
| PTGallonMin | numeric(18,2) | 9 |
| PTDemurrage | numeric(18,2) | 9 |
| PTFreeTime | numeric(18,0) | 9 |
| PTFuelSerCharge | numeric(18,0) | 9 |
| PMTestType | varchar(50) | 50 |
| PMTestBase | numeric(18,2) | 9 |
| PMTestIncrement | numeric(18,2) | 9 |
| PMTestGallon | numeric(18,3) | 9 |
| PMTestDrum | numeric(18,3) | 9 |
| PMTestBarrel | numeric(18,2) | 9 |
| PMTestTote | numeric(18,3) | 9 |
| PMSolidsTestType | varchar(50) | 50 |
| PMSolidsBase | numeric(18,2) | 9 |
| PMSolidsIncrement | numeric(18,2) | 9 |
| PMSolidsGallon | numeric(18,3) | 9 |
| PMSolidsDrum | numeric(18,3) | 9 |
| PMSolidsBarrel | numeric(18,3) | 9 |
| PMSolidsTote | numeric(18,2) | 9 |
| PMMetals | numeric(18,2) | 9 |
| PMAmmonia | numeric(18,2) | 9 |
| SpecialBilling | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectGeneratorProfilePricing]
AS
SELECT        dbo.Generator.Id, dbo.Generator.Name, dbo.Generator.Address, dbo.Generator.City, dbo.Generator.State, dbo.Generator.Zip, dbo.Generator.BillingName, dbo.Generator.BillingAddress, dbo.Generator.BillingCity, 
                         dbo.Generator.BillingState, dbo.Generator.BillingZip, dbo.Generator.Contact, dbo.Generator.Phone, dbo.Generator.Fax, dbo.Generator.Email, dbo.Generator.RegistrationNo, dbo.Generator.EpaIdNo, 
                         dbo.Generator.Type, dbo.Generator.Classification, dbo.Generator.Facility, dbo.ManifestMailingAddress.Id AS Mid, dbo.ManifestMailingAddress.Name AS MName, 
                         dbo.ManifestMailingAddress.Address AS MAddress, dbo.ManifestMailingAddress.City AS MCity, dbo.ManifestMailingAddress.State AS MState, dbo.ManifestMailingAddress.Zip AS MZip, 
                         dbo.EmergencyContact.Id AS EId, dbo.EmergencyContact.Name AS EName, dbo.EmergencyContact.Phone AS EPhone, dbo.Profile.PTHour, dbo.Profile.PTLoad, dbo.Profile.PTGallon, dbo.Profile.PTHourMin, 
                         dbo.Profile.PTGallonMin, dbo.Profile.PTDemurrage, dbo.Profile.PTFreeTime, dbo.Profile.PTFuelSerCharge, dbo.Profile.PMTestType, dbo.Profile.PMTestBase, dbo.Profile.PMTestIncrement, 
                         dbo.Profile.PMTestGallon, dbo.Profile.PMTestDrum, dbo.Profile.PMTestBarrel, dbo.Profile.PMTestTote, dbo.Profile.PMSolidsTestType, dbo.Profile.PMSolidsBase, dbo.Profile.PMSolidsIncrement, 
                         dbo.Profile.PMSolidsGallon, dbo.Profile.PMSolidsDrum, dbo.Profile.PMSolidsBarrel, dbo.Profile.PMSolidsTote, dbo.Profile.PMMetals, dbo.Profile.PMAmmonia, dbo.Profile.SpecialBilling
FROM            dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId LEFT OUTER JOIN
                         dbo.EmergencyContact ON dbo.Generator.Id = dbo.EmergencyContact.Id LEFT OUTER JOIN
                         dbo.ManifestMailingAddress ON dbo.Generator.Id = dbo.ManifestMailingAddress.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[EmergencyContact]](../Tables/dbo_EmergencyContact.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[ManifestMailingAddress]](../Tables/dbo_ManifestMailingAddress.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

