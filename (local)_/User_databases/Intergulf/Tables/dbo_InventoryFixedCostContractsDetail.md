#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InventoryFixedCostContractsDetail

# ![Tables](../../../../Images/Table32.png) [dbo].[InventoryFixedCostContractsDetail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 0 |
| Created | 8:59:40 PM Tuesday, August 12, 2008 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_InventoryFixedCostContractsDetail: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | ContractId | bigint | 8 | NULL allowed |  |
|  | ExposureDate | datetime | 8 | NULL allowed |  |
|  | Quantity | bigint | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | Comments | varchar(200) | 200 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_InventoryFixedCostContractsDetail: Id](../../../../Images/pkcluster.png)](#indexes) | PK_InventoryFixedCostContractsDetail | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InventoryFixedCostContractsDetail]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ContractId] [bigint] NULL,
[ExposureDate] [datetime] NULL,
[Quantity] [bigint] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Comments] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[InventoryFixedCostContractsDetail] ADD CONSTRAINT [PK_InventoryFixedCostContractsDetail] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectInventoryFixedCostContractsDetailActive]](../Views/dbo_vwSelectInventoryFixedCostContractsDetailActive.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

