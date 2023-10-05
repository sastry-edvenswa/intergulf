#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectAvailableForScheduledLoadsScheduled

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectAvailableForScheduledLoadsScheduled]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:23:06 PM Thursday, December 17, 2015 |
| Last Modified | 2:23:06 PM Thursday, December 17, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| Generator Name | varchar(100) | 100 |  |
| Customer Name | varchar(50) | 50 |  |
| Profile Number | varchar(50) | 50 |  |
| ScheduledDate | datetime | 8 |  |
| ScheduledTime | datetime | 8 |  |
| StartDateTime | bigint | 8 |  |
| EndDateTime | bigint | 8 |  |
| TruckId | varchar(50) | 50 |  |
| ActualDate | datetime | 8 |  |
| ActualTime | datetime | 8 |  |
| Driver First Name | varchar(50) | 50 |  |
| Driver Last Name | varchar(50) | 50 |  |
| ProfileType | varchar(50) | 50 |  |
| CustomerId | bigint | 8 |  |
| VendorId | bigint | 8 |  |
| DispatchStatus | varchar(50) | 50 |  |
| ContactName | varchar(100) | 100 |  |
| ContactPhone | varchar(50) | 50 |  |
| BillingDepartment | varchar(50) | 50 |  |
| BillingStatus | varchar(50) | 50 |  |
| VesselTank | varchar(100) | 100 |  |
| LabTestId | bigint | 8 |  |
| Status | varchar(50) | 50 |  |
| ScheduledLoadId | bigint | 8 |  |
| LabCheckOutDate | date | 3 |  |
| Direction | varchar(50) | 50 |  |
| DestinationFacility | varchar(50) | 50 |  |
| GeneratorFacility | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectAvailableForScheduledLoadsScheduled]
AS
SELECT     TOP (100) PERCENT dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.LoadsSchedule.StartDateTime, 
                      dbo.LoadsSchedule.EndDateTime, dbo.Loads.TruckId, dbo.Loads.ActualDate, dbo.Loads.ActualTime, dbo.Driver.FirstName AS [Driver First Name], 
                      dbo.Driver.LastName AS [Driver Last Name], dbo.Profile.ProfileType, dbo.Loads.CustomerId, dbo.Loads.VendorId, dbo.Loads.DispatchStatus, dbo.Loads.ContactName, 
                      dbo.Loads.ContactPhone, dbo.Loads.BillingDepartment, dbo.Loads.BillingStatus, dbo.Loads.VesselTank, dbo.Loads.LabTestId, dbo.LabTest.Status, 
                      dbo.LoadsSchedule.LoadId AS ScheduledLoadId, dbo.LoadsSchedule.LabCheckOutDate, dbo.Profile.Direction, dbo.Destination.Facility AS DestinationFacility, 
                      dbo.Generator.Facility AS GeneratorFacility
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                      dbo.LoadsSchedule ON dbo.Loads.Id = dbo.LoadsSchedule.LoadId LEFT OUTER JOIN
                      dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                      dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                      dbo.Profile LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id
WHERE     (dbo.Loads.DispatchStatus = 'Scheduled') AND (dbo.LoadsSchedule.LabCheckOutDate IS NULL) AND (dbo.LoadsSchedule.LoadId IS NULL)
ORDER BY dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime DESC

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsSchedule]](../Tables/dbo_LoadsSchedule.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

