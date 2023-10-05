#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LabMetals

# ![Tables](../../../../Images/Table32.png) [dbo].[LabMetals]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 8 |
| Created | 6:47:33 PM Monday, January 29, 2007 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LabMetals: Description](../../../../Images/pkcluster.png)](#indexes) | Description | varchar(50) | 50 | NOT NULL |
|  | WasteLimit | bigint | 8 | NULL allowed |
|  | RecycleLimit | bigint | 8 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LabMetals: Description](../../../../Images/pkcluster.png)](#indexes) | PK_LabMetals | Description | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LabMetals]
(
[Description] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[WasteLimit] [bigint] NULL,
[RecycleLimit] [bigint] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LabMetals] ADD CONSTRAINT [PK_LabMetals] PRIMARY KEY CLUSTERED ([Description]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

