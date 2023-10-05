#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.FuelSurCharge

# ![Tables](../../../../Images/Table32.png) [dbo].[FuelSurCharge]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 0 |
| Created | 1:44:21 PM Sunday, August 28, 2022 |
| Last Modified | 1:47:03 PM Sunday, August 28, 2022 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_FuelSurChargefuel surcharge: Year\Week](../../../../Images/pkcluster.png)](#indexes) | Year | int | 4 | NOT NULL |
| [![Cluster Primary Key PK_FuelSurChargefuel surcharge: Year\Week](../../../../Images/pkcluster.png)](#indexes) | Week | int | 4 | NOT NULL |
|  | FirstDayOfWeek | date | 3 | NULL allowed |
|  | LastDayOfWeek | date | 3 | NULL allowed |
|  | FuelSurcharge | numeric(18,2) | 9 | NULL allowed |
|  | CreateUser | varchar(50) | 50 | NULL allowed |
|  | CreateDateTime | datetime | 8 | NULL allowed |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_FuelSurChargefuel surcharge: Year\Week](../../../../Images/pkcluster.png)](#indexes) | PK_FuelSurChargefuel surcharge | Year, Week | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[FuelSurCharge]
(
[Year] [int] NOT NULL,
[Week] [int] NOT NULL,
[FirstDayOfWeek] [date] NULL,
[LastDayOfWeek] [date] NULL,
[FuelSurcharge] [numeric] (18, 2) NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[FuelSurCharge] ADD CONSTRAINT [PK_FuelSurChargefuel surcharge] PRIMARY KEY CLUSTERED ([Year], [Week]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

