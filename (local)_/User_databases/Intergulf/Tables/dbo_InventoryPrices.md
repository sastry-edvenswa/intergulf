#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InventoryPrices

# ![Tables](../../../../Images/Table32.png) [dbo].[InventoryPrices]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 462 |
| Created | 12:23:56 PM Thursday, February 21, 2008 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_InventoryPrices: MarketDate](../../../../Images/pkcluster.png)](#indexes) | MarketDate | datetime | 8 | NOT NULL |
|  | HighGravityOilPlatts | numeric(18,4) | 9 | NULL allowed |
|  | HighGravityOilNymex | numeric(18,4) | 9 | NULL allowed |
|  | FuelOilPlatts | numeric(18,2) | 9 | NULL allowed |
|  | FeedStockOilPlatts | numeric(18,2) | 9 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InventoryPrices: MarketDate](../../../../Images/pkcluster.png)](#indexes) | PK_InventoryPrices | MarketDate | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InventoryPrices]
(
[MarketDate] [datetime] NOT NULL,
[HighGravityOilPlatts] [numeric] (18, 4) NULL,
[HighGravityOilNymex] [numeric] (18, 4) NULL,
[FuelOilPlatts] [numeric] (18, 2) NULL,
[FeedStockOilPlatts] [numeric] (18, 2) NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[InventoryPrices] ADD CONSTRAINT [PK_InventoryPrices] PRIMARY KEY CLUSTERED ([MarketDate]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

