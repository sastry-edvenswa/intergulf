#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectTrailerLastLoad

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectTrailerLastLoad]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:59:50 AM Monday, June 12, 2017 |
| Last Modified | 11:59:50 AM Monday, June 12, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Load No | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| Trailer No | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectTrailerLastLoad]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id AS [Load No], dbo.Generator.Name AS [Generator Name], dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, 
                         dbo.Equipment.Id AS [Trailer No], dbo.Equipment.Description, dbo.Loads.DispatchStatus
FROM            dbo.Equipment INNER JOIN
                         dbo.Loads ON dbo.Equipment.Id = dbo.Loads.TrailerId LEFT OUTER JOIN
                         dbo.Generator RIGHT OUTER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
ORDER BY [Load No] DESC

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

