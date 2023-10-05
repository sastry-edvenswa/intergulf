#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InventoryLevels

# ![Tables](../../../../Images/Table32.png) [dbo].[InventoryLevels]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1130 |
| Created | 12:23:37 PM Thursday, February 21, 2008 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_InventoryCategoryLevels: MarketDate](../../../../Images/pkcluster.png)](#indexes) | MarketDate | datetime | 8 | NOT NULL |
|  | HighGravityOilLevel | numeric(19,0) | 9 | NULL allowed |
|  | FuelOilLevel | numeric(19,0) | 9 | NULL allowed |
|  | FeedStockOilLevel | numeric(19,0) | 9 | NULL allowed |
|  | AHighGravityOilLevel | numeric(19,0) | 9 | NULL allowed |
|  | AFuelOilLevel | numeric(19,0) | 9 | NULL allowed |
|  | AFeedStockOilLevel | numeric(19,0) | 9 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |
|  | HighGravityOilSale | numeric(18,0) | 9 | NULL allowed |
|  | FuelOilSale | numeric(18,0) | 9 | NULL allowed |
|  | FeedStockOilSale | numeric(18,0) | 9 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InventoryCategoryLevels: MarketDate](../../../../Images/pkcluster.png)](#indexes) | PK_InventoryCategoryLevels | MarketDate | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InventoryLevels]
(
[MarketDate] [datetime] NOT NULL,
[HighGravityOilLevel] [numeric] (19, 0) NULL,
[FuelOilLevel] [numeric] (19, 0) NULL,
[FeedStockOilLevel] [numeric] (19, 0) NULL,
[AHighGravityOilLevel] [numeric] (19, 0) NULL,
[AFuelOilLevel] [numeric] (19, 0) NULL,
[AFeedStockOilLevel] [numeric] (19, 0) NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HighGravityOilSale] [numeric] (18, 0) NULL,
[FuelOilSale] [numeric] (18, 0) NULL,
[FeedStockOilSale] [numeric] (18, 0) NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[InventoryLevels] ADD CONSTRAINT [PK_InventoryCategoryLevels] PRIMARY KEY CLUSTERED ([MarketDate]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

