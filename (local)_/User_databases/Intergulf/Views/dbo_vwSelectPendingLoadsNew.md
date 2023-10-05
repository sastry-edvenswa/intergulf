#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectPendingLoadsNew

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectPendingLoadsNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:37:41 PM Saturday, February 10, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileId | bigint | 8 |
| Profile Number | varchar(50) | 50 |
| LoadType | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ActualDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| ActualTime | datetime | 8 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| CustomerId | bigint | 8 |
| VendorId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| DispatchStatus | varchar(50) | 50 |
| ContactName | varchar(100) | 100 |
| ContactPhone | varchar(50) | 50 |
| PickupLocation | varchar(200) | 200 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectPendingLoadsNew]
AS
SELECT     TOP 100 PERCENT fnSelectLoads.Id, fnSelectLoads.ProfileId, fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectLoads.LoadType, 
                      fnSelectLoads.ScheduledDate, fnSelectLoads.ActualDate, fnSelectLoads.ScheduledTime, fnSelectLoads.ActualTime, 
                      fnSelectDriver.FirstName AS [Driver First Name], fnSelectDriver.LastName AS [Driver Last Name], fnSelectProfile.ProfileType, 
                      fnSelectLoads.CustomerId, fnSelectLoads.VendorId, fnSelectGenerator.Name AS [Generator Name], fnSelectLoads.DispatchStatus, 
                      fnSelectLoads.ContactName, fnSelectLoads.ContactPhone, fnSelectLoads.PickupLocation
FROM         dbo.fnSelectProfile() fnSelectProfile INNER JOIN
                      dbo.fnSelectGenerator() fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id RIGHT OUTER JOIN
                      dbo.fnSelectLoads() fnSelectLoads ON fnSelectProfile.Id = fnSelectLoads.ProfileId LEFT OUTER JOIN
                      dbo.fnSelectDriver() fnSelectDriver ON fnSelectLoads.DriverId = fnSelectDriver.Id
WHERE     (fnSelectLoads.DispatchStatus = 'Pending')
ORDER BY fnSelectLoads.ScheduledDate, fnSelectLoads.ScheduledTime
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

