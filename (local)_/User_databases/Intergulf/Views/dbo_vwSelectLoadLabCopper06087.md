#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadLabCopper06087

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadLabCopper06087]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:25:46 PM Friday, December 5, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| ProfileNumber | varchar(50) | 50 |
| AqueousCopper | decimal(18,0) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadLabCopper06087]
AS
SELECT     dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Profile.ProfileNumber, dbo.LabTest.AqueousCopper
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id
WHERE     (dbo.Profile.ProfileNumber = '06087') AND (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2014-10-22 00:00:00', 102))

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

