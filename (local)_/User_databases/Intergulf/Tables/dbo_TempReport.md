#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.TempReport

# ![Tables](../../../../Images/Table32.png) [dbo].[TempReport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 27 |
| Created | 10:27:52 AM Friday, May 8, 2009 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_TempReport: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | ReportName | varchar(50) | 50 | NULL allowed |  |
|  | UserName | varchar(50) | 50 | NULL allowed |  |
|  | Tank | varchar(50) | 50 | NULL allowed |  |
|  | LoadTank | varchar(50) | 50 | NULL allowed |  |
|  | LoadNo | varchar(50) | 50 | NULL allowed |  |
|  | Transporter | varchar(50) | 50 | NULL allowed |  |
|  | LoadDate | varchar(50) | 50 | NULL allowed |  |
|  | Truck | varchar(50) | 50 | NULL allowed |  |
|  | GeneratorName | varchar(200) | 200 | NULL allowed |  |
|  | TruckTime | varchar(50) | 50 | NULL allowed |  |
|  | TruckRate | varchar(50) | 50 | NULL allowed |  |
|  | TotalCharge | varchar(50) | 50 | NULL allowed |  |
|  | DispatchStatus | varchar(50) | 50 | NULL allowed |  |
|  | BillingDepartment | varchar(50) | 50 | NULL allowed |  |
|  | BillingStatus | varchar(50) | 50 | NULL allowed |  |
|  | VesselTank | varchar(50) | 50 | NULL allowed |  |
|  | SalesId | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_TempReport: Id](../../../../Images/pkcluster.png)](#indexes) | PK_TempReport | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[TempReport]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[ReportName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Tank] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LoadTank] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LoadNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Transporter] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LoadDate] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Truck] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GeneratorName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TruckTime] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TruckRate] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TotalCharge] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DispatchStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingDepartment] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[VesselTank] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SalesId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[TempReport] ADD CONSTRAINT [PK_TempReport] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

