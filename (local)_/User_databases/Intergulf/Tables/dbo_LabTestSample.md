#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LabTestSample

# ![Tables](../../../../Images/Table32.png) [dbo].[LabTestSample]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 11620 |
| Created | 4:46:35 PM Thursday, April 19, 2007 |
| Last Modified | 11:50:40 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LabTestSample: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | EntryDate | datetime | 8 | NULL allowed |  |
|  | DueDate | datetime | 8 | NULL allowed |  |
|  | Customer | varchar(4000) | 4000 | NULL allowed |  |
|  | Facility | varchar(4000) | 4000 | NULL allowed |  |
|  | MaterialDescription | varchar(4000) | 4000 | NULL allowed |  |
|  | FlashPoint | int | 4 | NULL allowed |  |
|  | CentrifugeSolidsPcnt | int | 4 | NULL allowed |  |
|  | FreePhaseWaterPcnt | int | 4 | NULL allowed |  |
|  | FreePhaseOrganicPcnt | int | 4 | NULL allowed |  |
|  | WaterByHach | int | 4 | NULL allowed |  |
|  | Zinc | int | 4 | NULL allowed |  |
|  | TotalSuspendedSolids | int | 4 | NULL allowed |  |
|  | Chlordtect | int | 4 | NULL allowed |  |
|  | TotalAcid | int | 4 | NULL allowed |  |
|  | APIGravity | int | 4 | NULL allowed |  |
|  | Compatibility | int | 4 | NULL allowed |  |
|  | Viscosity | int | 4 | NULL allowed |  |
|  | PH | int | 4 | NULL allowed |  |
|  | WaterDistillationPcnt | int | 4 | NULL allowed |  |
|  | Copper | int | 4 | NULL allowed |  |
|  | COD | int | 4 | NULL allowed |  |
|  | AshWtPcnt | int | 4 | NULL allowed |  |
|  | PpMp | int | 4 | NULL allowed |  |
|  | AACr | int | 4 | NULL allowed |  |
|  | AAPb | int | 4 | NULL allowed |  |
|  | AAAg | int | 4 | NULL allowed |  |
|  | AACo | int | 4 | NULL allowed |  |
|  | AASn | int | 4 | NULL allowed |  |
|  | AACu | int | 4 | NULL allowed |  |
|  | AANi | int | 4 | NULL allowed |  |
|  | AAZn | int | 4 | NULL allowed |  |
|  | AAFe | int | 4 | NULL allowed |  |
|  | Comments | varchar(4000) | 4000 | NULL allowed |  |
|  | OutsideLabTesting | varchar(500) | 500 | NULL allowed |  |
|  | PreFlashPointValue | varchar(5) | 5 | NULL allowed |  |
|  | FlashPointValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreCentrifugeSolidsPcntValue | varchar(5) | 5 | NULL allowed |  |
|  | CentrifugeSolidsPcntValue | decimal(18,1) | 9 | NULL allowed |  |
|  | PreFreePhaseWaterPcntValue | varchar(5) | 5 | NULL allowed |  |
|  | FreePhaseWaterPcntValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreFreePhaseOrganicPcntValue | varchar(5) | 5 | NULL allowed |  |
|  | FreePhaseOrganicPcntValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreWaterByHachValue | varchar(5) | 5 | NULL allowed |  |
|  | WaterByHachValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreZincValue | varchar(5) | 5 | NULL allowed |  |
|  | ZincValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreTotalSuspendedSolidsValue | varchar(5) | 5 | NULL allowed |  |
|  | TotalSuspendedSolidsValue | decimal(18,3) | 9 | NULL allowed |  |
|  | PreChlordtectValue | varchar(5) | 5 | NULL allowed |  |
|  | ChlordtectValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreTotalAcidValue | varchar(5) | 5 | NULL allowed |  |
|  | TotalAcidValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreAPIGravityValue | varchar(5) | 5 | NULL allowed |  |
|  | APIGravityValue | decimal(18,1) | 9 | NULL allowed |  |
|  | CompatibilityValue | varchar(2000) | 2000 | NULL allowed |  |
|  | ViscosityValue | varchar(2000) | 2000 | NULL allowed |  |
|  | PrePHValue | varchar(5) | 5 | NULL allowed |  |
|  | PHValue | decimal(18,1) | 9 | NULL allowed |  |
|  | PreWaterDistillationPcntValue | varchar(5) | 5 | NULL allowed |  |
|  | WaterDistillationPcntValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreCopperValue | varchar(5) | 5 | NULL allowed |  |
|  | CopperValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreCODValue | varchar(5) | 5 | NULL allowed |  |
|  | CODValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreAshWtPcntValue | varchar(5) | 5 | NULL allowed |  |
|  | AshWtPcntValue | decimal(18,2) | 9 | NULL allowed |  |
|  | PrePpMpValue | varchar(5) | 5 | NULL allowed |  |
|  | PpMpValue | decimal(18,0) | 9 | NULL allowed |  |
|  | TRComments | varchar(4000) | 4000 | NULL allowed |  |
|  | AACrValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AAPbValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AAAgValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AACoValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AASnValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AACuValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AANiValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AAZnValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AAFeValue | decimal(18,3) | 9 | NULL allowed |  |
|  | AAComments | varchar(4000) | 4000 | NULL allowed |  |
|  | Approved | varchar(10) | 10 | NULL allowed |  |
|  | ApprovedBy | varchar(50) | 50 | NULL allowed |  |
|  | Status | varchar(50) | 50 | NULL allowed |  |
|  | LabTechId | varchar(50) | 50 | NULL allowed |  |
|  | SalesPersonId | varchar(50) | 50 | NULL allowed |  |
|  | ApprovalStatus | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | EmailSent | varchar(10) | 10 | NULL allowed |  |
|  | TOC | int | 4 | NULL allowed |  |
|  | Sulfer | int | 4 | NULL allowed |  |
|  | H2S | int | 4 | NULL allowed |  |
|  | OrganicChlorides | int | 4 | NULL allowed |  |
|  | Ammonia | int | 4 | NULL allowed |  |
|  | PreTOCValue | varchar(5) | 5 | NULL allowed |  |
|  | TOCValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreSulferValue | varchar(5) | 5 | NULL allowed |  |
|  | SulferValue | decimal(18,5) | 9 | NULL allowed |  |
|  | PreH2SValue | varchar(5) | 5 | NULL allowed |  |
|  | H2SValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreOrganicChloridesValue | varchar(5) | 5 | NULL allowed |  |
|  | OrganicChloridesValue | decimal(18,0) | 9 | NULL allowed |  |
|  | PreAmmoniaValue | varchar(5) | 5 | NULL allowed |  |
|  | AmmoniaValue | decimal(18,0) | 9 | NULL allowed |  |
|  | FileName | varchar(500) | 500 | NULL allowed |  |
|  | PreViscosityValueNew | varchar(5) | 5 | NULL allowed |  |
|  | ViscosityValueNew | decimal(18,3) | 9 | NULL allowed |  |
|  | PrePCBValue | varchar(5) | 5 | NULL allowed |  |
|  | PCBValue | decimal(18,2) | 9 | NULL allowed |  |
|  | PCB | int | 4 | NULL allowed |  |
|  | InitialViscosity | decimal(18,3) | 9 | NULL allowed |  |
|  | FinalViscosity | decimal(18,3) | 9 | NULL allowed |  |
|  | OilStressTestComments | varchar(2000) | 2000 | NULL allowed |  |
|  | OilStressTest | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LabTestSample: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LabTestSample | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LabTestSample]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[EntryDate] [datetime] NULL,
[DueDate] [datetime] NULL,
[Customer] [varchar] (4000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Facility] [varchar] (4000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialDescription] [varchar] (4000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FlashPoint] [int] NULL,
[CentrifugeSolidsPcnt] [int] NULL,
[FreePhaseWaterPcnt] [int] NULL,
[FreePhaseOrganicPcnt] [int] NULL,
[WaterByHach] [int] NULL,
[Zinc] [int] NULL,
[TotalSuspendedSolids] [int] NULL,
[Chlordtect] [int] NULL,
[TotalAcid] [int] NULL,
[APIGravity] [int] NULL,
[Compatibility] [int] NULL,
[Viscosity] [int] NULL,
[PH] [int] NULL,
[WaterDistillationPcnt] [int] NULL,
[Copper] [int] NULL,
[COD] [int] NULL,
[AshWtPcnt] [int] NULL,
[PpMp] [int] NULL,
[AACr] [int] NULL,
[AAPb] [int] NULL,
[AAAg] [int] NULL,
[AACo] [int] NULL,
[AASn] [int] NULL,
[AACu] [int] NULL,
[AANi] [int] NULL,
[AAZn] [int] NULL,
[AAFe] [int] NULL,
[Comments] [varchar] (4000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OutsideLabTesting] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PreFlashPointValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FlashPointValue] [decimal] (18, 0) NULL,
[PreCentrifugeSolidsPcntValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CentrifugeSolidsPcntValue] [decimal] (18, 1) NULL,
[PreFreePhaseWaterPcntValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FreePhaseWaterPcntValue] [decimal] (18, 0) NULL,
[PreFreePhaseOrganicPcntValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FreePhaseOrganicPcntValue] [decimal] (18, 0) NULL,
[PreWaterByHachValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WaterByHachValue] [decimal] (18, 0) NULL,
[PreZincValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ZincValue] [decimal] (18, 0) NULL,
[PreTotalSuspendedSolidsValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TotalSuspendedSolidsValue] [decimal] (18, 3) NULL,
[PreChlordtectValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ChlordtectValue] [decimal] (18, 0) NULL,
[PreTotalAcidValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TotalAcidValue] [decimal] (18, 0) NULL,
[PreAPIGravityValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[APIGravityValue] [decimal] (18, 1) NULL,
[CompatibilityValue] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ViscosityValue] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PrePHValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PHValue] [decimal] (18, 1) NULL,
[PreWaterDistillationPcntValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WaterDistillationPcntValue] [decimal] (18, 0) NULL,
[PreCopperValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CopperValue] [decimal] (18, 0) NULL,
[PreCODValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CODValue] [decimal] (18, 0) NULL,
[PreAshWtPcntValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AshWtPcntValue] [decimal] (18, 2) NULL,
[PrePpMpValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PpMpValue] [decimal] (18, 0) NULL,
[TRComments] [varchar] (4000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AACrValue] [decimal] (18, 3) NULL,
[AAPbValue] [decimal] (18, 3) NULL,
[AAAgValue] [decimal] (18, 3) NULL,
[AACoValue] [decimal] (18, 3) NULL,
[AASnValue] [decimal] (18, 3) NULL,
[AACuValue] [decimal] (18, 3) NULL,
[AANiValue] [decimal] (18, 3) NULL,
[AAZnValue] [decimal] (18, 3) NULL,
[AAFeValue] [decimal] (18, 3) NULL,
[AAComments] [varchar] (4000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Approved] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ApprovedBy] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LabTechId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ApprovalStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EmailSent] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TOC] [int] NULL,
[Sulfer] [int] NULL,
[H2S] [int] NULL,
[OrganicChlorides] [int] NULL,
[Ammonia] [int] NULL,
[PreTOCValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TOCValue] [decimal] (18, 0) NULL,
[PreSulferValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SulferValue] [decimal] (18, 5) NULL,
[PreH2SValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[H2SValue] [decimal] (18, 0) NULL,
[PreOrganicChloridesValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OrganicChloridesValue] [decimal] (18, 0) NULL,
[PreAmmoniaValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AmmoniaValue] [decimal] (18, 0) NULL,
[FileName] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PreViscosityValueNew] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ViscosityValueNew] [decimal] (18, 3) NULL,
[PrePCBValue] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PCBValue] [decimal] (18, 2) NULL,
[PCB] [int] NULL,
[InitialViscosity] [decimal] (18, 3) NULL,
[FinalViscosity] [decimal] (18, 3) NULL,
[OilStressTestComments] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OilStressTest] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LabTestSample] ADD CONSTRAINT [PK_LabTestSample] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLabTestSampleForm]](../Views/dbo_vwRptLabTestSampleForm.md)
* [[dbo].[vwSelectProspectLabTestSample]](../Views/dbo_vwSelectProspectLabTestSample.md)
* [[dbo].[fnSelectLabTestSample]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTestSample.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

