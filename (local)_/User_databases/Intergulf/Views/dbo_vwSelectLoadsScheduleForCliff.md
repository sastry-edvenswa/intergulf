#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsScheduleForCliff

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsScheduleForCliff]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 6:59:49 PM Friday, July 28, 2017 |
| Last Modified | 6:59:49 PM Friday, July 28, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| LoadId | bigint | 8 |  |
| ScheduledDate | date | 3 |  |
| ScheduledTime | varchar(5) | 5 |  |
| Status | varchar(50) | 50 |  |
| CreateUser | varchar(50) | 50 |  |
| CreateDateTime | datetime | 8 |  |
| UpdateUser | varchar(50) | 50 |  |
| UpdateDateTime | datetime | 8 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsScheduleForCliff]
AS
SELECT        TOP (100) PERCENT Id, LoadId, ScheduledDate, ScheduledTime, Status, CreateUser, CreateDateTime, UpdateUser, UpdateDateTime
FROM            dbo.LoadsSchedule
WHERE        (LoadId = 224179) OR
                         (LoadId = 244262) OR
                         (LoadId = 244187) OR
                         (LoadId = 244290) OR
                         (LoadId = 244003) OR
                         (LoadId = 244149) OR
                         (LoadId = 244152) OR
                         (LoadId = 244215) OR
                         (LoadId = 244115) OR
                         (LoadId = 244156)
ORDER BY CreateDateTime
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

