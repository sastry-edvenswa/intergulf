#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectScheduledLoads

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectScheduledLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET ANSI_NULLS OFF
GO
CREATE FUNCTION [dbo].[fnSelectScheduledLoads]
                 (  )
RETURNS table
AS
RETURN (
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Loads.TruckId, dbo.Loads.ActualDate, 
                      dbo.Loads.ActualTime, dbo.Driver.FirstName AS [Driver First Name], dbo.Driver.LastName AS [Driver Last Name], dbo.Profile.ProfileType, 
                      dbo.Loads.CustomerId, dbo.Loads.VendorId, dbo.Loads.DispatchStatus, dbo.Loads.ContactName, dbo.Loads.ContactPhone, 
                      dbo.Loads.BillingDepartment, dbo.Loads.BillingStatus
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.Customer ON dbo.Loads.Id = dbo.Customer.Id LEFT OUTER JOIN
                      dbo.Profile LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id
WHERE     (dbo.Loads.DispatchStatus = 'Scheduled')
ORDER BY dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime
       )

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../../../Tables/dbo_Customer.md)
* [[dbo].[Driver]](../../../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../../../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../../../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../../../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

