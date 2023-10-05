#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.MonthlyDischargeReport

# ![Tables](../../../../Images/Table32.png) [dbo].[MonthlyDischargeReport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 3177 |
| Created | 3:00:36 AM Monday, July 23, 2012 |
| Last Modified | 3:11:13 PM Wednesday, October 17, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| Id | bigint | 8 | NOT NULL | 1 - 1 |
| UserName | varchar(50) | 50 | NULL allowed |  |
| CustomerName | varchar(200) | 200 | NULL allowed |  |
| GeneratorName | varchar(200) | 200 | NULL allowed |  |
| ProfileNumber | varchar(200) | 200 | NULL allowed |  |
| SICCode | varchar(200) | 200 | NULL allowed |  |
| EpaIdNo | varchar(200) | 200 | NULL allowed |  |
| StateId | varchar(200) | 200 | NULL allowed |  |
| TransporterName | varchar(200) | 200 | NULL allowed |  |
| TransporterId | varchar(200) | 200 | NULL allowed |  |
| OrganicWaste | varchar(200) | 200 | NULL allowed |  |
| OilyWaste | varchar(200) | 200 | NULL allowed |  |
| OtherWaste | varchar(200) | 200 | NULL allowed |  |
| WasteName | varchar(200) | 200 | NULL allowed |  |
| MaterialDescription | varchar(2000) | 2000 | NULL allowed |  |
| EPAWasteCode | varchar(200) | 200 | NULL allowed |  |
| TCEQWasteCode | varchar(200) | 200 | NULL allowed |  |
| IndustrialCategory | varchar(200) | 200 | NULL allowed |  |
| TreatmentDescription | varchar(200) | 200 | NULL allowed |  |
| GCApprovalDate | datetime | 8 | NULL allowed |  |
| GCApproved | bit | 1 | NULL allowed |  |
| Destination | varchar(200) | 200 | NULL allowed |  |
| Facility | varchar(200) | 200 | NULL allowed |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[MonthlyDischargeReport]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[UserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GeneratorName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileNumber] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SICCode] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EpaIdNo] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[StateId] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransporterName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransporterId] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OrganicWaste] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OilyWaste] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OtherWaste] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WasteName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialDescription] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EPAWasteCode] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TCEQWasteCode] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[IndustrialCategory] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TreatmentDescription] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GCApprovalDate] [datetime] NULL,
[GCApproved] [bit] NULL,
[Destination] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Facility] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptMonthlyDischarge]](../Views/dbo_vwRptMonthlyDischarge.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

