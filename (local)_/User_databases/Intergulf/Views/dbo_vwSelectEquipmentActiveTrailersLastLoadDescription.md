#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectEquipmentActiveTrailersLastLoadDescription

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectEquipmentActiveTrailersLastLoadDescription]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:00:43 PM Wednesday, March 28, 2018 |
| Last Modified | 4:32:34 PM Friday, February 1, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Status | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| Location | varchar(50) | 50 |
| LocationStatus | varchar(50) | 50 |
| Scheduled | varchar(3) | 3 |
| Planned | varchar(3) | 3 |
| Loaded | varchar(3) | 3 |
| TrailerCustomerDescription | varchar(100) | 100 |
| Insulated | varchar(25) | 25 |
| VaporRecovery | varchar(3) | 3 |
| DryBreak | varchar(3) | 3 |
| BellyRear | varchar(25) | 25 |
| MaxTemp | varchar(10) | 10 |
| LastLocationStatus | varchar(50) | 50 |
| TrailerLastLoadDescription | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectEquipmentActiveTrailersLastLoadDescription]
AS
SELECT        TOP (100) PERCENT dbo.Equipment.Id, dbo.Equipment.Description, dbo.Equipment.Type, dbo.Equipment.TrailerId, dbo.Equipment.Status, dbo.Driver.FirstName, dbo.Driver.LastName, dbo.Equipment.Location, 
                         dbo.Equipment.LocationStatus, dbo.fnIsTrailerScheduled(dbo.Equipment.Id) AS Scheduled, dbo.fnIsTrailerPlanned(dbo.Equipment.Id) AS Planned, dbo.fnIsTrailerLoaded(dbo.Equipment.Id) AS Loaded, 
                         dbo.Equipment.TrailerCustomerDescription, dbo.Equipment.Insulated, dbo.Equipment.VaporRecovery, dbo.Equipment.DryBreak, dbo.Equipment.BellyRear, dbo.Equipment.MaxTemp, 
                         dbo.Equipment.LastLocationStatus, dbo.Equipment.Id AS TrailerLastLoadDescription
FROM            dbo.Equipment LEFT OUTER JOIN
                         dbo.Driver ON dbo.Equipment.DriverId = dbo.Driver.Id
GROUP BY dbo.Equipment.Id, dbo.Equipment.Description, dbo.Equipment.Type, dbo.Equipment.TrailerId, dbo.Equipment.Status, dbo.Driver.FirstName, dbo.Driver.LastName, dbo.Equipment.Location, 
                         dbo.Equipment.LocationStatus, dbo.fnIsTrailerScheduled(dbo.Equipment.Id), LEN(dbo.Equipment.Id), dbo.fnIsTrailerPlanned(dbo.Equipment.Id), dbo.fnIsTrailerLoaded(dbo.Equipment.Id), 
                         dbo.Equipment.TrailerCustomerDescription, dbo.Equipment.Insulated, dbo.Equipment.VaporRecovery, dbo.Equipment.DryBreak, dbo.Equipment.BellyRear, dbo.Equipment.MaxTemp, 
                         dbo.Equipment.LastLocationStatus
HAVING        (dbo.Equipment.Type = 'Trailer') AND (dbo.Equipment.Status = 'Active')
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

