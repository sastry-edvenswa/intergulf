#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportProfilesNew

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportProfilesNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:23:20 PM Wednesday, July 18, 2018 |
| Last Modified | 2:29:36 PM Thursday, February 2, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Address | varchar(3000) | 3000 |
| City | varchar(50) | 50 |
| State | varchar(50) | 50 |
| Zip | varchar(50) | 50 |
| RegistrationNo | varchar(50) | 50 |
| EpaIdNo | varchar(50) | 50 |
| Customer Name | varchar(100) | 100 |
| Vendor Name | varchar(50) | 50 |
| Vendor No | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| Transporter Name | varchar(100) | 100 |
| WasteCode | varchar(50) | 50 |
| MaterialCode | nvarchar(50) | 100 |
| Material Code | nvarchar(50) | 100 |
| ProductCategory | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProcessDescription | varchar(3000) | 3000 |
| MaterialClassification | varchar(200) | 200 |
| StateWasteCode | varchar(50) | 50 |
| SICCode | varchar(50) | 50 |
| Volume | varchar(50) | 50 |
| LoadFrequency | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
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
| Destination | nvarchar(100) | 200 |
| DispatchNotes | varchar(6000) | 6000 |
| Approval | varchar(50) | 50 |
| ApprovalBy | varchar(50) | 50 |
| ApprovalDate | datetime | 8 |
| HazMat | varchar(50) | 50 |
| Placards | varchar(50) | 50 |
| PMTote | numeric(18,4) | 9 |
| PMGallon | numeric(18,4) | 9 |
| PMDrum | numeric(18,4) | 9 |
| PMBarrel | numeric(18,4) | 9 |
| PTHour | numeric(18,4) | 9 |
| PTLoad | numeric(18,4) | 9 |
| PTGallon | numeric(18,4) | 9 |
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
| HTYes | varchar(50) | 50 |
| HTNo | varchar(50) | 50 |
| HTPK | varchar(50) | 50 |
| HTAD | varchar(50) | 50 |
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
| Direction | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| StatusDescription | varchar(2000) | 2000 |
| SpecialBilling | bigint | 8 |
| EffectiveDate | datetime | 8 |
| IndexName | varchar(50) | 50 |
| IDiscountPcnt | numeric(18,3) | 9 |
| IGallon | numeric(18,3) | 9 |
| IBarrel | numeric(18,3) | 9 |
| ContactName | varchar(50) | 50 |
| ContactEmail | varchar(50) | 50 |
| ContactPhone | varchar(50) | 50 |
| ContactFax | varchar(50) | 50 |
| DeepWell | varchar(50) | 50 |
| ReviewedBySales | int | 4 |
| ReviewedByDispatch | int | 4 |
| BillingDepartment | varchar(100) | 100 |
| AirPermitTracking | varchar(3) | 3 |
| MSDSFileName | varchar(600) | 600 |
| MSDSUpdateUser | varchar(50) | 50 |
| MSDSUpdateDateTime | datetime | 8 |
| UOM | varchar(1) | 1 |
| LinkProfileId | bigint | 8 |
| CreateDate | datetime | 8 |
| EPAWasteCode1 | varchar(10) | 10 |
| EPAWasteCode2 | varchar(10) | 10 |
| EPAWasteCode3 | varchar(10) | 10 |
| EPAWasteCode4 | varchar(10) | 10 |
| IndustrialCategory | varchar(20) | 20 |
| GCApprovalDate | datetime | 8 |
| LinkDirection | varchar(10) | 10 |
| NewParkOnly | bit | 1 |
| LandfillOnly | bit | 1 |
| Clordtect | bit | 1 |
| StatusChangeDate | datetime | 8 |
| EstHours | varchar(50) | 50 |
| DOTCorrosive | bit | 1 |
| RiskFactor | int | 4 |
| CSUCommercial | bit | 1 |
| CSUOilBearing | bit | 1 |
| CSUUsedOil | bit | 1 |
| VaporPressure | varchar(50) | 50 |
| VaporPressureOther | varchar(50) | 50 |
| Benzene | varchar(50) | 50 |
| BenzeneOther | varchar(50) | 50 |
| TrailerLastLoadDescription | varchar(1000) | 1000 |
| CreateUser | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| CreateComputer | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| Generator Email | varchar(50) | 50 |
| Customer Email | varchar(50) | 50 |
| Last Load Date | datetime | 8 |
| ServiceType | varchar(50) | 50 |
| CompanyProfileNumber | varchar(100) | 100 |
| CSRPersonId | varchar(50) | 50 |
| WasteClass | varchar(3) | 3 |
| ContractNumber | varchar(20) | 20 |
| Product | varchar(20) | 20 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportProfilesNew]
AS
SELECT        TOP (100) PERCENT dbo.Profile.Id, dbo.Generator.Name AS [Generator Name], dbo.Generator.Address, dbo.Generator.City, dbo.Generator.State, dbo.Generator.Zip, dbo.Generator.RegistrationNo, 
                         dbo.Generator.EpaIdNo, dbo.Customer.Name AS [Customer Name], dbo.Vendor.Name AS [Vendor Name], dbo.Vendor.Mas90Id AS [Vendor No], dbo.Profile.ProfileNumber, 
                         dbo.Transporter.Name AS [Transporter Name], dbo.Profile.WasteCode, dbo.MaterialCode.MaterialCode, dbo.MaterialCode.Description AS [Material Code], dbo.Profile.ProductCategory, 
                         dbo.Profile.MaterialDescription, dbo.Profile.ProcessDescription, dbo.Profile.MaterialClassification, dbo.Profile.StateWasteCode, dbo.Profile.SICCode, dbo.Profile.Volume, dbo.Profile.LoadFrequency, 
                         dbo.Profile.ProfileType, dbo.Profile.SalesPersonId, dbo.Profile.Viscosity, dbo.Profile.PhRange, dbo.Profile.SpecificGravity, dbo.Profile.FlashPoint, dbo.Profile.Phase, dbo.Profile.ViscosityOther, 
                         dbo.Profile.PhRangeOther, dbo.Profile.SpecificGravityOther, dbo.Profile.FlashPointOther, dbo.Profile.PhaseOther, dbo.Profile.OtherComments, dbo.Profile.ShippingName, dbo.Profile.ShippingMethod, 
                         dbo.Profile.SpecialEquipment, dbo.Profile.SpecialInstructions, dbo.Profile.DocumentType, dbo.Destination.Name AS Destination, dbo.Profile.DispatchNotes, dbo.Profile.Approval, dbo.Profile.ApprovalBy, 
                         dbo.Profile.ApprovalDate, dbo.Profile.HazMat, dbo.Profile.Placards, dbo.Profile.PMTote, dbo.Profile.PMGallon, dbo.Profile.PMDrum, dbo.Profile.PMBarrel, dbo.Profile.PTHour, dbo.Profile.PTLoad, 
                         dbo.Profile.PTGallon, dbo.Profile.PTDemurrage, dbo.Profile.PTFreeTime, dbo.Profile.PTFuelSerCharge, dbo.Profile.PTHourMin, dbo.Profile.PTGallonMin, dbo.Profile.PMTestType, dbo.Profile.PMTestBase, 
                         dbo.Profile.PMTestIncrement, dbo.Profile.PMTestTote, dbo.Profile.PMTestGallon, dbo.Profile.PMTestDrum, dbo.Profile.PMTestBarrel, dbo.Profile.PMSolidsTestType, dbo.Profile.PMSolidsBase, 
                         dbo.Profile.PMSolidsIncrement, dbo.Profile.PMSolidsTote, dbo.Profile.PMSolidsGallon, dbo.Profile.PMSolidsDrum, dbo.Profile.PMSolidsBarrel, dbo.Profile.PMMetals, dbo.Profile.PMAmmonia, dbo.Profile.HTYes, 
                         dbo.Profile.HTNo, dbo.Profile.HTPK, dbo.Profile.HTAD, dbo.Profile.MinFlashPoint, dbo.Profile.MaxCentrifugeSolidsPcnt, dbo.Profile.MaxFreePhaseWaterPcnt, dbo.Profile.MaxFreePhaseOrganicPcnt, 
                         dbo.Profile.MaxWaterByHach, dbo.Profile.MaxChlordetect, dbo.Profile.MaxViscosity, dbo.Profile.MaxTotalAcid, dbo.Profile.MinAPIGravity, dbo.Profile.MaxWaterByDistillationPcnt, dbo.Profile.MaxAshWtPcnt, 
                         dbo.Profile.MaxPPMP, dbo.Profile.MaxSulfur, dbo.Profile.Compatibility, dbo.Profile.ProductComments, dbo.Profile.MaxSilicone, dbo.Profile.MaxSodium, dbo.Profile.MaxVanadium, dbo.Profile.MaxAluminum, 
                         dbo.Profile.Direction, dbo.Profile.Status, dbo.Profile.StatusDescription, dbo.Profile.SpecialBilling, dbo.Profile.EffectiveDate, dbo.Profile.IndexName, dbo.Profile.IDiscountPcnt, dbo.Profile.IGallon, 
                         dbo.Profile.IBarrel, dbo.Profile.ContactName, dbo.Profile.ContactEmail, dbo.Profile.ContactPhone, dbo.Profile.ContactFax, dbo.Profile.DeepWell, dbo.Profile.ReviewedBySales, dbo.Profile.ReviewedByDispatch, 
                         dbo.Profile.BillingDepartment, dbo.Profile.AirPermitTracking, dbo.Profile.MSDSFileName, dbo.Profile.MSDSUpdateUser, dbo.Profile.MSDSUpdateDateTime, dbo.Profile.UOM, dbo.Profile.LinkProfileId, 
                         dbo.Profile.CreateDate, dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Profile.IndustrialCategory, dbo.Profile.GCApprovalDate, 
                         dbo.Profile.LinkDirection, dbo.Profile.NewParkOnly, dbo.Profile.LandfillOnly, dbo.Profile.Clordtect, dbo.Profile.StatusChangeDate, dbo.Profile.EstHours, dbo.Profile.DOTCorrosive, dbo.Profile.RiskFactor, 
                         dbo.Profile.CSUCommercial, dbo.Profile.CSUOilBearing, dbo.Profile.CSUUsedOil, dbo.Profile.VaporPressure, dbo.Profile.VaporPressureOther, dbo.Profile.Benzene, dbo.Profile.BenzeneOther, 
                         dbo.Profile.TrailerLastLoadDescription, dbo.Profile.CreateUser, dbo.Profile.CreateDateTime, dbo.Profile.CreateComputer, dbo.Profile.Type, dbo.Profile.UpdateDateTime, dbo.Profile.UpdateUser, 
                         dbo.Profile.UpdateComputer, dbo.Generator.Email AS [Generator Email], dbo.Customer.Email AS [Customer Email], MAX(DISTINCT dbo.Loads.ScheduledDate) AS [Last Load Date], dbo.ServiceTypes.ServiceType, 
                         dbo.Profile.CompanyProfileNumber, dbo.Profile.CSRPersonId, dbo.Profile.WasteClass, dbo.Profile.ContractNumber, dbo.Profile.Product
FROM            dbo.Profile LEFT OUTER JOIN
                         dbo.ServiceTypes ON dbo.Profile.ServiceTypeId = dbo.ServiceTypes.Id LEFT OUTER JOIN
                         dbo.Destination ON dbo.Profile.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.MaterialCode ON dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID LEFT OUTER JOIN
                         dbo.Vendor ON dbo.Profile.VendorId = dbo.Vendor.Id LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Profile.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id LEFT OUTER JOIN
                         dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId
GROUP BY dbo.Profile.Id, dbo.Customer.Name, dbo.Vendor.Name, dbo.Profile.ProfileNumber, dbo.Transporter.Name, dbo.MaterialCode.Description, dbo.Profile.ProductCategory, dbo.Profile.MaterialDescription, 
                         dbo.Profile.ProcessDescription, dbo.Profile.SICCode, dbo.Profile.Volume, dbo.Profile.LoadFrequency, dbo.Profile.ProfileType, dbo.Profile.SalesPersonId, dbo.Profile.Viscosity, dbo.Profile.PhRange, 
                         dbo.Profile.SpecificGravity, dbo.Profile.FlashPoint, dbo.Profile.Phase, dbo.Profile.SpecificGravityOther, dbo.Profile.FlashPointOther, dbo.Profile.PhaseOther, dbo.Profile.OtherComments, dbo.Profile.ShippingName,
                          dbo.Profile.ShippingMethod, dbo.Profile.SpecialEquipment, dbo.Profile.SpecialInstructions, dbo.Profile.DocumentType, dbo.Destination.Name, dbo.Profile.DispatchNotes, dbo.Profile.Approval, 
                         dbo.Profile.ApprovalBy, dbo.Profile.ApprovalDate, dbo.Profile.WasteCode, dbo.MaterialCode.MaterialCode, dbo.Profile.MaterialClassification, dbo.Profile.StateWasteCode, dbo.Profile.ViscosityOther, 
                         dbo.Profile.PhRangeOther, dbo.Profile.HazMat, dbo.Profile.Placards, dbo.Profile.PMTote, dbo.Profile.PMGallon, dbo.Profile.PMDrum, dbo.Profile.PMBarrel, dbo.Profile.PTHour, dbo.Profile.PTLoad, 
                         dbo.Profile.PTGallon, dbo.Profile.PTDemurrage, dbo.Profile.PTFreeTime, dbo.Profile.PTFuelSerCharge, dbo.Profile.PTHourMin, dbo.Profile.PTGallonMin, dbo.Profile.PMTestType, dbo.Profile.PMTestBase, 
                         dbo.Profile.PMTestIncrement, dbo.Profile.PMTestTote, dbo.Profile.PMSolidsTestType, dbo.Profile.PMTestBarrel, dbo.Profile.PMTestDrum, dbo.Profile.PMTestGallon, dbo.Profile.PMSolidsBase, 
                         dbo.Profile.PMSolidsIncrement, dbo.Profile.PMSolidsTote, dbo.Profile.PMSolidsGallon, dbo.Profile.PMSolidsDrum, dbo.Profile.PMSolidsBarrel, dbo.Profile.PMMetals, dbo.Profile.PMAmmonia, dbo.Profile.HTYes, 
                         dbo.Profile.HTNo, dbo.Profile.HTPK, dbo.Profile.HTAD, dbo.Profile.MinFlashPoint, dbo.Profile.MaxCentrifugeSolidsPcnt, dbo.Profile.MaxFreePhaseWaterPcnt, dbo.Profile.MaxFreePhaseOrganicPcnt, 
                         dbo.Profile.MaxWaterByHach, dbo.Profile.MaxChlordetect, dbo.Profile.MaxViscosity, dbo.Profile.MaxTotalAcid, dbo.Profile.MinAPIGravity, dbo.Profile.MaxWaterByDistillationPcnt, dbo.Profile.MaxAshWtPcnt, 
                         dbo.Profile.MaxPPMP, dbo.Profile.MaxSulfur, dbo.Profile.Compatibility, dbo.Profile.ProductComments, dbo.Profile.MaxSilicone, dbo.Profile.MaxSodium, dbo.Profile.MaxVanadium, dbo.Profile.MaxAluminum, 
                         dbo.Profile.Direction, dbo.Profile.Status, dbo.Profile.StatusDescription, dbo.Profile.SpecialBilling, dbo.Profile.EffectiveDate, dbo.Profile.IndexName, dbo.Profile.IDiscountPcnt, dbo.Profile.IGallon, 
                         dbo.Profile.IBarrel, dbo.Profile.ContactName, dbo.Profile.ContactEmail, dbo.Profile.ContactPhone, dbo.Profile.ContactFax, dbo.Profile.DeepWell, dbo.Profile.ReviewedBySales, dbo.Profile.ReviewedByDispatch, 
                         dbo.Profile.BillingDepartment, dbo.Profile.AirPermitTracking, dbo.Profile.MSDSFileName, dbo.Profile.MSDSUpdateUser, dbo.Profile.MSDSUpdateDateTime, dbo.Profile.UOM, dbo.Profile.LinkProfileId, 
                         dbo.Profile.CreateDate, dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Profile.IndustrialCategory, dbo.Profile.GCApprovalDate, 
                         dbo.Profile.LinkDirection, dbo.Profile.NewParkOnly, dbo.Profile.LandfillOnly, dbo.Profile.Clordtect, dbo.Profile.StatusChangeDate, dbo.Profile.EstHours, dbo.Profile.DOTCorrosive, dbo.Profile.RiskFactor, 
                         dbo.Profile.CSUCommercial, dbo.Profile.CSUOilBearing, dbo.Profile.CSUUsedOil, dbo.Profile.VaporPressure, dbo.Profile.VaporPressureOther, dbo.Profile.Benzene, dbo.Profile.BenzeneOther, 
                         dbo.Profile.TrailerLastLoadDescription, dbo.Profile.CreateUser, dbo.Profile.CreateDateTime, dbo.Profile.CreateComputer, dbo.Profile.Type, dbo.Profile.UpdateDateTime, dbo.Profile.UpdateUser, 
                         dbo.Profile.UpdateComputer, dbo.Generator.Email, dbo.Customer.Email, dbo.Generator.Name, dbo.ServiceTypes.ServiceType, dbo.Profile.CompanyProfileNumber, dbo.Profile.CSRPersonId, 
                         dbo.Generator.Address, dbo.Generator.City, dbo.Generator.State, dbo.Generator.Zip, dbo.Profile.WasteClass, dbo.Generator.RegistrationNo, dbo.Generator.EpaIdNo, dbo.Vendor.Mas90Id, 
                         dbo.Profile.ContractNumber, dbo.Profile.Product
ORDER BY dbo.Profile.Id, [Last Load Date] DESC
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ServiceTypes]](../Tables/dbo_ServiceTypes.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

