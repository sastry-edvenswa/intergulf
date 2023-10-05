#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Product

# ![Tables](../../../../Images/Table32.png) [dbo].[Product]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 427 |
| Created | 1:45:43 PM Thursday, September 29, 2022 |
| Last Modified | 1:10:27 PM Monday, October 3, 2022 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Product: Product](../../../../Images/pkcluster.png)](#indexes) | Product | varchar(10) | 10 | NOT NULL |
|  | Description | varchar(500) | 500 | NULL allowed |
|  | Inventry | bit | 1 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Product: Product](../../../../Images/pkcluster.png)](#indexes) | PK_Product | Product | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Product]
(
[Product] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Description] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Inventry] [bit] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Product] ADD CONSTRAINT [PK_Product] PRIMARY KEY CLUSTERED ([Product]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSaturnTestProduct]](../Views/dbo_vwSaturnTestProduct.md)
* [[dbo].[vwSelectProductForSaturn]](../Views/dbo_vwSelectProductForSaturn.md)
* [[dbo].[vwSelectProducts]](../Views/dbo_vwSelectProducts.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

