#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectEquipmentNotInUse

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectEquipmentNotInUse]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:42:35 PM Wednesday, August 16, 2017 |
| Last Modified | 2:42:35 PM Wednesday, August 16, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | varchar(50) | 50 |
| Location | varchar(50) | 50 |
| LocationStatus | varchar(50) | 50 |
| Scheduled | varchar(3) | 3 |
| Planned | varchar(3) | 3 |
| Loaded | varchar(3) | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectEquipmentNotInUse]
AS
SELECT        TOP (100) PERCENT dbo.Equipment.Id, dbo.Equipment.Location, dbo.Equipment.LocationStatus, dbo.fnIsTrailerScheduled(dbo.Equipment.Id) AS Scheduled, 
                         dbo.fnIsTrailerPlanned(dbo.Equipment.Id) AS Planned, dbo.fnIsTrailerLoaded(dbo.Equipment.Id) AS Loaded
FROM            dbo.Equipment LEFT OUTER JOIN
                         dbo.Driver ON dbo.Equipment.DriverId = dbo.Driver.Id
GROUP BY dbo.Equipment.Id, dbo.Equipment.Type, dbo.Equipment.Status, dbo.Equipment.Location, dbo.Equipment.LocationStatus, dbo.fnIsTrailerScheduled(dbo.Equipment.Id), 
                         LEN(dbo.Equipment.Id), dbo.fnIsTrailerPlanned(dbo.Equipment.Id), dbo.fnIsTrailerLoaded(dbo.Equipment.Id)
HAVING        (dbo.Equipment.Type = 'Trailer') AND (dbo.Equipment.Status = 'Active') AND (dbo.fnIsTrailerScheduled(dbo.Equipment.Id) = 'No') AND 
                         (dbo.fnIsTrailerPlanned(dbo.Equipment.Id) = 'No') AND (dbo.fnIsTrailerLoaded(dbo.Equipment.Id) = 'No')
ORDER BY Scheduled DESC, dbo.Equipment.Location, LEN(dbo.Equipment.Id), dbo.Equipment.Id, dbo.Equipment.LocationStatus

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[fnIsTrailerLoaded]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnIsTrailerLoaded.md)
* [[dbo].[fnIsTrailerPlanned]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnIsTrailerPlanned.md)
* [[dbo].[fnIsTrailerScheduled]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnIsTrailerScheduled.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

