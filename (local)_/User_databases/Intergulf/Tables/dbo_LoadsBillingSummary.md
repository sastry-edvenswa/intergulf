#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsBillingSummary

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsBillingSummary]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 338400 |
| Created | 10:52:30 PM Monday, December 17, 2012 |
| Last Modified | 11:39:16 AM Monday, June 10, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsBillingSummary: LoadId](../../../../Images/pkcluster.png)](#indexes) | LoadId | bigint | 8 | NOT NULL |
|  | BillingTime | numeric(18,2) | 9 | NULL allowed |
|  | BillingRate | numeric(18,0) | 9 | NULL allowed |
|  | BillingDepartment | varchar(50) | 50 | NULL allowed |
|  | BillingStatus | varchar(50) | 50 | NULL allowed |
|  | DriverTimeNotes | varchar(2000) | 2000 | NULL allowed |
|  | AddWashOut | bit | 1 | NULL allowed |
|  | CreateDateTime | datetime | 8 | NULL allowed |
|  | CreateUser | varchar(50) | 50 | NULL allowed |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |
|  | DriverTime | numeric(18,2) | 9 | NULL allowed |
|  | TPBillingTime | numeric(18,2) | 9 | NULL allowed |
|  | TPBillingRate | numeric(18,0) | 9 | NULL allowed |
|  | TPDriverTime | numeric(18,2) | 9 | NULL allowed |
|  | TPAddWashOut | bit | 1 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LoadsBillingSummary: LoadId](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsBillingSummary | LoadId | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsBillingSummary]
(
[LoadId] [bigint] NOT NULL,
[BillingTime] [numeric] (18, 2) NULL,
[BillingRate] [numeric] (18, 0) NULL,
[BillingDepartment] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DriverTimeNotes] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AddWashOut] [bit] NULL,
[CreateDateTime] [datetime] NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DriverTime] [numeric] (18, 2) NULL,
[TPBillingTime] [numeric] (18, 2) NULL,
[TPBillingRate] [numeric] (18, 0) NULL,
[TPDriverTime] [numeric] (18, 2) NULL,
[TPAddWashOut] [bit] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsBillingSummary] ADD CONSTRAINT [PK_LoadsBillingSummary] PRIMARY KEY CLUSTERED ([LoadId]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadBillingAccountingNew]](../Views/dbo_vwRptLoadBillingAccountingNew.md)
* [[dbo].[vwRptLoadBillingSummary]](../Views/dbo_vwRptLoadBillingSummary.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadsTrailerStorage]](../Views/dbo_vwRptLoadsTrailerStorage.md)
* [[dbo].[vwSelectExportIntergulfDriversOnSiteTime]](../Views/dbo_vwSelectExportIntergulfDriversOnSiteTime.md)
* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)
* [[dbo].[vwSelectExportLoadsForAccounting]](../Views/dbo_vwSelectExportLoadsForAccounting.md)
* [[dbo].[vwSelectExportLoadsTruckTimes]](../Views/dbo_vwSelectExportLoadsTruckTimes.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectLoadsBillingMotiva20121001]](../Views/dbo_vwSelectLoadsBillingMotiva20121001.md)
* [[dbo].[vwSelectLoadsFor225ByMonth]](../Views/dbo_vwSelectLoadsFor225ByMonth.md)
* [[dbo].[vwSelectLoadsReadyForAccounting]](../Views/dbo_vwSelectLoadsReadyForAccounting.md)
* [[dbo].[vwSelectLoadsReadyForAccountingExport]](../Views/dbo_vwSelectLoadsReadyForAccountingExport.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)
* [[dbo].[vwSelectReadyToBillLoadsInternalNew]](../Views/dbo_vwSelectReadyToBillLoadsInternalNew.md)
* [[dbo].[vwSelectReadyToBillLoadsNew]](../Views/dbo_vwSelectReadyToBillLoadsNew.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectWashoutAllTables]](../Views/dbo_vwSelectWashoutAllTables.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

