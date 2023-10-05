#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsTrailerStorageReport

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsTrailerStorageReport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 5443 |
| Created | 10:16:49 PM Sunday, May 5, 2013 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsTrailerStorageReport: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | LoadId | bigint | 8 | NOT NULL |  |
|  | TrailerId | varchar(50) | 50 | NULL allowed |  |
|  | StartDate | datetime | 8 | NULL allowed |  |
|  | EndDate | datetime | 8 | NULL allowed |  |
|  | UserName | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LoadsTrailerStorageReport: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsTrailerStorageReport | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsTrailerStorageReport]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[LoadId] [bigint] NOT NULL,
[TrailerId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[StartDate] [datetime] NULL,
[EndDate] [datetime] NULL,
[UserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsTrailerStorageReport] ADD CONSTRAINT [PK_LoadsTrailerStorageReport] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadsTrailerStorage]](../Views/dbo_vwRptLoadsTrailerStorage.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

