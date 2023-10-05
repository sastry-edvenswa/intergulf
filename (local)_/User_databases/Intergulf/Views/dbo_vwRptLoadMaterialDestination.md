#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadMaterialDestination

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadMaterialDestination]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:49:56 PM Monday, July 16, 2007 |
| Last Modified | 3:36:31 PM Tuesday, March 12, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| Generator Name | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| ProfileNumber | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| Profile Billing Department | varchar(100) | 100 |
| Load Billing Department | varchar(50) | 50 |
| Load Vessel Tank | varchar(100) | 100 |
| Load Tank Number | varchar(50) | 50 |
| LoadType | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadMaterialDestination]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Generator.Name AS [Generator Name], dbo.Destination.Name AS Destination, dbo.Profile.ProfileNumber, dbo.Profile.MaterialDescription, 
                         dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Profile.BillingDepartment AS [Profile Billing Department], dbo.Loads.BillingDepartment AS [Load Billing Department], 
                         dbo.Loads.VesselTank AS [Load Vessel Tank], dbo.Loads.TankNumber AS [Load Tank Number], dbo.Loads.LoadType
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                         dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
ORDER BY Destination, [Generator Name], dbo.Profile.ProfileNumber, dbo.Loads.ScheduledDate
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

