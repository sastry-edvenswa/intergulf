#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Pumps

# ![Tables](../../../../Images/Table32.png) [dbo].[Pumps]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 19 |
| Created | 4:41:52 PM Monday, January 11, 2016 |
| Last Modified | 10:03:50 PM Tuesday, January 30, 2018 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Pumps: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | Description | varchar(50) | 50 | NULL allowed |  |
|  | Number | bigint | 8 | NULL allowed |  |
|  | SortOrder | bigint | 8 | NULL allowed |  |
|  | Status | nchar(10) | 20 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | ExcludeFromResourceCheck | varchar(3) | 3 | NULL allowed |  |
|  | ExcludeFromReportAverages | varchar(3) | 3 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Pumps: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Pumps | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Pumps]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[Description] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Number] [bigint] NULL,
[SortOrder] [bigint] NULL,
[Status] [nchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExcludeFromResourceCheck] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExcludeFromReportAverages] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Pumps] ADD CONSTRAINT [PK_Pumps] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadScheduleByPump]](../Views/dbo_vwRptLoadScheduleByPump.md)
* [[dbo].[vwRptSelectSchedulePumpTimes]](../Views/dbo_vwRptSelectSchedulePumpTimes.md)
* [[dbo].[vwRptSelectScheduleTimes]](../Views/dbo_vwRptSelectScheduleTimes.md)
* [[dbo].[vwSelectLoadsFor225ByMonth]](../Views/dbo_vwSelectLoadsFor225ByMonth.md)
* [[dbo].[vwSelectLoadsScheduled]](../Views/dbo_vwSelectLoadsScheduled.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

