#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectLoadsReadyToBill

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectLoadsReadyToBill]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | NO |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET QUOTED_IDENTIFIER OFF
GO
SET ANSI_NULLS OFF
GO

CREATE  FUNCTION [dbo].[fnSelectLoadsReadyToBill]
                 (  )
RETURNS table
AS
RETURN (
SELECT     TOP 100 PERCENT fnSelectLoads.Id, fnSelectProfile.GeneratorId, fnSelectGenerator.Name AS [Generator Name], 
                      fnSelectCustomer.Name AS [Customer Name], fnSelectLoads.ProfileId AS [Profile Number], fnSelectLoads.ScheduledDate, 
                      fnSelectLoads.ScheduledTime, fnSelectLoads.TruckId, fnSelectLoads.ActualDate, fnSelectLoads.ActualTime, 
                      fnSelectDriver.FirstName AS [Driver First Name], fnSelectDriver.LastName AS [Driver Last Name], fnSelectProfile.ProfileType, 
                      fnSelectLoads.DispatchStatus, fnSelectLoads.BillingDepartment, fnSelectLoads.BillingStatus, fnSelectLoads.CustomerId, 
                      fnSelectDestination.Name AS [Destination Name], fnSelectLoads.VesselTank
FROM         dbo.fnSelectDestination() fnSelectDestination RIGHT OUTER JOIN
                      dbo.fnSelectLoads() fnSelectLoads ON fnSelectDestination.Id = fnSelectLoads.DestinationId LEFT OUTER JOIN
                      dbo.fnSelectGenerator() fnSelectGenerator RIGHT OUTER JOIN
                      dbo.fnSelectProfile() fnSelectProfile ON fnSelectGenerator.Id = fnSelectProfile.GeneratorId ON 
                      fnSelectLoads.ProfileId = fnSelectProfile.Id LEFT OUTER JOIN
                      dbo.fnSelectDriver() fnSelectDriver ON fnSelectLoads.DriverId = fnSelectDriver.Id LEFT OUTER JOIN
                      dbo.fnSelectCustomer() fnSelectCustomer ON fnSelectLoads.CustomerId = fnSelectCustomer.Id
ORDER BY fnSelectLoads.ScheduledDate, fnSelectLoads.ScheduledTime, fnSelectLoads.TruckId
       )
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectCustomer]](dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectDestination]](dbo_fnSelectDestination.md)
* [[dbo].[fnSelectDriver]](dbo_fnSelectDriver.md)
* [[dbo].[fnSelectGenerator]](dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLoads]](dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](dbo_fnSelectProfile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

