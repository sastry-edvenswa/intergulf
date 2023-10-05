#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProfileFormProduct

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProfileFormProduct]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:17:00 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Customer Id | bigint | 8 |
| Customer Name | varchar(50) | 50 |
| Generator Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Profile Id | bigint | 8 |
| Profile Name | varchar(50) | 50 |
| TransporterId | bigint | 8 |
| MaterialDescription | varchar(3000) | 3000 |
| Volume | varchar(50) | 50 |
| LoadFrequency | varchar(50) | 50 |
| ShippingName | varchar(1000) | 1000 |
| ShippingMethod | varchar(50) | 50 |
| SpecialEquipment | varchar(3000) | 3000 |
| SpecialInstructions | varchar(3000) | 3000 |
| DocumentType | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| Notes | varchar(5000) | 5000 |
| SalesPersonId | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| Address | varchar(50) | 50 |
| City | varchar(50) | 50 |
| State | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| BillingName | varchar(50) | 50 |
| BillingAddress | varchar(50) | 50 |
| BillingCity | varchar(50) | 50 |
| BillingState | varchar(50) | 50 |
| BillingZip | varchar(50) | 50 |
| Contact | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| Fax | varchar(50) | 50 |
| Email | varchar(50) | 50 |
| RegistrationNo | varchar(50) | 50 |
| EpaIdNo | varchar(50) | 50 |
| Generator Type | varchar(50) | 50 |
| Classification | varchar(50) | 50 |
| Name | varchar(50) | 50 |
| Transporter Contact | varchar(50) | 50 |
| Transporter Phone | varchar(50) | 50 |
| Transporter Epa No | varchar(50) | 50 |
| Transporter Tceq No | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| PMTote | numeric(18,3) | 9 |
| PMGallon | numeric(18,3) | 9 |
| PMDrum | numeric(18,3) | 9 |
| PMBarrel | numeric(18,3) | 9 |
| PTHour | numeric(18,2) | 9 |
| PTLoad | numeric(18,2) | 9 |
| PTGallon | numeric(18,2) | 9 |
| PTDemurrage | numeric(18,2) | 9 |
| PTFreeTime | numeric(18,0) | 9 |
| PTFuelSerCharge | numeric(18,0) | 9 |
| PTHourMin | numeric(18,2) | 9 |
| PTGallonMin | numeric(18,2) | 9 |
| Status | varchar(20) | 20 |
| StatusDescription | varchar(2000) | 2000 |
| SpecialBilling | bigint | 8 |
| MinFlashPoint | numeric(18,0) | 9 |
| MaxCentrifugeSolidsPcnt | numeric(18,0) | 9 |
| MaxFreePhaseWaterPcnt | numeric(18,0) | 9 |
| MaxFreePhaseOrganicPcnt | numeric(18,0) | 9 |
| MaxWaterByHach | numeric(18,0) | 9 |
| MaxChlordetect | numeric(18,0) | 9 |
| MaxViscosity | numeric(18,0) | 9 |
| MaxTotalAcid | numeric(18,0) | 9 |
| MinAPIGravity | numeric(18,0) | 9 |
| MaxWaterByDistillationPcnt | numeric(18,0) | 9 |
| MaxAshWtPcnt | numeric(18,0) | 9 |
| MaxPPMP | numeric(18,0) | 9 |
| MaxSulfur | numeric(18,0) | 9 |
| Compatibility | varchar(3000) | 3000 |
| ProductComments | varchar(3000) | 3000 |
| MaxSilicone | numeric(18,0) | 9 |
| MaxSodium | numeric(18,0) | 9 |
| MaxVanadium | numeric(18,0) | 9 |
| MaxAluminum | numeric(18,0) | 9 |
| EffectiveDate | datetime | 8 |
| Placards | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProfileFormProduct]
AS
SELECT     TOP 100 PERCENT Profile.CustomerId AS [Customer Id], dbo.Customer.Name AS [Customer Name], Profile.GeneratorId AS [Generator Id], 
                      dbo.Generator.Name AS [Generator Name], Profile.Id AS [Profile Id], Profile.ProfileNumber AS [Profile Name], Profile.TransporterId, 
                      Profile.MaterialDescription, Profile.Volume, Profile.LoadFrequency, Profile.ShippingName, Profile.ShippingMethod, Profile.SpecialEquipment, 
                      Profile.SpecialInstructions, Profile.DocumentType, Profile.ProfileType, Profile.Notes, Profile.SalesPersonId, Profile.Direction, Profile.Type, 
                      dbo.Generator.Address, dbo.Generator.City, dbo.Generator.State, dbo.Generator.Zip, dbo.Generator.BillingName, dbo.Generator.BillingAddress, 
                      dbo.Generator.BillingCity, dbo.Generator.BillingState, dbo.Generator.BillingZip, dbo.Generator.Contact, dbo.Generator.Phone, dbo.Generator.Fax, 
                      dbo.Generator.Email, dbo.Generator.RegistrationNo, dbo.Generator.EpaIdNo, dbo.Generator.Type AS [Generator Type], dbo.Generator.Classification, 
                      dbo.Transporter.Name, dbo.Transporter.Contact AS [Transporter Contact], dbo.Transporter.Phone AS [Transporter Phone], 
                      dbo.Transporter.EpaIdNo AS [Transporter Epa No], dbo.Transporter.TceqNo AS [Transporter Tceq No], dbo.UserMaster.FirstName, 
                      dbo.UserMaster.LastName, Profile.PMTote, Profile.PMGallon, Profile.PMDrum, Profile.PMBarrel, Profile.PTHour, Profile.PTLoad, Profile.PTGallon, 
                      Profile.PTDemurrage, Profile.PTFreeTime, Profile.PTFuelSerCharge, Profile.PTHourMin, Profile.PTGallonMin, Profile.Status, Profile.StatusDescription, 
                      Profile.SpecialBilling, Profile.MinFlashPoint, Profile.MaxCentrifugeSolidsPcnt, Profile.MaxFreePhaseWaterPcnt, Profile.MaxFreePhaseOrganicPcnt, 
                      Profile.MaxWaterByHach, Profile.MaxChlordetect, Profile.MaxViscosity, Profile.MaxTotalAcid, Profile.MinAPIGravity, 
                      Profile.MaxWaterByDistillationPcnt, Profile.MaxAshWtPcnt, Profile.MaxPPMP, Profile.MaxSulfur, Profile.Compatibility, Profile.ProductComments, 
                      Profile.MaxSilicone, Profile.MaxSodium, Profile.MaxVanadium, Profile.MaxAluminum, Profile.EffectiveDate, Profile.Placards
FROM         dbo.Profile Profile INNER JOIN
                      dbo.UserMaster ON Profile.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                      dbo.Generator ON Profile.GeneratorId = dbo.Generator.Id LEFT OUTER JOIN
                      dbo.Customer ON Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                      dbo.Transporter ON Profile.TransporterId = dbo.Transporter.Id
ORDER BY dbo.Customer.Name, dbo.Generator.Name, Profile.ProfileNumber
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

