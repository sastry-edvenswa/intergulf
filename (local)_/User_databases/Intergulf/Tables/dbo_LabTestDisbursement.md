#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LabTestDisbursement

# ![Tables](../../../../Images/Table32.png) [dbo].[LabTestDisbursement]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 319980 |
| Created | 6:47:34 PM Monday, January 29, 2007 |
| Last Modified | 7:47:25 PM Thursday, May 11, 2023 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LabTestDisbursement: Id\LabTestId\Tank](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6](../../../../Images/Index.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Cluster Primary Key PK_LabTestDisbursement: Id\LabTestId\Tank](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6](../../../../Images/Index.png)](#indexes) | LabTestId | bigint | 8 | NOT NULL |  |
| [![Cluster Primary Key PK_LabTestDisbursement: Id\LabTestId\Tank](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6](../../../../Images/Index.png)](#indexes) | Tank | varchar(50) | 50 | NOT NULL |  |
| [![Indexes _dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6](../../../../Images/Index.png)](#indexes) | Phase | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6](../../../../Images/Index.png)](#indexes) | Quantity | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6](../../../../Images/Index.png)](#indexes) | Unit | varchar(50) | 50 | NULL allowed |  |
|  | OnLoan | varchar(3) | 3 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LabTestDisbursement: Id\LabTestId\Tank](../../../../Images/pkcluster.png)](#indexes) | PK_LabTestDisbursement | Id, LabTestId, Tank |  | YES |
|  | _dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6 | LabTestId, Tank, Phase | Id, Quantity, Unit |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LabTestDisbursement]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[LabTestId] [bigint] NOT NULL,
[Tank] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Phase] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Quantity] [decimal] (18, 2) NULL,
[Unit] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OnLoan] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LabTestDisbursement] ADD CONSTRAINT [PK_LabTestDisbursement] PRIMARY KEY CLUSTERED ([Id], [LabTestId], [Tank]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LabTestDisbursement_5_21575115__K2_K3_K4_1_5_6] ON [dbo].[LabTestDisbursement] ([LabTestId], [Tank], [Phase]) INCLUDE ([Id], [Quantity], [Unit]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwRptLabTestFormDisbursements]](../Views/dbo_vwRptLabTestFormDisbursements.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwSaturnTestLabTextDisbursement]](../Views/dbo_vwSaturnTestLabTextDisbursement.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportLoadLabVolumeNew]](../Views/dbo_vwSelectExportLoadLabVolumeNew.md)
* [[dbo].[vwSelectLabTestDisbursement]](../Views/dbo_vwSelectLabTestDisbursement.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectSaturnTransactionsLoads]](../Views/dbo_vwSelectSaturnTransactionsLoads.md)
* [[dbo].[fnSelectLabTestDisbursement]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTestDisbursement.md)
* [[dbo].[fnSelectLoadTanks]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSelectLoadTanks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

