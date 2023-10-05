#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsBilling

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsBilling]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 235425 |
| Created | 10:51:53 PM Monday, December 17, 2012 |
| Last Modified | 3:58:20 PM Tuesday, February 5, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsBilling: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19, _dta_stat_471672728_2_3](../../../../Images/Index.png)](#indexes)(2) | LoadId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19, _dta_stat_471672728_2_3](../../../../Images/Index.png)](#indexes)(2) | LegNumber | int | 4 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | BeginningDate | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | DriverId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | TruckId | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | TrailerId | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | StartTime | numeric(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | PickupLocationArrivalTime | numeric(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | PickupLocationDepartTime | numeric(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | DeliveryLocationArrivalTime | numeric(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | DeliveryLocationDepartTime | numeric(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | EndTime | numeric(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | CreateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | CreateUser | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | CreateComputer | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | UpdateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | UpdateUser | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19](../../../../Images/Index.png)](#indexes) | UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsBilling: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsBilling | Id |  | YES |
|  | _dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19 | LoadId, LegNumber | Id, BeginningDate, DriverId, TruckId, UpdateComputer, EndTime, CreateDateTime, CreateUser, CreateComputer, UpdateDateTime, UpdateUser, TrailerId, StartTime, PickupLocationArrivalTime, PickupLocationDepartTime, DeliveryLocationArrivalTime, DeliveryLocationDepartTime |  |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_471672728_2_3 | LoadId, LegNumber |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsBilling]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[LoadId] [bigint] NULL,
[LegNumber] [int] NULL,
[BeginningDate] [datetime] NULL,
[DriverId] [bigint] NULL,
[TruckId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TrailerId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[StartTime] [numeric] (18, 2) NULL,
[PickupLocationArrivalTime] [numeric] (18, 2) NULL,
[PickupLocationDepartTime] [numeric] (18, 2) NULL,
[DeliveryLocationArrivalTime] [numeric] (18, 2) NULL,
[DeliveryLocationDepartTime] [numeric] (18, 2) NULL,
[EndTime] [numeric] (18, 2) NULL,
[CreateDateTime] [datetime] NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsBilling] ADD CONSTRAINT [PK_LoadsBilling] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LoadsBilling_5_471672728__K2_K3_1_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19] ON [dbo].[LoadsBilling] ([LoadId], [LegNumber]) INCLUDE ([Id], [BeginningDate], [DriverId], [TruckId], [TrailerId], [StartTime], [PickupLocationArrivalTime], [PickupLocationDepartTime], [DeliveryLocationArrivalTime], [DeliveryLocationDepartTime], [EndTime], [CreateDateTime], [CreateUser], [CreateComputer], [UpdateDateTime], [UpdateUser], [UpdateComputer]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_471672728_2_3] ON [dbo].[LoadsBilling] ([LoadId], [LegNumber])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectExportLoadArrivalTimePerformance]](../Views/dbo_vwSelectExportLoadArrivalTimePerformance.md)
* [[dbo].[vwSelectExportLoadsTruckTimes]](../Views/dbo_vwSelectExportLoadsTruckTimes.md)
* [[dbo].[vwSelectLegOneDriverOnSiteTime]](../Views/dbo_vwSelectLegOneDriverOnSiteTime.md)
* [[dbo].[vwSelectLoadBillingTimes]](../Views/dbo_vwSelectLoadBillingTimes.md)
* [[dbo].[vwSelectLoadsBillingMotiva20121001]](../Views/dbo_vwSelectLoadsBillingMotiva20121001.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

