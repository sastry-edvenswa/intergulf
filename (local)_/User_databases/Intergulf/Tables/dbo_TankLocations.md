#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.TankLocations

# ![Tables](../../../../Images/Table32.png) [dbo].[TankLocations]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 18 |
| Created | 5:49:17 PM Wednesday, September 25, 2019 |
| Last Modified | 5:49:17 PM Wednesday, September 25, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_TankLocations: Location](../../../../Images/pkcluster.png)](#indexes) | Location | varchar(50) | 50 | NOT NULL |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TankLocations: Location](../../../../Images/pkcluster.png)](#indexes) | PK_TankLocations | Location | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[TankLocations]
(
[Location] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[TankLocations] ADD CONSTRAINT [PK_TankLocations] PRIMARY KEY CLUSTERED ([Location]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

