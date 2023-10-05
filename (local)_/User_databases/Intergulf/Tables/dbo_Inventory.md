#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Inventory

# ![Tables](../../../../Images/Table32.png) [dbo].[Inventory]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 3403 |
| Created | 12:22:09 PM Thursday, February 21, 2008 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_InventoryIn: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | Customer | varchar(50) | 50 | NULL allowed |  |
|  | Category | varchar(50) | 50 | NULL allowed |  |
|  | Tank | varchar(50) | 50 | NULL allowed |  |
|  | ExposureDate | datetime | 8 | NULL allowed |  |
|  | Quantity | bigint | 8 | NULL allowed |  |
|  | Cost | decimal(19,4) | 9 | NULL allowed |  |
|  | TransType | varchar(50) | 50 | NULL allowed |  |
|  | TransDate | datetime | 8 | NULL allowed |  |
|  | IncomingQuantity | bigint | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InventoryIn: Id](../../../../Images/pkcluster.png)](#indexes) | PK_InventoryIn | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Inventory]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[Customer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Category] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Tank] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExposureDate] [datetime] NULL,
[Quantity] [bigint] NULL,
[Cost] [decimal] (19, 4) NULL,
[TransType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransDate] [datetime] NULL,
[IncomingQuantity] [bigint] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Inventory] ADD CONSTRAINT [PK_InventoryIn] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

