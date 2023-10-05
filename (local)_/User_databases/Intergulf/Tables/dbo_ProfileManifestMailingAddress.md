#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileManifestMailingAddress

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileManifestMailingAddress]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 646 |
| Created | 10:03:01 PM Monday, August 8, 2011 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileManifestMailingAddress: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL |
|  | Name | varchar(100) | 100 | NULL allowed |
|  | Address | varchar(3000) | 3000 | NULL allowed |
|  | City | varchar(50) | 50 | NULL allowed |
|  | State | varchar(50) | 50 | NULL allowed |
|  | Zip | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileManifestMailingAddress: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileManifestMailingAddress | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileManifestMailingAddress]
(
[Id] [bigint] NOT NULL,
[Name] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Address] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Zip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileManifestMailingAddress] ADD CONSTRAINT [PK_ProfileManifestMailingAddress] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
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

