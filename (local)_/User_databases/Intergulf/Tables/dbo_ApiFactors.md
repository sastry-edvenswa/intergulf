#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ApiFactors

# ![Tables](../../../../Images/Table32.png) [dbo].[ApiFactors]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Row Count (~) | 851 |
| Created | 3:52:58 PM Tuesday, June 19, 2007 |
| Last Modified | 11:50:34 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK__ApiFactors__345EC57D: Api](../../../../Images/pkcluster.png)](#indexes) | Api | numeric(18,2) | 9 | NOT NULL |
|  | LbsFactor | numeric(18,3) | 9 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK__ApiFactors__345EC57D: Api](../../../../Images/pkcluster.png)](#indexes) | PK__ApiFactors__345EC57D | Api | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ApiFactors]
(
[Api] [numeric] (18, 2) NOT NULL,
[LbsFactor] [numeric] (18, 3) NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ApiFactors] ADD CONSTRAINT [PK__ApiFactors__345EC57D] PRIMARY KEY CLUSTERED ([Api]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

