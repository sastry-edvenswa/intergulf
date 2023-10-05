#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.MaterialCode

# ![Tables](../../../../Images/Table32.png) [dbo].[MaterialCode]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1244 |
| Created | 11:05:54 PM Monday, December 17, 2012 |
| Last Modified | 3:58:13 PM Tuesday, February 5, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Key _dta_index_MaterialCode_c_5_599673184__K1: ID](../../../../Images/cluster.png)](#indexes)[![Indexes _dta_stat_599673184_1_3_2](../../../../Images/Index.png)](#indexes) | ID | int | 4 | NOT NULL | 1 - 1 |
| [![Indexes _dta_stat_599673184_3_2, _dta_stat_599673184_1_3_2, _dta_stat_599673184_2_29](../../../../Images/Index.png)](#indexes)(3) | MaterialCode | nvarchar(50) | 100 | NULL allowed |  |
| [![Indexes _dta_stat_599673184_3_2, _dta_stat_599673184_1_3_2](../../../../Images/Index.png)](#indexes)(2) | Description | nvarchar(50) | 100 | NULL allowed |  |
|  | PreProperShippingName | nvarchar(100) | 200 | NULL allowed |  |
|  | ProperShippingName | nvarchar(300) | 600 | NULL allowed |  |
|  | PostProperShippingName | nvarchar(100) | 200 | NULL allowed |  |
|  | ProfileType | nvarchar(50) | 100 | NULL allowed |  |
|  | AltProperShippingName | nvarchar(100) | 200 | NULL allowed |  |
|  | MSDSNumber | nvarchar(50) | 100 | NULL allowed |  |
|  | Notes | ntext | max | NULL allowed |  |
|  | Hazmat | nvarchar(50) | 100 | NULL allowed |  |
|  | Number | nvarchar(50) | 100 | NULL allowed |  |
|  | PackageType | nvarchar(50) | 100 | NULL allowed |  |
|  | ProductName | nvarchar(50) | 100 | NULL allowed |  |
|  | ProductClassification | nvarchar(50) | 100 | NULL allowed |  |
|  | ProductPackingGroup | nvarchar(50) | 100 | NULL allowed |  |
|  | ProductHazardClass | nvarchar(50) | 100 | NULL allowed |  |
|  | ProductPlacardNumber | nvarchar(50) | 100 | NULL allowed |  |
|  | CustomersUsing | nvarchar(50) | 100 | NULL allowed |  |
|  | IntergulfClass | nvarchar(50) | 100 | NULL allowed |  |
|  | ProperShippingNameId | bigint | 8 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | IsRQ | bit | 1 | NULL allowed |  |
|  | IsWaste | bit | 1 | NULL allowed |  |
|  | Constituents1 | nvarchar(50) | 100 | NULL allowed |  |
|  | Constituents2 | nvarchar(50) | 100 | NULL allowed |  |
| [![Indexes _dta_stat_599673184_2_29](../../../../Images/Index.png)](#indexes) | ReviewedById | nvarchar(50) | 100 | NULL allowed |  |
|  | UseProperShippingName | nvarchar(500) | 1000 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns |
|---|---|---|
| [![Cluster Key _dta_index_MaterialCode_c_5_599673184__K1: ID](../../../../Images/cluster.png)](#indexes) | _dta_index_MaterialCode_c_5_599673184__K1 | ID |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_599673184_1_3_2 | ID, Description, MaterialCode |
| _dta_stat_599673184_2_29 | MaterialCode, ReviewedById |
| _dta_stat_599673184_3_2 | Description, MaterialCode |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[MaterialCode]
(
[ID] [int] NOT NULL IDENTITY(1, 1),
[MaterialCode] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Description] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PreProperShippingName] [nvarchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProperShippingName] [nvarchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PostProperShippingName] [nvarchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileType] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AltProperShippingName] [nvarchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MSDSNumber] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [ntext] COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Hazmat] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Number] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PackageType] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProductName] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProductClassification] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProductPackingGroup] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProductHazardClass] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProductPlacardNumber] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomersUsing] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[IntergulfClass] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProperShippingNameId] [bigint] NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[IsRQ] [bit] NULL,
[IsWaste] [bit] NULL,
[Constituents1] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Constituents2] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReviewedById] [nvarchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UseProperShippingName] [nvarchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
CREATE CLUSTERED INDEX [_dta_index_MaterialCode_c_5_599673184__K1] ON [dbo].[MaterialCode] ([ID]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_599673184_3_2] ON [dbo].[MaterialCode] ([Description], [MaterialCode])
GO
CREATE STATISTICS [_dta_stat_599673184_1_3_2] ON [dbo].[MaterialCode] ([ID], [Description], [MaterialCode])
GO
CREATE STATISTICS [_dta_stat_599673184_2_29] ON [dbo].[MaterialCode] ([MaterialCode], [ReviewedById])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadAccountingDetail]](../Views/dbo_vwRptLoadAccountingDetail.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadLabWorksheet]](../Views/dbo_vwRptLoadLabWorksheet.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadRequest]](../Views/dbo_vwRptLoadRequest.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileBol]](../Views/dbo_vwRptProfileBol.md)
* [[dbo].[vwRptProfileManifest]](../Views/dbo_vwRptProfileManifest.md)
* [[dbo].[vwRptProfileTCEQ]](../Views/dbo_vwRptProfileTCEQ.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectExportProfiles]](../Views/dbo_vwSelectExportProfiles.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectLoadsCount]](../Views/dbo_vwSelectLoadsCount.md)
* [[dbo].[vwSelectLoadsInactive]](../Views/dbo_vwSelectLoadsInactive.md)
* [[dbo].[vwSelectProfileProperShippingName]](../Views/dbo_vwSelectProfileProperShippingName.md)
* [[dbo].[vwSelectProfilesInactive]](../Views/dbo_vwSelectProfilesInactive.md)
* [[dbo].[vwSelectProfilesWithErrors]](../Views/dbo_vwSelectProfilesWithErrors.md)
* [[dbo].[vwSelectReviewProfileProperShippingName]](../Views/dbo_vwSelectReviewProfileProperShippingName.md)
* [[dbo].[fnProperShippingName]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProperShippingName.md)
* [[dbo].[fnSelectMaterialCode]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectMaterialCode.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

