#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Driver

# ![Tables](../../../../Images/Table32.png) [dbo].[Driver]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 362 |
| Created | 6:47:33 PM Monday, January 29, 2007 |
| Last Modified | 3:35:50 PM Wednesday, May 29, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Driver: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | DriverId | bigint | 8 | NULL allowed |  |
|  | FirstName | varchar(50) | 50 | NULL allowed |  |
|  | LastName | varchar(50) | 50 | NULL allowed |  |
|  | SsNo | varchar(50) | 50 | NULL allowed |  |
|  | BirthDate | datetime | 8 | NULL allowed |  |
|  | LicenseExpirationDate | datetime | 8 | NULL allowed |  |
|  | Status | varchar(50) | 50 | NULL allowed |  |
|  | Phone | varchar(50) | 50 | NULL allowed |  |
|  | Cell | varchar(50) | 50 | NULL allowed |  |
|  | ShipQualified | int | 4 | NULL allowed |  |
|  | InTraining | int | 4 | NULL allowed |  |
|  | NonHazOnly | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Driver: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Driver | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Driver]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[DriverId] [bigint] NULL,
[FirstName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LastName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SsNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BirthDate] [datetime] NULL,
[LicenseExpirationDate] [datetime] NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Cell] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ShipQualified] [int] NULL,
[InTraining] [int] NULL,
[NonHazOnly] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Driver] ADD CONSTRAINT [PK_Driver] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwEquipmentDisplay]](../Views/dbo_vwEquipmentDisplay.md)
* [[dbo].[vwRptLabTestForm]](../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadSchedule]](../Views/dbo_vwRptLoadSchedule.md)
* [[dbo].[vwRptLoadScheduleNew]](../Views/dbo_vwRptLoadScheduleNew.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwSaturnTestDriver]](../Views/dbo_vwSaturnTestDriver.md)
* [[dbo].[vwSelectActiveTrucks]](../Views/dbo_vwSelectActiveTrucks.md)
* [[dbo].[vwSelectActiveTrucksNew]](../Views/dbo_vwSelectActiveTrucksNew.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectDriverForSaturn]](../Views/dbo_vwSelectDriverForSaturn.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectEquipmentActiveTrailers]](../Views/dbo_vwSelectEquipmentActiveTrailers.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadDescription]](../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadDescription.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadDescriptionOld]](../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadDescriptionOld.md)
* [[dbo].[vwSelectEquipmentActiveTrailersLastLoadId]](../Views/dbo_vwSelectEquipmentActiveTrailersLastLoadId.md)
* [[dbo].[vwSelectEquipmentDriver]](../Views/dbo_vwSelectEquipmentDriver.md)
* [[dbo].[vwSelectEquipmentNotInUse]](../Views/dbo_vwSelectEquipmentNotInUse.md)
* [[dbo].[vwSelectExportLoadsForEBE]](../Views/dbo_vwSelectExportLoadsForEBE.md)
* [[dbo].[vwSelectExportLoadsForEBETemp]](../Views/dbo_vwSelectExportLoadsForEBETemp.md)
* [[dbo].[vwSelectLegOneDriverOnSiteTime]](../Views/dbo_vwSelectLegOneDriverOnSiteTime.md)
* [[dbo].[vwSelectLoadBillingTimes]](../Views/dbo_vwSelectLoadBillingTimes.md)
* [[dbo].[vwSelectLoadDriver]](../Views/dbo_vwSelectLoadDriver.md)
* [[dbo].[vwSelectLoadsForSaturn]](../Views/dbo_vwSelectLoadsForSaturn.md)
* [[dbo].[vwSelectPendingLoads]](../Views/dbo_vwSelectPendingLoads.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectScheduledLoads]](../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[fnSelectActiveDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectActiveDriver.md)
* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)
* [[dbo].[fnSelectOneEquipmentDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneEquipmentDriver.md)
* [[dbo].[fnSelectOneLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLabTest.md)
* [[dbo].[fnSelectScheduledLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectScheduledLoads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

