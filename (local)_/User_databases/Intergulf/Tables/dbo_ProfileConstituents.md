#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileConstituents

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileConstituents]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 12864 |
| Created | 6:47:35 PM Monday, January 29, 2007 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileConstituents: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | GeneratorId | numeric(18,0) | 9 | NULL allowed |  |
|  | ProfileId | numeric(18,0) | 9 | NULL allowed |  |
|  | PetroleumPcnt | varchar(50) | 50 | NULL allowed |  |
|  | PetroleumPhase | varchar(300) | 300 | NULL allowed |  |
|  | AqueousPcnt | varchar(50) | 50 | NULL allowed |  |
|  | AqueousPhase | varchar(300) | 300 | NULL allowed |  |
|  | SolidsPcnt | varchar(50) | 50 | NULL allowed |  |
|  | SolidsPhase | varchar(300) | 300 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileConstituents: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileConstituents | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileConstituents]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[GeneratorId] [numeric] (18, 0) NULL,
[ProfileId] [numeric] (18, 0) NULL,
[PetroleumPcnt] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumPhase] [varchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousPcnt] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousPhase] [varchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SolidsPcnt] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SolidsPhase] [varchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileConstituents] ADD CONSTRAINT [PK_ProfileConstituents] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptProfileFormConstituents]](../Views/dbo_vwRptProfileFormConstituents.md)
* [[dbo].[vwSelectExportProfileVolume]](../Views/dbo_vwSelectExportProfileVolume.md)
* [[dbo].[vwSelectProfileVolumeTest]](../Views/dbo_vwSelectProfileVolumeTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

