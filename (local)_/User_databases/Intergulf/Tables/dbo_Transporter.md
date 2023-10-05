#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Transporter

# ![Tables](../../../../Images/Table32.png) [dbo].[Transporter]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 452 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 2:01:24 PM Friday, November 16, 2018 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Transporter: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(19,0) | 9 | NOT NULL |
|  | Name | varchar(100) | 100 | NULL allowed |
|  | Contact | varchar(50) | 50 | NULL allowed |
|  | Phone | varchar(50) | 50 | NULL allowed |
|  | EpaIdNo | varchar(50) | 50 | NULL allowed |
|  | TceqNo | varchar(50) | 50 | NULL allowed |
|  | DotNo | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Transporter: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Transporter | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Transporter]
(
[Id] [numeric] (19, 0) NOT NULL,
[Name] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Contact] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EpaIdNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TceqNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DotNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Transporter] ADD CONSTRAINT [PK_Transporter] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwEquipmentDisplay]](../Views/dbo_vwEquipmentDisplay.md)
* [[dbo].[vwRptLabTestForm]](../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadInventoryDetails]](../Views/dbo_vwRptLoadInventoryDetails.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileBol]](../Views/dbo_vwRptProfileBol.md)
* [[dbo].[vwRptProfileForm]](../Views/dbo_vwRptProfileForm.md)
* [[dbo].[vwRptProfileFormProduct]](../Views/dbo_vwRptProfileFormProduct.md)
* [[dbo].[vwRptProfileManifest]](../Views/dbo_vwRptProfileManifest.md)
* [[dbo].[vwRptProfileTCEQ]](../Views/dbo_vwRptProfileTCEQ.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectExportIntergulfDriversOnSiteTime]](../Views/dbo_vwSelectExportIntergulfDriversOnSiteTime.md)
* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)
* [[dbo].[vwSelectExportLoadsForAccounting]](../Views/dbo_vwSelectExportLoadsForAccounting.md)
* [[dbo].[vwSelectExportLoadsForSteers]](../Views/dbo_vwSelectExportLoadsForSteers.md)
* [[dbo].[vwSelectExportProfiles]](../Views/dbo_vwSelectExportProfiles.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectLoadsEManifestCheck]](../Views/dbo_vwSelectLoadsEManifestCheck.md)
* [[dbo].[vwSelectLoadsReadyForAccountingExport]](../Views/dbo_vwSelectLoadsReadyForAccountingExport.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)
* [[dbo].[vwSelectLoadsScheduleForExport]](../Views/dbo_vwSelectLoadsScheduleForExport.md)
* [[dbo].[vwSelectMonthlyDischarge]](../Views/dbo_vwSelectMonthlyDischarge.md)
* [[dbo].[vwSelectProfilePrePrint]](../Views/dbo_vwSelectProfilePrePrint.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectTransporterForSaturn]](../Views/dbo_vwSelectTransporterForSaturn.md)
* [[dbo].[fnSelectOneLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLabTest.md)
* [[dbo].[fnSelectTransporter]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectTransporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

