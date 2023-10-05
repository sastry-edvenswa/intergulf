#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.EquipmentLastLoadDescription

# ![Tables](../../../../Images/Table32.png) [dbo].[EquipmentLastLoadDescription]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 295 |
| Created | 10:10:54 PM Monday, July 17, 2017 |
| Last Modified | 10:10:54 PM Monday, July 17, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_EquipmentLastLoadDescription: Description](../../../../Images/pkcluster.png)](#indexes) | Description | varchar(800) | 800 | NOT NULL |
|  | Status | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_EquipmentLastLoadDescription: Description](../../../../Images/pkcluster.png)](#indexes) | PK_EquipmentLastLoadDescription | Description | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[EquipmentLastLoadDescription]
(
[Description] [varchar] (800) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[EquipmentLastLoadDescription] ADD CONSTRAINT [PK_EquipmentLastLoadDescription] PRIMARY KEY CLUSTERED ([Description]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

