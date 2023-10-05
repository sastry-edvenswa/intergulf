#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProfileForm

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProfileForm]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:15:17 PM Monday, January 29, 2007 |
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
| WasteCode | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProcessDescription | varchar(3000) | 3000 |
| MaterialClassification | varchar(200) | 200 |
| StateWasteCode | varchar(50) | 50 |
| SICCode | varchar(50) | 50 |
| Volume | varchar(50) | 50 |
| LoadFrequency | varchar(50) | 50 |
| Viscosity | varchar(50) | 50 |
| PhRange | varchar(50) | 50 |
| SpecificGravity | varchar(50) | 50 |
| FlashPoint | varchar(50) | 50 |
| Phase | varchar(50) | 50 |
| ViscosityOther | varchar(50) | 50 |
| PhRangeOther | varchar(50) | 50 |
| SpecificGravityOther | varchar(50) | 50 |
| FlashPointOther | varchar(50) | 50 |
| PhaseOther | varchar(50) | 50 |
| OtherComments | varchar(50) | 50 |
| ShippingName | varchar(1000) | 1000 |
| ShippingMethod | varchar(50) | 50 |
| SpecialEquipment | varchar(3000) | 3000 |
| SpecialInstructions | varchar(3000) | 3000 |
| DocumentType | varchar(50) | 50 |
| Placards | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| HTYes | varchar(50) | 50 |
| HTNo | varchar(50) | 50 |
| HTPK | varchar(50) | 50 |
| HTAD | varchar(50) | 50 |
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
| PMTestType | varchar(50) | 50 |
| PMTestBase | numeric(18,2) | 9 |
| PMTestIncrement | numeric(18,2) | 9 |
| PMTestTote | numeric(18,3) | 9 |
| PMTestGallon | numeric(18,3) | 9 |
| PMTestDrum | numeric(18,3) | 9 |
| PMTestBarrel | numeric(18,2) | 9 |
| PMSolidsTestType | varchar(50) | 50 |
| PMSolidsBase | numeric(18,2) | 9 |
| PMSolidsIncrement | numeric(18,2) | 9 |
| PMSolidsTote | numeric(18,2) | 9 |
| PMSolidsGallon | numeric(18,3) | 9 |
| PMSolidsDrum | numeric(18,3) | 9 |
| PMSolidsBarrel | numeric(18,3) | 9 |
| PMMetals | numeric(18,2) | 9 |
| PMAmmonia | numeric(18,2) | 9 |
| Status | varchar(20) | 20 |
| StatusDescription | varchar(2000) | 2000 |
| SpecialBilling | bigint | 8 |
| EffectiveDate | datetime | 8 |
| DeepWell | char(10) | 10 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProfileForm]
AS
SELECT     TOP 100 PERCENT Profile.CustomerId AS [Customer Id], dbo.Customer.Name AS [Customer Name], Profile.GeneratorId AS [Generator Id], 
                      dbo.Generator.Name AS [Generator Name], Profile.Id AS [Profile Id], Profile.ProfileNumber AS [Profile Name], Profile.TransporterId, Profile.WasteCode, 
                      Profile.MaterialDescription, Profile.ProcessDescription, Profile.MaterialClassification, Profile.StateWasteCode, Profile.SICCode, Profile.Volume, 
                      Profile.LoadFrequency, Profile.Viscosity, Profile.PhRange, Profile.SpecificGravity, Profile.FlashPoint, Profile.Phase, Profile.ViscosityOther, 
                      Profile.PhRangeOther, Profile.SpecificGravityOther, Profile.FlashPointOther, Profile.PhaseOther, Profile.OtherComments, Profile.ShippingName, 
                      Profile.ShippingMethod, Profile.SpecialEquipment, Profile.SpecialInstructions, Profile.DocumentType, Profile.Placards, Profile.ProfileType, 
                      Profile.HTYes, Profile.HTNo, Profile.HTPK, Profile.HTAD, Profile.Notes, Profile.SalesPersonId, Profile.Direction, Profile.Type, dbo.Generator.Address, 
                      dbo.Generator.City, dbo.Generator.State, dbo.Generator.Zip, dbo.Generator.BillingName, dbo.Generator.BillingAddress, dbo.Generator.BillingCity, 
                      dbo.Generator.BillingState, dbo.Generator.BillingZip, dbo.Generator.Contact, dbo.Generator.Phone, dbo.Generator.Fax, dbo.Generator.Email, 
                      dbo.Generator.RegistrationNo, dbo.Generator.EpaIdNo, dbo.Generator.Type AS [Generator Type], dbo.Generator.Classification, dbo.Transporter.Name, 
                      dbo.Transporter.Contact AS [Transporter Contact], dbo.Transporter.Phone AS [Transporter Phone], dbo.Transporter.EpaIdNo AS [Transporter Epa No], 
                      dbo.Transporter.TceqNo AS [Transporter Tceq No], dbo.UserMaster.FirstName, dbo.UserMaster.LastName, Profile.PMTote, Profile.PMGallon, 
                      Profile.PMDrum, Profile.PMBarrel, Profile.PTHour, Profile.PTLoad, Profile.PTGallon, Profile.PTDemurrage, Profile.PTFreeTime, Profile.PTFuelSerCharge,
                       Profile.PTHourMin, Profile.PTGallonMin, Profile.PMTestType, Profile.PMTestBase, Profile.PMTestIncrement, Profile.PMTestTote, Profile.PMTestGallon, 
                      Profile.PMTestDrum, Profile.PMTestBarrel, Profile.PMSolidsTestType, Profile.PMSolidsBase, Profile.PMSolidsIncrement, Profile.PMSolidsTote, 
                      Profile.PMSolidsGallon, Profile.PMSolidsDrum, Profile.PMSolidsBarrel, Profile.PMMetals, Profile.PMAmmonia, Profile.Status, Profile.StatusDescription, 
                      Profile.SpecialBilling, Profile.EffectiveDate, Profile.DeepWell
FROM         dbo.Profile Profile LEFT OUTER JOIN
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

