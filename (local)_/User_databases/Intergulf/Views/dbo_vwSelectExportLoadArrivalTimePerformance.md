#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadArrivalTimePerformance

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadArrivalTimePerformance]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:57:22 PM Monday, April 15, 2019 |
| Last Modified | 3:59:57 PM Monday, April 22, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| Vendor Name | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| Profile Direction | varchar(50) | 50 |
| Scheduled Date | varchar(30) | 30 |
| Scheduled Time | varchar(30) | 30 |
| LegNumber | int | 4 |
| Pickup Date | varchar(30) | 30 |
| Pickup Time | varchar(30) | 30 |
| CPickupTime | varchar(30) | 30 |
| Destination Name | nvarchar(100) | 200 |
| Truck Id | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| BillingTime | numeric(18,2) | 9 |
| BillingRate | numeric(18,0) | 9 |
| BillingStatus | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| Transporter | varchar(100) | 100 |
| WasteCode | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| AccountingPrint | varchar(3) | 3 |
| AccountingAction | varchar(40) | 40 |
| AccountingStatus | varchar(40) | 40 |
| Accountingnotes | varchar(3000) | 3000 |
| ScheduledDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportLoadArrivalTimePerformance]
AS
SELECT        TOP (100) PERCENT fnSelectLoads.Id, fnSelectGenerator.Name AS [Generator Name], fnSelectCustomer.Name AS [Customer Name], fnSelectVendor.Name AS [Vendor Name], 
                         fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectProfile.Direction AS [Profile Direction], CONVERT(Varchar, fnSelectLoads.ScheduledDate, 110) AS [Scheduled Date], CONVERT(Varchar, 
                         fnSelectLoads.ScheduledTime, 108) AS [Scheduled Time], dbo.LoadsBilling.LegNumber, CONVERT(Varchar, dbo.LoadsBilling.BeginningDate, 110) AS [Pickup Date], CONVERT(Varchar, 
                         dbo.LoadsBilling.PickupLocationArrivalTime, 108) AS [Pickup Time], dbo.fnToPickupTimeRealTime(fnSelectProfile.Direction, CONVERT(Varchar, dbo.LoadsBilling.PickupLocationArrivalTime, 108)) AS CPickupTime, 
                         fnSelectDestination.Name AS [Destination Name], fnSelectLoads.TruckId AS [Truck Id], fnSelectLoads.TrailerId, fnSelectDriver.FirstName AS [Driver First Name], fnSelectDriver.LastName AS [Driver Last Name], 
                         fnSelectLoads.DispatchStatus, dbo.LoadsBillingSummary.BillingDepartment, dbo.LoadsBillingSummary.BillingTime, dbo.LoadsBillingSummary.BillingRate, dbo.LoadsBillingSummary.BillingStatus, 
                         fnSelectLoads.VesselTank, dbo.Transporter.Name AS Transporter, fnSelectProfile.WasteCode, fnSelectLoads.DeliveryReleaseNumber, fnSelectProfile.SalesPersonId, fnSelectLoads.AccountingPrint, 
                         fnSelectLoads.AccountingAction, fnSelectLoads.AccountingStatus, fnSelectLoads.Accountingnotes, fnSelectLoads.ScheduledDate
FROM            dbo.LoadsBillingSummary RIGHT OUTER JOIN
                         dbo.LoadsBilling RIGHT OUTER JOIN
                         dbo.fnSelectLoads() AS fnSelectLoads ON dbo.LoadsBilling.LoadId = fnSelectLoads.Id LEFT OUTER JOIN
                         dbo.Transporter ON fnSelectLoads.TransporterId = dbo.Transporter.Id ON dbo.LoadsBillingSummary.LoadId = fnSelectLoads.Id LEFT OUTER JOIN
                         dbo.fnSelectLabTest() AS fnSelectLabTest ON fnSelectLoads.LabTestId = fnSelectLabTest.Id LEFT OUTER JOIN
                         dbo.fnSelectDestination() AS fnSelectDestination ON fnSelectLoads.DestinationId = fnSelectDestination.Id LEFT OUTER JOIN
                         dbo.fnSelectVendor() AS fnSelectVendor RIGHT OUTER JOIN
                         dbo.fnSelectProfile() AS fnSelectProfile ON fnSelectVendor.Id = fnSelectProfile.VendorId LEFT OUTER JOIN
                         dbo.fnSelectGenerator() AS fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id ON fnSelectLoads.ProfileId = fnSelectProfile.Id LEFT OUTER JOIN
                         dbo.fnSelectDriver() AS fnSelectDriver ON fnSelectLoads.DriverId = fnSelectDriver.Id LEFT OUTER JOIN
                         dbo.fnSelectCustomer() AS fnSelectCustomer ON fnSelectLoads.CustomerId = fnSelectCustomer.Id
ORDER BY [Scheduled Date], [Scheduled Time], [Truck Id]
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadsBilling]](../Tables/dbo_LoadsBilling.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTest.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)
* [[dbo].[fnSelectVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectVendor.md)
* [[dbo].[fnToPickupTimeRealTime]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnToPickupTimeRealTime.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

