#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsWithProfileExpDateToMarkInactive

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsWithProfileExpDateToMarkInactive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:44:18 PM Tuesday, May 1, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| SchYear | int | 4 |
| ProfileId | bigint | 8 |
| ProfileNumber | varchar(50) | 50 |
| ExpDate | datetime | 8 |
| ExpYear | int | 4 |
| ProfileType | varchar(50) | 50 |
| Status | varchar(20) | 20 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsWithProfileExpDateToMarkInactive]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Loads.ScheduledDate, YEAR(dbo.Loads.ScheduledDate) AS SchYear, dbo.Loads.ProfileId, 
                      dbo.Profile.ProfileNumber, dbo.Profile.EffectiveDate AS ExpDate, YEAR(dbo.Profile.EffectiveDate) AS ExpYear, dbo.Profile.ProfileType, 
                      dbo.Profile.Status
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE     (dbo.Profile.ProfileType = 'Waste') AND (dbo.Profile.Status = 'Active') AND (YEAR(dbo.Profile.EffectiveDate) <= 2011)
ORDER BY dbo.Loads.ProfileId, dbo.Loads.ScheduledDate DESC

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

