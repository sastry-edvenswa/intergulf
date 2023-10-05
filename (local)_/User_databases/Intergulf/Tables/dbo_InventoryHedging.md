#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.InventoryHedging

# ![Tables](../../../../Images/Table32.png) [dbo].[InventoryHedging]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Heap | YES |
| Row Count (~) | 287 |
| Created | 12:23:23 PM Thursday, February 21, 2008 |
| Last Modified | 12:23:23 PM Thursday, February 21, 2008 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| Id | bigint | 8 | NOT NULL | 1 - 1 |
| Category | varchar(50) | 50 | NULL allowed |  |
| ExposureDate | datetime | 8 | NULL allowed |  |
| HedgeValue | decimal(19,0) | 9 | NULL allowed |  |
| HedgeQuantity | decimal(18,0) | 9 | NULL allowed |  |
| TransType | varchar(50) | 50 | NULL allowed |  |
| TransDate | datetime | 8 | NULL allowed |  |
| UpdateUser | varchar(50) | 50 | NULL allowed |  |
| UpdateDateTime | datetime | 8 | NULL allowed |  |
| UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[InventoryHedging]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[Category] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExposureDate] [datetime] NULL,
[HedgeValue] [decimal] (19, 0) NULL,
[HedgeQuantity] [decimal] (18, 0) NULL,
[TransType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransDate] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

