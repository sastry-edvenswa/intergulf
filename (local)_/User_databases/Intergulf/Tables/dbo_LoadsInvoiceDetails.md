#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsInvoiceDetails

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsInvoiceDetails]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 0 |
| Created | 6:45:25 PM Sunday, September 23, 2018 |
| Last Modified | 6:45:25 PM Sunday, September 23, 2018 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsInvoiceDetails: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL |
|  | LoadId | bigint | 8 | NULL allowed |
|  | LineOrder | bigint | 8 | NULL allowed |
|  | SageCode | varchar(50) | 50 | NULL allowed |
|  | Price | numeric(18,2) | 9 | NULL allowed |
|  | Quanitiy | numeric(18,0) | 9 | NULL allowed |
|  | Unit | varchar(50) | 50 | NULL allowed |
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
| [![Cluster Primary Key PK_LoadsInvoiceDetails: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsInvoiceDetails | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsInvoiceDetails]
(
[Id] [bigint] NOT NULL,
[LoadId] [bigint] NULL,
[LineOrder] [bigint] NULL,
[SageCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Price] [numeric] (18, 2) NULL,
[Quanitiy] [numeric] (18, 0) NULL,
[Unit] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsInvoiceDetails] ADD CONSTRAINT [PK_LoadsInvoiceDetails] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

