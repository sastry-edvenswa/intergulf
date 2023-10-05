#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InventoryHedgePositions

# ![Tables](../../../../Images/Table32.png) [dbo].[InventoryHedgePositions]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 237 |
| Created | 12:23:09 PM Thursday, February 21, 2008 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_InventoryHedgePositions: MarketDate](../../../../Images/pkcluster.png)](#indexes) | MarketDate | datetime | 8 | NOT NULL |
|  | HighGravityOilPosition | bigint | 8 | NULL allowed |
|  | HighGravityOilQuantity | bigint | 8 | NULL allowed |
|  | FuelOilPosition | bigint | 8 | NULL allowed |
|  | FuelOilQuantity | bigint | 8 | NULL allowed |
|  | FeedStockOilPosition | bigint | 8 | NULL allowed |
|  | FeedStockOilQuantity | bigint | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InventoryHedgePositions: MarketDate](../../../../Images/pkcluster.png)](#indexes) | PK_InventoryHedgePositions | MarketDate | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InventoryHedgePositions]
(
[MarketDate] [datetime] NOT NULL,
[HighGravityOilPosition] [bigint] NULL,
[HighGravityOilQuantity] [bigint] NULL,
[FuelOilPosition] [bigint] NULL,
[FuelOilQuantity] [bigint] NULL,
[FeedStockOilPosition] [bigint] NULL,
[FeedStockOilQuantity] [bigint] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[InventoryHedgePositions] ADD CONSTRAINT [PK_InventoryHedgePositions] PRIMARY KEY CLUSTERED ([MarketDate]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

