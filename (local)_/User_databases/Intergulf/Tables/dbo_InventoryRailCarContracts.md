#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InventoryRailCarContracts

# ![Tables](../../../../Images/Table32.png) [dbo].[InventoryRailCarContracts]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 9 |
| Created | 8:59:52 PM Tuesday, August 12, 2008 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_InventoryContracts: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | VendorId | bigint | 8 | NULL allowed |  |
|  | SalesPersonId | varchar(50) | 50 | NULL allowed |  |
|  | ExposureDate | datetime | 8 | NULL allowed |  |
|  | Category | varchar(50) | 50 | NULL allowed |  |
|  | Quantity | bigint | 8 | NULL allowed |  |
|  | Type | varchar(50) | 50 | NULL allowed |  |
|  | Product | varchar(50) | 50 | NULL allowed |  |
|  | ActQuantity | bigint | 8 | NULL allowed |  |
|  | MarketCost | numeric(18,4) | 9 | NULL allowed |  |
|  | Comments | varchar(2000) | 2000 | NULL allowed |  |
|  | TransType | varchar(50) | 50 | NULL allowed |  |
|  | TransDate | datetime | 8 | NULL allowed |  |
|  | Status | varchar(10) | 10 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | RefNo | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InventoryContracts: Id](../../../../Images/pkcluster.png)](#indexes) | PK_InventoryContracts | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InventoryRailCarContracts]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[VendorId] [bigint] NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExposureDate] [datetime] NULL,
[Category] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Quantity] [bigint] NULL,
[Type] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Product] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ActQuantity] [bigint] NULL,
[MarketCost] [numeric] (18, 4) NULL,
[Comments] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransDate] [datetime] NULL,
[Status] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[RefNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[InventoryRailCarContracts] ADD CONSTRAINT [PK_InventoryContracts] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectInventoryRailCarContracts]](../Views/dbo_vwSelectInventoryRailCarContracts.md)
* [[dbo].[vwSelectInventoryRailCarContractsDetailActive]](../Views/dbo_vwSelectInventoryRailCarContractsDetailActive.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

