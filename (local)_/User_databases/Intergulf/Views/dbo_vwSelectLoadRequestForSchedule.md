#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadRequestForSchedule

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadRequestForSchedule]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:04:06 PM Tuesday, January 30, 2018 |
| Last Modified | 10:04:06 PM Tuesday, January 30, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadRequestNo | bigint | 8 |
| Generator | varchar(100) | 100 |
| ProfileNo | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| SpecialRequirements | varchar(3000) | 3000 |
| LoadRequestDate | datetime | 8 |
| LoadRequestTime | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadRequestForSchedule]
AS
SELECT        dbo.LoadRequest.Id AS LoadRequestNo, dbo.Generator.Name AS Generator, dbo.Profile.ProfileNumber AS ProfileNo, dbo.Profile.Direction, dbo.Profile.ProfileType, 
                         dbo.LoadRequest.VesselTank, dbo.Destination.Name AS Destination, dbo.LoadRequest.SpecialRequirements, dbo.LoadRequest.LoadRequestDate, 
                         dbo.LoadRequest.LoadRequestTime, dbo.Profile.MaterialDescription
FROM            dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId RIGHT OUTER JOIN
                         dbo.LoadRequest LEFT OUTER JOIN
                         dbo.Destination ON dbo.LoadRequest.DestinationId = dbo.Destination.Id ON dbo.Profile.Id = dbo.LoadRequest.ProfileId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

