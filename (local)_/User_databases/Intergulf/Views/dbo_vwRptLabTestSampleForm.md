#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLabTestSampleForm

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLabTestSampleForm]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:13:07 PM Sunday, February 8, 2015 |
| Last Modified | 10:13:07 PM Sunday, February 8, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| EntryDate | datetime | 8 |  |
| DueDate | datetime | 8 |  |
| Customer | varchar(4000) | 4000 |  |
| Facility | varchar(4000) | 4000 |  |
| MaterialDescription | varchar(4000) | 4000 |  |
| FlashPoint | int | 4 |  |
| CentrifugeSolidsPcnt | int | 4 |  |
| FreePhaseWaterPcnt | int | 4 |  |
| FreePhaseOrganicPcnt | int | 4 |  |
| WaterByHach | int | 4 |  |
| Zinc | int | 4 |  |
| TotalSuspendedSolids | int | 4 |  |
| Chlordtect | int | 4 |  |
| TotalAcid | int | 4 |  |
| APIGravity | int | 4 |  |
| Compatibility | int | 4 |  |
| Viscosity | int | 4 |  |
| PH | int | 4 |  |
| WaterDistillationPcnt | int | 4 |  |
| Copper | int | 4 |  |
| COD | int | 4 |  |
| AshWtPcnt | int | 4 |  |
| PpMp | int | 4 |  |
| AACr | int | 4 |  |
| AAPb | int | 4 |  |
| AAAg | int | 4 |  |
| AACo | int | 4 |  |
| AASn | int | 4 |  |
| AACu | int | 4 |  |
| AANi | int | 4 |  |
| AAZn | int | 4 |  |
| AAFe | int | 4 |  |
| Comments | varchar(4000) | 4000 |  |
| OutsideLabTesting | varchar(500) | 500 |  |
| PreFlashPointValue | varchar(5) | 5 |  |
| FlashPointValue | decimal(18,0) | 9 |  |
| PreCentrifugeSolidsPcntValue | varchar(5) | 5 |  |
| CentrifugeSolidsPcntValue | decimal(18,1) | 9 |  |
| PreFreePhaseWaterPcntValue | varchar(5) | 5 |  |
| FreePhaseWaterPcntValue | decimal(18,0) | 9 |  |
| PreFreePhaseOrganicPcntValue | varchar(5) | 5 |  |
| FreePhaseOrganicPcntValue | decimal(18,0) | 9 |  |
| PreWaterByHachValue | varchar(5) | 5 |  |
| WaterByHachValue | decimal(18,0) | 9 |  |
| PreZincValue | varchar(5) | 5 |  |
| ZincValue | decimal(18,0) | 9 |  |
| PreTotalSuspendedSolidsValue | varchar(5) | 5 |  |
| TotalSuspendedSolidsValue | decimal(18,3) | 9 |  |
| PreChlordtectValue | varchar(5) | 5 |  |
| ChlordtectValue | decimal(18,0) | 9 |  |
| PreTotalAcidValue | varchar(5) | 5 |  |
| TotalAcidValue | decimal(18,0) | 9 |  |
| PreAPIGravityValue | varchar(5) | 5 |  |
| APIGravityValue | decimal(18,1) | 9 |  |
| CompatibilityValue | varchar(2000) | 2000 |  |
| ViscosityValue | varchar(2000) | 2000 |  |
| PrePHValue | varchar(5) | 5 |  |
| PHValue | decimal(18,1) | 9 |  |
| PreWaterDistillationPcntValue | varchar(5) | 5 |  |
| WaterDistillationPcntValue | decimal(18,0) | 9 |  |
| PreCopperValue | varchar(5) | 5 |  |
| CopperValue | decimal(18,0) | 9 |  |
| PreCODValue | varchar(5) | 5 |  |
| CODValue | decimal(18,0) | 9 |  |
| PreAshWtPcntValue | varchar(5) | 5 |  |
| AshWtPcntValue | decimal(18,2) | 9 |  |
| PrePpMpValue | varchar(5) | 5 |  |
| PpMpValue | decimal(18,0) | 9 |  |
| TRComments | varchar(4000) | 4000 |  |
| AACrValue | decimal(18,3) | 9 |  |
| AAPbValue | decimal(18,3) | 9 |  |
| AAAgValue | decimal(18,3) | 9 |  |
| AACoValue | decimal(18,3) | 9 |  |
| AASnValue | decimal(18,3) | 9 |  |
| AACuValue | decimal(18,3) | 9 |  |
| AANiValue | decimal(18,3) | 9 |  |
| AAZnValue | decimal(18,3) | 9 |  |
| AAFeValue | decimal(18,3) | 9 |  |
| AAComments | varchar(4000) | 4000 |  |
| Approved | varchar(10) | 10 |  |
| ApprovedBy | varchar(50) | 50 |  |
| Status | varchar(50) | 50 |  |
| ApprovalStatus | varchar(50) | 50 |  |
| Lab First Name | varchar(50) | 50 |  |
| Lab Last Name | varchar(50) | 50 |  |
| Salesperson First Name | varchar(50) | 50 |  |
| Salesperson Last Name | varchar(50) | 50 |  |
| TOC | int | 4 |  |
| Sulfer | int | 4 |  |
| H2S | int | 4 |  |
| OrganicChlorides | int | 4 |  |
| Ammonia | int | 4 |  |
| PreTOCValue | varchar(5) | 5 |  |
| TOCValue | decimal(18,0) | 9 |  |
| PreSulferValue | varchar(5) | 5 |  |
| SulferValue | decimal(18,5) | 9 |  |
| PreH2SValue | varchar(5) | 5 |  |
| H2SValue | decimal(18,0) | 9 |  |
| PreOrganicChloridesValue | varchar(5) | 5 |  |
| OrganicChloridesValue | decimal(18,0) | 9 |  |
| PreAmmoniaValue | varchar(5) | 5 |  |
| AmmoniaValue | decimal(18,0) | 9 |  |
| PreViscosityValueNew | varchar(5) | 5 |  |
| ViscosityValueNew | decimal(18,3) | 9 |  |
| PrePCBValue | varchar(5) | 5 |  |
| PCBValue | decimal(18,2) | 9 |  |
| InitialViscosity | decimal(18,3) | 9 |  |
| FinalViscosity | decimal(18,3) | 9 |  |
| OilStressTestComments | varchar(2000) | 2000 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLabTestSampleForm]
AS
SELECT     dbo.LabTestSample.Id, dbo.LabTestSample.EntryDate, dbo.LabTestSample.DueDate, dbo.LabTestSample.Customer, dbo.LabTestSample.Facility, 
                      dbo.LabTestSample.MaterialDescription, dbo.LabTestSample.FlashPoint, dbo.LabTestSample.CentrifugeSolidsPcnt, dbo.LabTestSample.FreePhaseWaterPcnt, 
                      dbo.LabTestSample.FreePhaseOrganicPcnt, dbo.LabTestSample.WaterByHach, dbo.LabTestSample.Zinc, dbo.LabTestSample.TotalSuspendedSolids, 
                      dbo.LabTestSample.Chlordtect, dbo.LabTestSample.TotalAcid, dbo.LabTestSample.APIGravity, dbo.LabTestSample.Compatibility, dbo.LabTestSample.Viscosity, 
                      dbo.LabTestSample.PH, dbo.LabTestSample.WaterDistillationPcnt, dbo.LabTestSample.Copper, dbo.LabTestSample.COD, dbo.LabTestSample.AshWtPcnt, 
                      dbo.LabTestSample.PpMp, dbo.LabTestSample.AACr, dbo.LabTestSample.AAPb, dbo.LabTestSample.AAAg, dbo.LabTestSample.AACo, dbo.LabTestSample.AASn, 
                      dbo.LabTestSample.AACu, dbo.LabTestSample.AANi, dbo.LabTestSample.AAZn, dbo.LabTestSample.AAFe, dbo.LabTestSample.Comments, 
                      dbo.LabTestSample.OutsideLabTesting, dbo.LabTestSample.PreFlashPointValue, dbo.LabTestSample.FlashPointValue, 
                      dbo.LabTestSample.PreCentrifugeSolidsPcntValue, dbo.LabTestSample.CentrifugeSolidsPcntValue, dbo.LabTestSample.PreFreePhaseWaterPcntValue, 
                      dbo.LabTestSample.FreePhaseWaterPcntValue, dbo.LabTestSample.PreFreePhaseOrganicPcntValue, dbo.LabTestSample.FreePhaseOrganicPcntValue, 
                      dbo.LabTestSample.PreWaterByHachValue, dbo.LabTestSample.WaterByHachValue, dbo.LabTestSample.PreZincValue, dbo.LabTestSample.ZincValue, 
                      dbo.LabTestSample.PreTotalSuspendedSolidsValue, dbo.LabTestSample.TotalSuspendedSolidsValue, dbo.LabTestSample.PreChlordtectValue, 
                      dbo.LabTestSample.ChlordtectValue, dbo.LabTestSample.PreTotalAcidValue, dbo.LabTestSample.TotalAcidValue, dbo.LabTestSample.PreAPIGravityValue, 
                      dbo.LabTestSample.APIGravityValue, dbo.LabTestSample.CompatibilityValue, dbo.LabTestSample.ViscosityValue, dbo.LabTestSample.PrePHValue, 
                      dbo.LabTestSample.PHValue, dbo.LabTestSample.PreWaterDistillationPcntValue, dbo.LabTestSample.WaterDistillationPcntValue, 
                      dbo.LabTestSample.PreCopperValue, dbo.LabTestSample.CopperValue, dbo.LabTestSample.PreCODValue, dbo.LabTestSample.CODValue, 
                      dbo.LabTestSample.PreAshWtPcntValue, dbo.LabTestSample.AshWtPcntValue, dbo.LabTestSample.PrePpMpValue, dbo.LabTestSample.PpMpValue, 
                      dbo.LabTestSample.TRComments, dbo.LabTestSample.AACrValue, dbo.LabTestSample.AAPbValue, dbo.LabTestSample.AAAgValue, dbo.LabTestSample.AACoValue, 
                      dbo.LabTestSample.AASnValue, dbo.LabTestSample.AACuValue, dbo.LabTestSample.AANiValue, dbo.LabTestSample.AAZnValue, dbo.LabTestSample.AAFeValue, 
                      dbo.LabTestSample.AAComments, dbo.LabTestSample.Approved, dbo.LabTestSample.ApprovedBy, dbo.LabTestSample.Status, dbo.LabTestSample.ApprovalStatus, 
                      UserMaster_1.FirstName AS [Lab First Name], UserMaster_1.LastName AS [Lab Last Name], UserMaster_2.FirstName AS [Salesperson First Name], 
                      UserMaster_2.LastName AS [Salesperson Last Name], dbo.LabTestSample.TOC, dbo.LabTestSample.Sulfer, dbo.LabTestSample.H2S, 
                      dbo.LabTestSample.OrganicChlorides, dbo.LabTestSample.Ammonia, dbo.LabTestSample.PreTOCValue, dbo.LabTestSample.TOCValue, 
                      dbo.LabTestSample.PreSulferValue, dbo.LabTestSample.SulferValue, dbo.LabTestSample.PreH2SValue, dbo.LabTestSample.H2SValue, 
                      dbo.LabTestSample.PreOrganicChloridesValue, dbo.LabTestSample.OrganicChloridesValue, dbo.LabTestSample.PreAmmoniaValue, 
                      dbo.LabTestSample.AmmoniaValue, dbo.LabTestSample.PreViscosityValueNew, dbo.LabTestSample.ViscosityValueNew, dbo.LabTestSample.PrePCBValue, 
                      dbo.LabTestSample.PCBValue, dbo.LabTestSample.InitialViscosity, dbo.LabTestSample.FinalViscosity, dbo.LabTestSample.OilStressTestComments
FROM         dbo.LabTestSample LEFT OUTER JOIN
                      dbo.UserMaster AS UserMaster_2 ON dbo.LabTestSample.SalesPersonId = UserMaster_2.UserName LEFT OUTER JOIN
                      dbo.UserMaster AS UserMaster_1 ON dbo.LabTestSample.LabTechId = UserMaster_1.UserName

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTestSample]](../Tables/dbo_LabTestSample.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

