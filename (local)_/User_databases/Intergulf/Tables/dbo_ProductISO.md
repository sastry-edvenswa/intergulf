#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProductISO

# ![Tables](../../../../Images/Table32.png) [dbo].[ProductISO]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 633 |
| Created | 6:47:35 PM Monday, January 29, 2007 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ProductISO: ID](../../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NOT NULL |
|  | UN_NUMBER | nvarchar(255) | 510 | NULL allowed |
|  | MATERIAL | nvarchar(255) | 510 | NULL allowed |
|  | SISO_MAX_M | nvarchar(255) | 510 | NULL allowed |
|  | SPRO_MAXDM | nvarchar(255) | 510 | NULL allowed |
|  | SPRO_MAXNM | nvarchar(255) | 510 | NULL allowed |
|  | LISO_MAX_M | nvarchar(255) | 510 | NULL allowed |
|  | LPRO_MAXDM | nvarchar(255) | 510 | NULL allowed |
|  | LPRO_MAXNM | nvarchar(255) | 510 | NULL allowed |
|  | SISO_MAX | nvarchar(255) | 510 | NULL allowed |
|  | SPRO_MAXD | nvarchar(255) | 510 | NULL allowed |
|  | SPRO_MAXN | nvarchar(255) | 510 | NULL allowed |
|  | LISO_MAX | nvarchar(255) | 510 | NULL allowed |
|  | LPRO_MAXD | nvarchar(255) | 510 | NULL allowed |
|  | LPRO_MAXN | nvarchar(255) | 510 | NULL allowed |
|  | SHIP_HAZ | nvarchar(255) | 510 | NULL allowed |
|  | WATER | nvarchar(255) | 510 | NULL allowed |
|  | SORTID | float | 8 | NULL allowed |
|  | W_FRMULA | nvarchar(255) | 510 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProductISO: ID](../../../../Images/pkcluster.png)](#indexes) | PK_ProductISO | ID | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProductISO]
(
[ID] [int] NOT NULL,
[UN_NUMBER] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MATERIAL] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SISO_MAX_M] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SPRO_MAXDM] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SPRO_MAXNM] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LISO_MAX_M] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LPRO_MAXDM] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LPRO_MAXNM] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SISO_MAX] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SPRO_MAXD] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SPRO_MAXN] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LISO_MAX] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LPRO_MAXD] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LPRO_MAXN] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SHIP_HAZ] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WATER] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SORTID] [float] NULL,
[W_FRMULA] [nvarchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProductISO] ADD CONSTRAINT [PK_ProductISO] PRIMARY KEY CLUSTERED ([ID]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

