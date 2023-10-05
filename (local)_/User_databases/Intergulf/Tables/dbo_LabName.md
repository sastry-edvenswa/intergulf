#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LabName

# ![Tables](../../../../Images/Table32.png) [dbo].[LabName]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 8 |
| Created | 9:17:25 AM Saturday, May 1, 2021 |
| Last Modified | 9:18:16 AM Saturday, May 1, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LabName: LabName](../../../../Images/pkcluster.png)](#indexes) | LabName | varchar(50) | 50 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LabName: LabName](../../../../Images/pkcluster.png)](#indexes) | PK_LabName | LabName | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LabName]
(
[LabName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LabName] ADD CONSTRAINT [PK_LabName] PRIMARY KEY CLUSTERED ([LabName]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

