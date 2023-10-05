#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Destination

# ![Tables](../../../../Images/Table32.png) [dbo].[Destination]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 476 |
| Created | 8:42:11 PM Thursday, February 22, 2007 |
| Last Modified | 3:58:22 PM Tuesday, February 5, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Indexes _dta_index_Destination_5_1634104862__K1_2_19, _dta_stat_1634104862_1_2](../../../../Images/Index.png)](#indexes)(2) | Id | int | 4 | NOT NULL | 1 - 1 |
| [![Indexes _dta_index_Destination_5_1634104862__K1_2_19, _dta_stat_1634104862_1_2](../../../../Images/Index.png)](#indexes)(2) | Name | nvarchar(100) | 200 | NULL allowed |  |
|  | Address | nvarchar(50) | 100 | NULL allowed |  |
|  | City | nvarchar(50) | 100 | NULL allowed |  |
|  | State | nvarchar(50) | 100 | NULL allowed |  |
|  | Zip | nvarchar(50) | 100 | NULL allowed |  |
|  | Contact | nvarchar(50) | 100 | NULL allowed |  |
|  | Phone | nvarchar(50) | 100 | NULL allowed |  |
|  | Fax | nvarchar(50) | 100 | NULL allowed |  |
|  | Email | nvarchar(50) | 100 | NULL allowed |  |
|  | Notes | nvarchar(500) | 1000 | NULL allowed |  |
|  | EpaIdNo | nvarchar(50) | 100 | NULL allowed |  |
|  | TceqNo | nvarchar(50) | 100 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | AllowHazards | varchar(2) | 2 | NULL allowed |  |
|  | FacilityName | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Destination_5_1634104862__K1_2_19](../../../../Images/Index.png)](#indexes) | Facility | varchar(50) | 50 | NULL allowed |  |
|  | Status | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Name | Key Columns | Included Columns |
|---|---|---|
| _dta_index_Destination_5_1634104862__K1_2_19 | Id | Name, Facility |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_1634104862_1_2 | Id, Name |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Destination]
(
[Id] [int] NOT NULL IDENTITY(1, 1),
[Name] [nvarchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Address] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Zip] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Contact] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Fax] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Email] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [nvarchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EpaIdNo] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TceqNo] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AllowHazards] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FacilityName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Facility] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_Destination_5_1634104862__K1_2_19] ON [dbo].[Destination] ([Id]) INCLUDE ([Name], [Facility]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_1634104862_1_2] ON [dbo].[Destination] ([Id], [Name])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfile]](../Views/dbo_vwChooseProfile.md)
* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadMaterialDestination]](../Views/dbo_vwRptLoadMaterialDestination.md)
* [[dbo].[vwRptLoadMaterialGenerator]](../Views/dbo_vwRptLoadMaterialGenerator.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarks]](../Views/dbo_vwRptLoadMaterialGeneratorKStarks.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarksProfileNo]](../Views/dbo_vwRptLoadMaterialGeneratorKStarksProfileNo.md)
* [[dbo].[vwRptLoadRequest]](../Views/dbo_vwRptLoadRequest.md)
* [[dbo].[vwRptLoadSchedule]](../Views/dbo_vwRptLoadSchedule.md)
* [[dbo].[vwRptLoadScheduleNew]](../Views/dbo_vwRptLoadScheduleNew.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileBol]](../Views/dbo_vwRptProfileBol.md)
* [[dbo].[vwRptProfileTCEQ]](../Views/dbo_vwRptProfileTCEQ.md)
* [[dbo].[vwRptWasteLoads]](../Views/dbo_vwRptWasteLoads.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectExportBayportTimes]](../Views/dbo_vwSelectExportBayportTimes.md)
* [[dbo].[vwSelectExportIntergulfDriversOnSiteTime]](../Views/dbo_vwSelectExportIntergulfDriversOnSiteTime.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportLoadLabVolumeNew]](../Views/dbo_vwSelectExportLoadLabVolumeNew.md)
* [[dbo].[vwSelectExportLoadsForEBE]](../Views/dbo_vwSelectExportLoadsForEBE.md)
* [[dbo].[vwSelectExportLoadsForEBETemp]](../Views/dbo_vwSelectExportLoadsForEBETemp.md)
* [[dbo].[vwSelectExportLoadsForSchedule]](../Views/dbo_vwSelectExportLoadsForSchedule.md)
* [[dbo].[vwSelectExportLoadsForSteers]](../Views/dbo_vwSelectExportLoadsForSteers.md)
* [[dbo].[vwSelectExportProfiles]](../Views/dbo_vwSelectExportProfiles.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectExportProfileVolume]](../Views/dbo_vwSelectExportProfileVolume.md)
* [[dbo].[vwSelectExportStrangTimes]](../Views/dbo_vwSelectExportStrangTimes.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectLoadForSchedule]](../Views/dbo_vwSelectLoadForSchedule.md)
* [[dbo].[vwSelectLoadRequestForSchedule]](../Views/dbo_vwSelectLoadRequestForSchedule.md)
* [[dbo].[vwSelectLoads]](../Views/dbo_vwSelectLoads.md)
* [[dbo].[vwSelectLoadsByProfileCreateDate]](../Views/dbo_vwSelectLoadsByProfileCreateDate.md)
* [[dbo].[vwSelectLoadsEManifestCheck]](../Views/dbo_vwSelectLoadsEManifestCheck.md)
* [[dbo].[vwSelectLoadsFor225ByMonth]](../Views/dbo_vwSelectLoadsFor225ByMonth.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectLoadsForBayportTurnTimes]](../Views/dbo_vwSelectLoadsForBayportTurnTimes.md)
* [[dbo].[vwSelectLoadsForSaturn]](../Views/dbo_vwSelectLoadsForSaturn.md)
* [[dbo].[vwSelectLoadsMotiva20121001]](../Views/dbo_vwSelectLoadsMotiva20121001.md)
* [[dbo].[vwSelectLoadsScheduledForChart]](../Views/dbo_vwSelectLoadsScheduledForChart.md)
* [[dbo].[vwSelectLoadsScheduleForExport]](../Views/dbo_vwSelectLoadsScheduleForExport.md)
* [[dbo].[vwSelectMonthlyDischarge]](../Views/dbo_vwSelectMonthlyDischarge.md)
* [[dbo].[vwSelectPendingLoads]](../Views/dbo_vwSelectPendingLoads.md)
* [[dbo].[vwSelectProfilePrePrint]](../Views/dbo_vwSelectProfilePrePrint.md)
* [[dbo].[vwSelectProfileVolumeTest]](../Views/dbo_vwSelectProfileVolumeTest.md)
* [[dbo].[vwSelectRequestedLoads]](../Views/dbo_vwSelectRequestedLoads.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectScheduledLoads]](../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[vwSelectTrailerScheduledLoads]](../Views/dbo_vwSelectTrailerScheduledLoads.md)
* [[dbo].[vwSteersTest]](../Views/dbo_vwSteersTest.md)
* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectProfileGlobalSearch]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfileGlobalSearch.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

