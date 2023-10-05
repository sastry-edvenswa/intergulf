#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProductHazardousMaterial

# ![Tables](../../../../Images/Table32.png) [dbo].[ProductHazardousMaterial]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 3880 |
| Created | 6:47:35 PM Monday, January 29, 2007 |
| Last Modified | 6:47:35 PM Monday, January 29, 2007 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|
| ID | int | 4 | NOT NULL |
| Symbols | nvarchar(8) | 16 | NULL allowed |
| ProperShippingName | nvarchar(1000) | 2000 | NULL allowed |
| HazardClass | nvarchar(15) | 30 | NULL allowed |
| UNNumber | nvarchar(10) | 20 | NULL allowed |
| PackingGroup | nvarchar(5) | 10 | NULL allowed |
| Label | nvarchar(30) | 60 | NULL allowed |
| SpecialProvisions | nvarchar(90) | 180 | NULL allowed |
| Exception | nvarchar(15) | 30 | NULL allowed |
| NonBulk | nvarchar(15) | 30 | NULL allowed |
| Bulk | nvarchar(15) | 30 | NULL allowed |
| PassengerAir | nvarchar(15) | 30 | NULL allowed |
| CargoAir | nvarchar(15) | 30 | NULL allowed |
| Vessel | nvarchar(5) | 10 | NULL allowed |
| VesselSP | nvarchar(35) | 70 | NULL allowed |
| SortOrder | int | 4 | NULL allowed |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProductHazardousMaterial]
(
[ID] [int] NOT NULL,
[Symbols] [nvarchar] (8) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProperShippingName] [nvarchar] (1000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HazardClass] [nvarchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UNNumber] [nvarchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PackingGroup] [nvarchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Label] [nvarchar] (30) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecialProvisions] [nvarchar] (90) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Exception] [nvarchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NonBulk] [nvarchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Bulk] [nvarchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PassengerAir] [nvarchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CargoAir] [nvarchar] (15) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Vessel] [nvarchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[VesselSP] [nvarchar] (35) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SortOrder] [int] NULL
) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileBol]](../Views/dbo_vwRptProfileBol.md)
* [[dbo].[vwRptProfileManifest]](../Views/dbo_vwRptProfileManifest.md)
* [[dbo].[vwRptProfileTCEQ]](../Views/dbo_vwRptProfileTCEQ.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[fnSelectProductHazardousMaterial]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProductHazardousMaterial.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

