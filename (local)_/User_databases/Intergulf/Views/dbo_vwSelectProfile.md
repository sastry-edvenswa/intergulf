#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfile

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfile]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:46:56 PM Wednesday, November 15, 2017 |
| Last Modified | 7:46:56 PM Wednesday, November 15, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| CustomerId | bigint | 8 |
| VendorId | bigint | 8 |
| GeneratorId | bigint | 8 |
| ProfileNumber | varchar(50) | 50 |
| TransporterId | bigint | 8 |
| LabTestSampleId | bigint | 8 |
| WasteCode | varchar(50) | 50 |
| MaterialCodeId | int | 4 |
| ProductCategory | varchar(50) | 50 |
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
| DispatchNotes | varchar(6000) | 6000 |
| DocumentType | varchar(50) | 50 |
| Approval | varchar(50) | 50 |
| ApprovalBy | varchar(50) | 50 |
| ApprovalDate | datetime | 8 |
| HazMat | varchar(50) | 50 |
| Placards | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
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
| Notes | varchar(5000) | 5000 |
| SalesPersonId | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| StatusDescription | varchar(2000) | 2000 |
| SpecialBilling | bigint | 8 |
| OldProfileId | varchar(50) | 50 |
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
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| AirPermitTracking | varchar(3) | 3 |
| MSDSFileName | varchar(600) | 600 |
| MSDSUpdateUser | varchar(50) | 50 |
| MSDSUpdateComputer | varchar(50) | 50 |
| MSDSUpdateDateTime | datetime | 8 |
| UOM | varchar(1) | 1 |
| LinkProfileId | bigint | 8 |
| DestinationId | bigint | 8 |
| InactiveReviewed | bit | 1 |
| InactiveExclude | bit | 1 |
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
| CreateUser | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| CreateComputer | varchar(50) | 50 |
| CSUCommercial | bit | 1 |
| CSUOilBearing | bit | 1 |
| CSUUsedOil | bit | 1 |
| VaporPressure | varchar(50) | 50 |
| VaporPressureOther | varchar(50) | 50 |
| Benzene | varchar(50) | 50 |
| BenzeneOther | varchar(50) | 50 |
| TrailerLastLoadDescription | varchar(1000) | 1000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfile]
AS
SELECT        Id, CustomerId, VendorId, GeneratorId, ProfileNumber, TransporterId, LabTestSampleId, WasteCode, MaterialCodeId, ProductCategory, MaterialDescription, 
                         ProcessDescription, MaterialClassification, StateWasteCode, SICCode, Volume, LoadFrequency, Viscosity, PhRange, SpecificGravity, FlashPoint, Phase, 
                         ViscosityOther, PhRangeOther, SpecificGravityOther, FlashPointOther, PhaseOther, OtherComments, ShippingName, ShippingMethod, SpecialEquipment, 
                         SpecialInstructions, DispatchNotes, DocumentType, Approval, ApprovalBy, ApprovalDate, HazMat, Placards, ProfileType, PMTote, PMGallon, PMDrum, PMBarrel, 
                         PTHour, PTLoad, PTGallon, PTDemurrage, PTFreeTime, PTFuelSerCharge, PTHourMin, PTGallonMin, PMTestType, PMTestBase, PMTestIncrement, PMTestTote, 
                         PMTestGallon, PMTestDrum, PMTestBarrel, PMSolidsTestType, PMSolidsBase, PMSolidsIncrement, PMSolidsTote, PMSolidsGallon, PMSolidsDrum, 
                         PMSolidsBarrel, PMMetals, PMAmmonia, HTYes, HTNo, HTPK, HTAD, MinFlashPoint, MaxCentrifugeSolidsPcnt, MaxFreePhaseWaterPcnt, 
                         MaxFreePhaseOrganicPcnt, MaxWaterByHach, MaxChlordetect, MaxViscosity, MaxTotalAcid, MinAPIGravity, MaxWaterByDistillationPcnt, MaxAshWtPcnt, 
                         MaxPPMP, MaxSulfur, Compatibility, ProductComments, MaxSilicone, MaxSodium, MaxVanadium, MaxAluminum, Notes, SalesPersonId, Direction, Type, Status, 
                         StatusDescription, SpecialBilling, OldProfileId, EffectiveDate, IndexName, IDiscountPcnt, IGallon, IBarrel, ContactName, ContactEmail, ContactPhone, ContactFax, 
                         DeepWell, ReviewedBySales, ReviewedByDispatch, BillingDepartment, UpdateDateTime, UpdateUser, UpdateComputer, AirPermitTracking, MSDSFileName, 
                         MSDSUpdateUser, MSDSUpdateComputer, MSDSUpdateDateTime, UOM, LinkProfileId, DestinationId, InactiveReviewed, InactiveExclude, CreateDate, 
                         EPAWasteCode1, EPAWasteCode2, EPAWasteCode3, EPAWasteCode4, IndustrialCategory, GCApprovalDate, LinkDirection, NewParkOnly, LandfillOnly, Clordtect, 
                         StatusChangeDate, EstHours, DOTCorrosive, RiskFactor, CreateUser, CreateDateTime, CreateComputer, CSUCommercial, CSUOilBearing, CSUUsedOil, 
                         VaporPressure, VaporPressureOther, Benzene, BenzeneOther, TrailerLastLoadDescription
FROM            dbo.fnSelectProfile() AS fnSelectProfile

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

