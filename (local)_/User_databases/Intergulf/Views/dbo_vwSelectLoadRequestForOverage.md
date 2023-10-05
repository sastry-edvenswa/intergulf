#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadRequestForOverage

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadRequestForOverage]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:25:25 PM Wednesday, May 24, 2023 |
| Last Modified | 7:15:41 PM Wednesday, June 7, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| LoadRequestDate | datetime | 8 |
| GeneratorName | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| CSRPersonId | varchar(50) | 50 |
| LRNoLoads | decimal(18,0) | 9 |
| Processed | int | 4 |
| LNoLoads | int | 4 |
| OAEmailDateTime | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadRequestForOverage]
AS
SELECT        TOP (100) PERCENT dbo.LoadRequest.Id, dbo.LoadRequest.LoadRequestDate, dbo.Generator.Name AS GeneratorName, dbo.Profile.ProfileNumber, dbo.Profile.SalesPersonId, dbo.Profile.CSRPersonId, 
                         dbo.LoadRequest.NoLoads AS LRNoLoads, dbo.LoadRequest.Processed,
                             (SELECT        COUNT(1) AS LoadCount
                               FROM            dbo.Loads
                               WHERE        (LoadRequestId = dbo.LoadRequest.Id)) AS LNoLoads, dbo.LoadRequest.OAEmailDateTime
FROM            dbo.Generator RIGHT OUTER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId RIGHT OUTER JOIN
                         dbo.LoadRequest ON dbo.Profile.Id = dbo.LoadRequest.ProfileId
WHERE        (dbo.LoadRequest.Processed <> 1) OR
                         (dbo.LoadRequest.Processed IS NULL)
ORDER BY dbo.LoadRequest.LoadRequestDate
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

