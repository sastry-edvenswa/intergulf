#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Equipment

# ![Tables](../../../../Images/Table32.png) [dbo].[Equipment]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 510 |
| Created | 12:17:30 PM Monday, March 19, 2007 |
| Last Modified | 2:48:41 PM Tuesday, June 4, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Equipment: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_stat_2034106287_2_1, _dta_stat_2034106287_6_1_3_4, _dta_stat_2034106287_1_3_4](../../../../Images/Index.png)](#indexes)(3) | Id | varchar(50) | 50 | NOT NULL |
| [![Indexes _dta_stat_2034106287_2_1, _dta_stat_2034106287_2_3, _dta_stat_2034106287_4_3_2](../../../../Images/Index.png)](#indexes)(3) | Description | varchar(50) | 50 | NULL allowed |
| [![Indexes _dta_stat_2034106287_2_3, _dta_stat_2034106287_6_1_3_4, _dta_stat_2034106287_1_3_4, _dta_stat_2034106287_4_3_2, _dta_stat_2034106287_4_3_6](../../../../Images/Index.png)](#indexes)(5) | Type | varchar(50) | 50 | NULL allowed |
| [![Indexes _dta_stat_2034106287_6_1_3_4, _dta_stat_2034106287_6_4, _dta_stat_2034106287_1_3_4, _dta_stat_2034106287_4_3_2, _dta_stat_2034106287_4_3_6](../../../../Images/Index.png)](#indexes)(5) | Status | varchar(50) | 50 | NULL allowed |
|  | TrailerId | varchar(50) | 50 | NULL allowed |
| [![Indexes _dta_stat_2034106287_6_1_3_4, _dta_stat_2034106287_6_4, _dta_stat_2034106287_4_3_6](../../../../Images/Index.png)](#indexes)(3) | DriverId | bigint | 8 | NULL allowed |
|  | TransporterId | bigint | 8 | NULL allowed |
|  | VinNo | varchar(50) | 50 | NULL allowed |
|  | MakeYear | varchar(50) | 50 | NULL allowed |
|  | Make | varchar(50) | 50 | NULL allowed |
|  | LicensePlate | varchar(50) | 50 | NULL allowed |
|  | Location | varchar(50) | 50 | NULL allowed |
|  | LocationStatus | varchar(50) | 50 | NULL allowed |
|  | TrailerCustomerDescription | varchar(100) | 100 | NULL allowed |
|  | Insulated | varchar(25) | 25 | NULL allowed |
|  | VaporRecovery | varchar(3) | 3 | NULL allowed |
|  | DryBreak | varchar(3) | 3 | NULL allowed |
|  | BellyRear | varchar(25) | 25 | NULL allowed |
|  | MaxTemp | varchar(10) | 10 | NULL allowed |
|  | CreateUser | varchar(50) | 50 | NULL allowed |
|  | CreateDateTime | datetime | 8 | NULL allowed |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |
|  | LastLocationStatus | varchar(50) | 50 | NULL allowed |
|  | ThirdPartyTransporter | int | 4 | NULL allowed |
|  | PTLoad | numeric(18,2) | 9 | NULL allowed |
|  | PTHour | numeric(18,2) | 9 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Equipment: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Equipment | Id | YES |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_2034106287_1_3_4 | Id, Type, Status |
| _dta_stat_2034106287_2_1 | Description, Id |
| _dta_stat_2034106287_2_3 | Description, Type |
| _dta_stat_2034106287_4_3_2 | Status, Type, Description |
| _dta_stat_2034106287_4_3_6 | Status, Type, DriverId |
| _dta_stat_2034106287_6_1_3_4 | DriverId, Id, Type, Status |
| _dta_stat_2034106287_6_4 | DriverId, Status |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Equipment]
(
[Id] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Description] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Type] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TrailerId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DriverId] [bigint] NULL,
[TransporterId] [bigint] NULL,
[VinNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MakeYear] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Make] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LicensePlate] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Location] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LocationStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TrailerCustomerDescription] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Insulated] [varchar] (25) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[VaporRecovery] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DryBreak] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BellyRear] [varchar] (25) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaxTemp] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LastLocationStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ThirdPartyTransporter] [int] NULL,
[PTLoad] [numeric] (18, 2) NULL,
[PTHour] [numeric] (18, 2) NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Equipment] ADD CONSTRAINT [PK_Equipment] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_2034106287_2_1] ON [dbo].[Equipment] ([Description], [Id])
GO
CREATE STATISTICS [_dta_stat_2034106287_2_3] ON [dbo].[Equipment] ([Description], [Type])
GO
CREATE STATISTICS [_dta_stat_2034106287_6_1_3_4] ON [dbo].[Equipment] ([DriverId], [Id], [Type], [Status])
GO
CREATE STATISTICS [_dta_stat_2034106287_6_4] ON [dbo].[Equipment] ([DriverId], [Status])
GO
CREATE STATISTICS [_dta_stat_2034106287_1_3_4] ON [dbo].[Equipment] ([Id], [Type], [Status])
GO
CREATE STATISTICS [_dta_stat_2034106287_4_3_2] ON [dbo].[Equipment] ([Status], [Type], [Description])
GO
CREATE STATISTICS [_dta_stat_2034106287_4_3_6] ON [dbo].[Equipment] ([Status], [Type], [DriverId])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwEquipmentDisplay]](../Views/dbo_vwEquipmentDisplay.md)
* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadSchedule]](../Views/dbo_vwRptLoadSchedule.md)
* [[dbo].[vwRptLoadScheduleNew]](../Views/dbo_vwRptLoadScheduleNew.md)
* [[dbo].[vwSelectActiveTrucks]](../Views/dbo_vwSelectActiveTrucks.md)
* [[dbo].[vwSelectActiveTrucksNew]](../Views/dbo_vwSelectActiveTrucksNew.md)
* [[dbo].[vwSelectEquipmentActiveTrailers]](../Views/dbo_vwSelectEquipmentActiveTrailers.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadDescription]](../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadDescription.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadDescriptionOld]](../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadDescriptionOld.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadId]](../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadId.md)
* [[dbo].[vwSelectEquipmentDriver]](../Views/dbo_vwSelectEquipmentDriver.md)
* [[dbo].[vwSelectEquipmentForSaturn]](../Views/dbo_vwSelectEquipmentForSaturn.md)
* [[dbo].[vwSelectEquipmentLastLoadDescription]](../Views/dbo_vwSelectEquipmentLastLoadDescription.md)
* [[dbo].[vwSelectEquipmentNotInUse]](../Views/dbo_vwSelectEquipmentNotInUse.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectLoadForSchedule]](../Views/dbo_vwSelectLoadForSchedule.md)
* [[dbo].[vwSelectLoads]](../Views/dbo_vwSelectLoads.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectTrailerLastLoad]](../Views/dbo_vwSelectTrailerLastLoad.md)
* [[dbo].[vwSelectTrailerScheduledLoads]](../Views/dbo_vwSelectTrailerScheduledLoads.md)
* [[dbo].[fnSelectActiveTrailerEquipment]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectActiveTrailerEquipment.md)
* [[dbo].[fnSelectActiveTruckEquipment]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectActiveTruckEquipment.md)
* [[dbo].[fnSelectEquipment]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectEquipment.md)
* [[dbo].[fnSelectOneEquipmentDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneEquipmentDriver.md)
* [[dbo].[fnTrailerLastLoadDescription]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerLastLoadDescription.md)
* [[dbo].[fnTrailerLastLoadId]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerLastLoadId.md)
* [[dbo].[fnTrailerTest]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

