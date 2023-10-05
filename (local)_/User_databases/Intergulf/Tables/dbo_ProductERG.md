#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProductERG

# ![Tables](../../../../Images/Table32.png) [dbo].[ProductERG]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 3407 |
| Created | 6:47:35 PM Monday, January 29, 2007 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ProductERG: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | MATERIAL | nvarchar(255) | 510 | NULL allowed |
|  | UN_NUMBER | nvarchar(255) | 510 | NULL allowed |
|  | NUMERIC_ID | float | 8 | NULL allowed |
|  | ALPHA_ID | float | 8 | NULL allowed |
|  | GUIDE_PAGE | nvarchar(255) | 510 | NULL allowed |
|  | PRTC_TABLE | nvarchar(255) | 510 | NULL allowed |
|  | WATR_REACT | nvarchar(255) | 510 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProductERG: ID](../../../../Images/pkcluster.png)](#indexes) | PK_ProductERG | ID | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProductERG]
(
[ID] [int] NOT NULL,
[MATERIAL] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UN_NUMBER] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NUMERIC_ID] [float] NULL,
[ALPHA_ID] [float] NULL,
[GUIDE_PAGE] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PRTC_TABLE] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WATR_REACT] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProductERG] ADD CONSTRAINT [PK_ProductERG] PRIMARY KEY CLUSTERED ([ID]) ON [PRIMARY]
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


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

