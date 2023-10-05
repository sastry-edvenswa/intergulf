#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InventoryRailCarContractsDetail

# ![Tables](../../../../Images/Table32.png) [dbo].[InventoryRailCarContractsDetail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 50 |
| Created | 9:00:11 PM Tuesday, August 12, 2008 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_InventoryContractDetail: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | ContractId | bigint | 8 | NULL allowed |  |
|  | CarNumber | varchar(50) | 50 | NULL allowed |  |
|  | BolNumber | varchar(50) | 50 | NULL allowed |  |
|  | Shipper | varchar(50) | 50 | NULL allowed |  |
|  | ShipDate | datetime | 8 | NULL allowed |  |
|  | ETADate | datetime | 8 | NULL allowed |  |
|  | ArriveDate | datetime | 8 | NULL allowed |  |
|  | CallInDate | datetime | 8 | NULL allowed |  |
|  | SpotDate | datetime | 8 | NULL allowed |  |
|  | DischargeDate | datetime | 8 | NULL allowed |  |
|  | ReleaseDate | datetime | 8 | NULL allowed |  |
|  | Quantity | bigint | 8 | NULL allowed |  |
|  | ActQuantity | bigint | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | Comments | varchar(600) | 600 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InventoryContractDetail: Id](../../../../Images/pkcluster.png)](#indexes) | PK_InventoryContractDetail | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InventoryRailCarContractsDetail]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ContractId] [bigint] NULL,
[CarNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BolNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Shipper] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ShipDate] [datetime] NULL,
[ETADate] [datetime] NULL,
[ArriveDate] [datetime] NULL,
[CallInDate] [datetime] NULL,
[SpotDate] [datetime] NULL,
[DischargeDate] [datetime] NULL,
[ReleaseDate] [datetime] NULL,
[Quantity] [bigint] NULL,
[ActQuantity] [bigint] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Comments] [varchar] (600) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[InventoryRailCarContractsDetail] ADD CONSTRAINT [PK_InventoryContractDetail] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectInventoryRailCarContractsDetail]](../Views/dbo_vwSelectInventoryRailCarContractsDetail.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

