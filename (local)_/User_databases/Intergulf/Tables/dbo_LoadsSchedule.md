#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsSchedule

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsSchedule]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 61180 |
| Created | 10:28:39 PM Monday, February 1, 2016 |
| Last Modified | 3:58:21 PM Tuesday, February 5, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsSchedule: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_2_1](../../../../Images/Index.png)](#indexes)(2) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K2, _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_2_1, _dta_stat_1332199796_2_3_25, _dta_stat_1332199796_2_24_25, _dta_stat_1332199796_13_2_3, _dta_stat_1332199796_13_2_24, _dta_stat_1332199796_3_25_13_2_4, _dta_stat_1332199796_24_25_13_2_14_15](../../../../Images/Index.png)](#indexes)(9) | LoadId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_2_3_25, _dta_stat_1332199796_13_2_3, _dta_stat_1332199796_3_25_13_2_4, _dta_stat_1332199796_4_25_3](../../../../Images/Index.png)](#indexes)(5) | ScheduledDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_3_25_13_2_4, _dta_stat_1332199796_4_25_3](../../../../Images/Index.png)](#indexes)(3) | ScheduledTime | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | ScheduledTimeUnits | int | 4 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | StartDateTime | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | EndDateTime | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | ArrivalDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | ArrivalTime | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | LabCheckInDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | LabCheckInTime | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | RackNo | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_13_2_3, _dta_stat_1332199796_13_2_24, _dta_stat_1332199796_3_25_13_2_4, _dta_stat_1332199796_24_25_13_2_14_15](../../../../Images/Index.png)](#indexes)(5) | PumpNo | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_14_15_25_24, _dta_stat_1332199796_24_25_13_2_14_15](../../../../Images/Index.png)](#indexes)(3) | PadStartDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_14_15_25_24, _dta_stat_1332199796_24_25_13_2_14_15](../../../../Images/Index.png)](#indexes)(3) | PadStartTime | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | PadStopDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | PadStopTime | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | PumpStartDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | PumpStartTime | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | PumpStopDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | PumpStopTime | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | LabCheckOutDate | date | 3 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | LabCheckOutTime | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_2_24_25, _dta_stat_1332199796_14_15_25_24, _dta_stat_1332199796_13_2_24, _dta_stat_1332199796_24_25_13_2_14_15](../../../../Images/Index.png)](#indexes)(5) | Status | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_, _dta_stat_1332199796_2_3_25, _dta_stat_1332199796_2_24_25, _dta_stat_1332199796_14_15_25_24, _dta_stat_1332199796_3_25_13_2_4, _dta_stat_1332199796_4_25_3, _dta_stat_1332199796_24_25_13_2_14_15](../../../../Images/Index.png)](#indexes)(7) | OverRideStatus | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | CreateUser | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | CreateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | CreateComputer | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | UpdateUser | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | UpdateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | ScheduledStartDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | ScheduledEndDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_](../../../../Images/Index.png)](#indexes) | ActualPumpNo | varchar(50) | 50 | NULL allowed |  |
|  | CompleteDate | date | 3 | NULL allowed |  |
|  | CompleteTime | varchar(5) | 5 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsSchedule: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsSchedule | Id |  | YES |
|  | _dta_index_LoadsSchedule_5_1332199796__K2 | LoadId |  |  |
|  | _dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_ | ScheduledDate, ScheduledTime, OverRideStatus | ScheduledEndDateTime, ActualPumpNo, CreateDateTime, CreateComputer, UpdateUser, UpdateDateTime, UpdateComputer, ScheduledStartDateTime, PumpStopDate, PumpStopTime, LabCheckOutDate, LabCheckOutTime, Status, CreateUser, PadStartDate, PadStartTime, PadStopDate, PadStopTime, PumpStartDate, PumpStartTime, ArrivalDate, ArrivalTime, LabCheckInDate, LabCheckInTime, RackNo, PumpNo, Id, LoadId, ScheduledTimeUnits, StartDateTime, EndDateTime |  |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_1332199796_13_2_24 | PumpNo, LoadId, Status |
| _dta_stat_1332199796_13_2_3 | PumpNo, LoadId, ScheduledDate |
| _dta_stat_1332199796_14_15_25_24 | PadStartDate, PadStartTime, OverRideStatus, Status |
| _dta_stat_1332199796_24_25_13_2_14_15 | Status, OverRideStatus, PumpNo, LoadId, PadStartDate, PadStartTime |
| _dta_stat_1332199796_2_1 | LoadId, Id |
| _dta_stat_1332199796_2_24_25 | LoadId, Status, OverRideStatus |
| _dta_stat_1332199796_2_3_25 | LoadId, ScheduledDate, OverRideStatus |
| _dta_stat_1332199796_3_25_13_2_4 | ScheduledDate, OverRideStatus, PumpNo, LoadId, ScheduledTime |
| _dta_stat_1332199796_4_25_3 | ScheduledTime, OverRideStatus, ScheduledDate |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsSchedule]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[LoadId] [bigint] NULL,
[ScheduledDate] [date] NULL,
[ScheduledTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ScheduledTimeUnits] [int] NULL,
[StartDateTime] [bigint] NULL,
[EndDateTime] [bigint] NULL,
[ArrivalDate] [date] NULL,
[ArrivalTime] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LabCheckInDate] [date] NULL,
[LabCheckInTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[RackNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PumpNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PadStartDate] [date] NULL,
[PadStartTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PadStopDate] [date] NULL,
[PadStopTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PumpStartDate] [date] NULL,
[PumpStartTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PumpStopDate] [date] NULL,
[PumpStopTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LabCheckOutDate] [date] NULL,
[LabCheckOutTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OverRideStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ScheduledStartDateTime] [datetime] NULL,
[ScheduledEndDateTime] [datetime] NULL,
[ActualPumpNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CompleteDate] [date] NULL,
[CompleteTime] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsSchedule] ADD CONSTRAINT [PK_LoadsSchedule] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LoadsSchedule_5_1332199796__K2] ON [dbo].[LoadsSchedule] ([LoadId]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LoadsSchedule_5_1332199796__K3_K4_K25_1_2_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_26_27_28_29_30_31_] ON [dbo].[LoadsSchedule] ([ScheduledDate], [ScheduledTime], [OverRideStatus]) INCLUDE ([Id], [LoadId], [ScheduledTimeUnits], [StartDateTime], [EndDateTime], [ArrivalDate], [ArrivalTime], [LabCheckInDate], [LabCheckInTime], [RackNo], [PumpNo], [PadStartDate], [PadStartTime], [PadStopDate], [PadStopTime], [PumpStartDate], [PumpStartTime], [PumpStopDate], [PumpStopTime], [LabCheckOutDate], [LabCheckOutTime], [Status], [CreateUser], [CreateDateTime], [CreateComputer], [UpdateUser], [UpdateDateTime], [UpdateComputer], [ScheduledStartDateTime], [ScheduledEndDateTime], [ActualPumpNo]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_1332199796_2_1] ON [dbo].[LoadsSchedule] ([LoadId], [Id])
GO
CREATE STATISTICS [_dta_stat_1332199796_2_3_25] ON [dbo].[LoadsSchedule] ([LoadId], [ScheduledDate], [OverRideStatus])
GO
CREATE STATISTICS [_dta_stat_1332199796_2_24_25] ON [dbo].[LoadsSchedule] ([LoadId], [Status], [OverRideStatus])
GO
CREATE STATISTICS [_dta_stat_1332199796_14_15_25_24] ON [dbo].[LoadsSchedule] ([PadStartDate], [PadStartTime], [OverRideStatus], [Status])
GO
CREATE STATISTICS [_dta_stat_1332199796_13_2_3] ON [dbo].[LoadsSchedule] ([PumpNo], [LoadId], [ScheduledDate])
GO
CREATE STATISTICS [_dta_stat_1332199796_13_2_24] ON [dbo].[LoadsSchedule] ([PumpNo], [LoadId], [Status])
GO
CREATE STATISTICS [_dta_stat_1332199796_3_25_13_2_4] ON [dbo].[LoadsSchedule] ([ScheduledDate], [OverRideStatus], [PumpNo], [LoadId], [ScheduledTime])
GO
CREATE STATISTICS [_dta_stat_1332199796_4_25_3] ON [dbo].[LoadsSchedule] ([ScheduledTime], [OverRideStatus], [ScheduledDate])
GO
CREATE STATISTICS [_dta_stat_1332199796_24_25_13_2_14_15] ON [dbo].[LoadsSchedule] ([Status], [OverRideStatus], [PumpNo], [LoadId], [PadStartDate], [PadStartTime])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadScheduleByPump]](../Views/dbo_vwRptLoadScheduleByPump.md)
* [[dbo].[vwRptSelectSchedulePumpTimes]](../Views/dbo_vwRptSelectSchedulePumpTimes.md)
* [[dbo].[vwRptSelectScheduleTimes]](../Views/dbo_vwRptSelectScheduleTimes.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectLoadPadTimesForExport]](../Views/dbo_vwSelectLoadPadTimesForExport.md)
* [[dbo].[vwSelectLoadsFor225ByMonth]](../Views/dbo_vwSelectLoadsFor225ByMonth.md)
* [[dbo].[vwSelectLoadsScheduleCreateUser]](../Views/dbo_vwSelectLoadsScheduleCreateUser.md)
* [[dbo].[vwSelectLoadsScheduled]](../Views/dbo_vwSelectLoadsScheduled.md)
* [[dbo].[vwSelectLoadsScheduledForChart]](../Views/dbo_vwSelectLoadsScheduledForChart.md)
* [[dbo].[vwSelectLoadsScheduledLoad]](../Views/dbo_vwSelectLoadsScheduledLoad.md)
* [[dbo].[vwSelectLoadsScheduleForCliff]](../Views/dbo_vwSelectLoadsScheduleForCliff.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

