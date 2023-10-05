#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadRequestLoadTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadRequestLoadTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:54:16 PM Monday, July 1, 2019 |
| Last Modified | 5:05:48 PM Monday, July 1, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LR No | bigint | 8 |
| LR Create Date | varchar(30) | 30 |
| LR Create Time | varchar(30) | 30 |
| LR Date | varchar(30) | 30 |
| LR Time | varchar(30) | 30 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| LR Create User | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| Load No | bigint | 8 |
| Load Salesperson | varchar(50) | 50 |
| Load Create User | varchar(50) | 50 |
| Load Create Date | varchar(30) | 30 |
| Load Create Time | varchar(30) | 30 |
| Load Requested Date | varchar(30) | 30 |
| Load Requested Time | varchar(30) | 30 |
| Load Scheduled Date | varchar(30) | 30 |
| Load Scheduled Time | varchar(30) | 30 |
| CreateDateTime | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadRequestLoadTimes]
AS
SELECT        TOP (100) PERCENT dbo.LoadRequest.Id AS [LR No], CONVERT(varchar, dbo.LoadRequest.CreateDate, 110) AS [LR Create Date], CONVERT(varchar, dbo.LoadRequest.CreateTime, 8) AS [LR Create Time], 
                         CONVERT(varchar, dbo.LoadRequest.LoadRequestDate, 110) AS [LR Date], CONVERT(varchar, dbo.LoadRequest.LoadRequestTime, 8) AS [LR Time], dbo.LoadRequest.UpdateDateTime, 
                         dbo.LoadRequest.UpdateUser, dbo.LoadRequest.CreateUser AS [LR Create User], dbo.LoadRequest.SalesPersonId, dbo.Loads.Id AS [Load No], dbo.Loads.SalesPersonId AS [Load Salesperson], 
                         dbo.Loads.CreateUser AS [Load Create User], CONVERT(varchar, dbo.Loads.CreateDateTime, 110) AS [Load Create Date], CONVERT(varchar, dbo.Loads.CreateDateTime, 8) AS [Load Create Time], 
                         CONVERT(varchar, dbo.Loads.RequestedDate, 110) AS [Load Requested Date], CONVERT(varchar, dbo.Loads.RequestedTime, 8) AS [Load Requested Time], CONVERT(varchar, dbo.Loads.ScheduledDate, 110) 
                         AS [Load Scheduled Date], CONVERT(varchar, dbo.Loads.ScheduledTime, 8) AS [Load Scheduled Time], dbo.Loads.CreateDateTime
FROM            dbo.LoadRequest INNER JOIN
                         dbo.Loads ON dbo.LoadRequest.Id = dbo.Loads.LoadRequestId
WHERE        (dbo.Loads.CreateDateTime > CONVERT(DATETIME, '2019-01-01 00:00:00', 102))
ORDER BY dbo.Loads.CreateDateTime
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

