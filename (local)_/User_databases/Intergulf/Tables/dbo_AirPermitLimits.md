#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.AirPermitLimits

# ![Tables](../../../../Images/Table32.png) [dbo].[AirPermitLimits]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1 |
| Created | 6:19:50 PM Monday, June 11, 2007 |
| Last Modified | 11:50:34 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK__AirPermitLimits__24285DB4: Id](../../../../Images/pkcluster.png)](#indexes) | Id | varchar(50) | 50 | NOT NULL |
|  | MonthLimit | numeric(13,0) | 9 | NULL allowed |
|  | YearLimit | numeric(13,0) | 9 | NULL allowed |
|  | YearAdjustment | numeric(13,0) | 9 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK__AirPermitLimits__24285DB4: Id](../../../../Images/pkcluster.png)](#indexes) | PK__AirPermitLimits__24285DB4 | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[AirPermitLimits]
(
[Id] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[MonthLimit] [numeric] (13, 0) NULL,
[YearLimit] [numeric] (13, 0) NULL,
[YearAdjustment] [numeric] (13, 0) NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[AirPermitLimits] ADD CONSTRAINT [PK__AirPermitLimits__24285DB4] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

