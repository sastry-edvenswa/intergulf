#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectReadyToBillLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectReadyToBillLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:49:36 PM Wednesday, August 20, 2008 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| GeneratorId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| Profile Number | bigint | 8 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| TruckId | varchar(50) | 50 |
| ActualDate | datetime | 8 |
| ActualTime | datetime | 8 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| CustomerId | bigint | 8 |
| Destination Name | nvarchar(100) | 200 |
| VesselTank | varchar(100) | 100 |
| TransporterId | numeric(19,0) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectReadyToBillLoads]
AS
SELECT     TOP 100 PERCENT fnSelectLoads.Id, fnSelectProfile.GeneratorId, fnSelectGenerator.Name AS [Generator Name], 
                      fnSelectCustomer.Name AS [Customer Name], fnSelectLoads.ProfileId AS [Profile Number], fnSelectLoads.ScheduledDate, 
                      fnSelectLoads.ScheduledTime, fnSelectLoads.TruckId, fnSelectLoads.ActualDate, fnSelectLoads.ActualTime, 
                      fnSelectDriver.FirstName AS [Driver First Name], fnSelectDriver.LastName AS [Driver Last Name], fnSelectProfile.ProfileType, 
                      fnSelectLoads.DispatchStatus, fnSelectLoads.BillingDepartment, fnSelectLoads.BillingStatus, fnSelectLoads.CustomerId, 
                      fnSelectDestination.Name AS [Destination Name], fnSelectLoads.VesselTank, fnSelectTransporter.Id AS TransporterId
FROM         dbo.fnSelectEquipment() fnSelectEquipment INNER JOIN
                      dbo.fnSelectTransporter() fnSelectTransporter ON fnSelectEquipment.TransporterId = fnSelectTransporter.Id RIGHT OUTER JOIN
                      dbo.fnSelectLoads() fnSelectLoads ON fnSelectEquipment.Id = fnSelectLoads.TruckId LEFT OUTER JOIN
                      dbo.fnSelectDestination() fnSelectDestination ON fnSelectLoads.DestinationId = fnSelectDestination.Id LEFT OUTER JOIN
                      dbo.fnSelectGenerator() fnSelectGenerator RIGHT OUTER JOIN
                      dbo.fnSelectProfile() fnSelectProfile ON fnSelectGenerator.Id = fnSelectProfile.GeneratorId ON 
                      fnSelectLoads.ProfileId = fnSelectProfile.Id LEFT OUTER JOIN
                      dbo.fnSelectDriver() fnSelectDriver ON fnSelectLoads.DriverId = fnSelectDriver.Id LEFT OUTER JOIN
                      dbo.fnSelectCustomer() fnSelectCustomer ON fnSelectLoads.CustomerId = fnSelectCustomer.Id
ORDER BY fnSelectLoads.ScheduledDate, fnSelectLoads.ScheduledTime, fnSelectLoads.TruckId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)
* [[dbo].[fnSelectEquipment]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectEquipment.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)
* [[dbo].[fnSelectTransporter]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectTransporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

