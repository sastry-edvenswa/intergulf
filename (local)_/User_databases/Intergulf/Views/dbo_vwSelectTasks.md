#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectTasks

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectTasks]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:09:40 PM Sunday, September 17, 2017 |
| Last Modified | 10:09:40 PM Sunday, September 17, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| TaskName | varchar(200) | 200 |
| Frequency | varchar(50) | 50 |
| Interval | int | 4 |
| RunDate | date | 3 |
| RunMonth | int | 4 |
| RunWeek | int | 4 |
| RunDay | int | 4 |
| RunHour | int | 4 |
| RunMinute | int | 4 |
| LastRun | varchar(50) | 50 |
| NextRunDate | date | 3 |
| NextRunMonth | int | 4 |
| NextRunWeek | int | 4 |
| NextRunDay | int | 4 |
| NextRunHour | int | 4 |
| NextRunMinute | int | 4 |
| Status | varchar(50) | 50 |
| SortOrder | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectTasks]
AS
SELECT     TOP (100) PERCENT dbo.Tasks.Id, dbo.Tasks.TaskName, dbo.Tasks.Frequency, dbo.Tasks.Interval, dbo.Tasks.RunDate, dbo.Tasks.RunMonth, dbo.Tasks.RunWeek, 
                      dbo.Tasks.RunDay, dbo.Tasks.RunHour, dbo.Tasks.RunMinute, dbo.Tasks.LastRun, dbo.Tasks.NextRunDate, dbo.Tasks.NextRunMonth, dbo.Tasks.NextRunWeek, 
                      dbo.Tasks.NextRunDay, dbo.Tasks.NextRunHour, dbo.Tasks.NextRunMinute, dbo.Tasks.Status, dbo.TaskFrequency.SortOrder
FROM         dbo.Tasks LEFT OUTER JOIN
                      dbo.TaskFrequency ON dbo.Tasks.Frequency = dbo.TaskFrequency.Frequency
ORDER BY dbo.TaskFrequency.SortOrder, dbo.Tasks.TaskName

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[TaskFrequency]](../Tables/dbo_TaskFrequency.md)
* [[dbo].[Tasks]](../Tables/dbo_Tasks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

