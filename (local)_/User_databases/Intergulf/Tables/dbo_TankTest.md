#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.TankTest

# ![Tables](../../../../Images/Table32.png) [dbo].[TankTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 211 |
| Created | 9:53:22 PM Tuesday, September 4, 2007 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TankTest: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | Tank | varchar(50) | 50 | NULL allowed |  |
|  | Turn | varchar(50) | 50 | NULL allowed |  |
|  | Location | varchar(50) | 50 | NULL allowed |  |
|  | LabTechId | varchar(50) | 50 | NULL allowed |  |
|  | TestDate | datetime | 8 | NULL allowed |  |
|  | PreFlashPoint | varchar(1) | 1 | NULL allowed |  |
|  | FlashPoint | numeric(18,3) | 9 | NULL allowed |  |
|  | PreAPI | varchar(1) | 1 | NULL allowed |  |
|  | API | numeric(18,3) | 9 | NULL allowed |  |
|  | PreAPITemp | varchar(1) | 1 | NULL allowed |  |
|  | APITemp | numeric(18,0) | 9 | NULL allowed |  |
|  | PreAdjAPI | varchar(1) | 1 | NULL allowed |  |
|  | AdjAPI | numeric(18,3) | 9 | NULL allowed |  |
|  | PrePcntWater | varchar(1) | 1 | NULL allowed |  |
|  | PcntWater | numeric(18,3) | 9 | NULL allowed |  |
|  | PrePcntAsh | varchar(1) | 1 | NULL allowed |  |
|  | PcntAsh | numeric(18,3) | 9 | NULL allowed |  |
|  | PreChlordetect | varchar(1) | 1 | NULL allowed |  |
|  | Chlordetect | numeric(18,3) | 9 | NULL allowed |  |
|  | PreViscosity | varchar(1) | 1 | NULL allowed |  |
|  | Viscosity | numeric(18,3) | 9 | NULL allowed |  |
|  | PreSilicon | varchar(1) | 1 | NULL allowed |  |
|  | Silicon | numeric(18,3) | 9 | NULL allowed |  |
|  | PreSulfur | varchar(1) | 1 | NULL allowed |  |
|  | Sulfur | numeric(18,3) | 9 | NULL allowed |  |
|  | PreSodium | varchar(1) | 1 | NULL allowed |  |
|  | Sodium | numeric(18,3) | 9 | NULL allowed |  |
|  | PreAluminum | varchar(1) | 1 | NULL allowed |  |
|  | Aluminum | numeric(18,3) | 9 | NULL allowed |  |
|  | PreVanadium | varchar(1) | 1 | NULL allowed |  |
|  | Vanadium | numeric(18,3) | 9 | NULL allowed |  |
|  | TankLevel | varchar(50) | 50 | NULL allowed |  |
|  | Comments | varchar(3000) | 3000 | NULL allowed |  |
|  | ApprovedById | varchar(50) | 50 | NULL allowed |  |
|  | Status | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TankTest: Id](../../../../Images/pkcluster.png)](#indexes) | PK_TankTest | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[TankTest]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[Tank] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Turn] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Location] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LabTechId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TestDate] [datetime] NULL,
[PreFlashPoint] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FlashPoint] [numeric] (18, 3) NULL,
[PreAPI] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[API] [numeric] (18, 3) NULL,
[PreAPITemp] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[APITemp] [numeric] (18, 0) NULL,
[PreAdjAPI] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AdjAPI] [numeric] (18, 3) NULL,
[PrePcntWater] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PcntWater] [numeric] (18, 3) NULL,
[PrePcntAsh] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PcntAsh] [numeric] (18, 3) NULL,
[PreChlordetect] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Chlordetect] [numeric] (18, 3) NULL,
[PreViscosity] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Viscosity] [numeric] (18, 3) NULL,
[PreSilicon] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Silicon] [numeric] (18, 3) NULL,
[PreSulfur] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Sulfur] [numeric] (18, 3) NULL,
[PreSodium] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Sodium] [numeric] (18, 3) NULL,
[PreAluminum] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Aluminum] [numeric] (18, 3) NULL,
[PreVanadium] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Vanadium] [numeric] (18, 3) NULL,
[TankLevel] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Comments] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ApprovedById] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[TankTest] ADD CONSTRAINT [PK_TankTest] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptTankTurnLabTest]](../Views/dbo_vwRptTankTurnLabTest.md)
* [[dbo].[fnSelectTankTurnLabTests]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectTankTurnLabTests.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

