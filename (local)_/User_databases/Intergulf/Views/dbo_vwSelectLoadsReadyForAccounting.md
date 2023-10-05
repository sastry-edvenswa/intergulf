#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsReadyForAccounting

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsReadyForAccounting]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:51:43 PM Wednesday, January 28, 2015 |
| Last Modified | 10:15:37 PM Monday, July 12, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Generator Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Id | bigint | 8 |
| Customer Name | varchar(100) | 100 |
| Vendor Id | bigint | 8 |
| Vendor Name | varchar(50) | 50 |
| Profile Number | bigint | 8 |
| Profile Direction | varchar(50) | 50 |
| Profile Type | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| Destination Name | nvarchar(100) | 200 |
| Truck Id | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| LabTestId | bigint | 8 |
| LabTestDate | datetime | 8 |
| DocumentNumber | varchar(50) | 50 |
| AccountingPrint | varchar(3) | 3 |
| AccountingAction | varchar(40) | 40 |
| AccountingStatus | varchar(40) | 40 |
| Accountingnotes | varchar(3000) | 3000 |
| BillingTime | numeric(18,2) | 9 |
| BillingRate | numeric(18,0) | 9 |
| Id | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsReadyForAccounting]
AS
SELECT        TOP (100) PERCENT fnSelectProfile.GeneratorId AS [Generator Id], fnSelectGenerator.Name AS [Generator Name], fnSelectProfile.CustomerId AS [Customer Id], fnSelectCustomer.Name AS [Customer Name], 
                         fnSelectProfile.VendorId AS [Vendor Id], fnSelectVendor.Name AS [Vendor Name], fnSelectLoads.ProfileId AS [Profile Number], fnSelectProfile.Direction AS [Profile Direction], 
                         fnSelectProfile.ProfileType AS [Profile Type], fnSelectLoads.ScheduledDate, fnSelectLoads.ScheduledTime, fnSelectDestination.Name AS [Destination Name], fnSelectLoads.TruckId AS [Truck Id], 
                         fnSelectLoads.TrailerId, fnSelectDriver.FirstName AS [Driver First Name], fnSelectDriver.LastName AS [Driver Last Name], fnSelectLoads.DispatchStatus, fnSelectLoads.BillingDepartment, 
                         fnSelectLoads.BillingStatus, fnSelectLoads.VesselTank, fnSelectLabTest.Id AS LabTestId, fnSelectLabTest.TestDate AS LabTestDate, fnSelectLabTest.DocumentNumber, fnSelectLoads.AccountingPrint, 
                         fnSelectLoads.AccountingAction, fnSelectLoads.AccountingStatus, fnSelectLoads.Accountingnotes, dbo.LoadsBillingSummary.BillingTime, dbo.LoadsBillingSummary.BillingRate, fnSelectLoads.Id
FROM            dbo.fnSelectLabTest() AS fnSelectLabTest RIGHT OUTER JOIN
                         dbo.fnSelectLoads() AS fnSelectLoads LEFT OUTER JOIN
                         dbo.LoadsBillingSummary ON fnSelectLoads.Id = dbo.LoadsBillingSummary.LoadId ON fnSelectLabTest.Id = fnSelectLoads.LabTestId LEFT OUTER JOIN
                         dbo.fnSelectDestination() AS fnSelectDestination ON fnSelectLoads.DestinationId = fnSelectDestination.Id LEFT OUTER JOIN
                         dbo.fnSelectVendor() AS fnSelectVendor RIGHT OUTER JOIN
                         dbo.fnSelectProfile() AS fnSelectProfile ON fnSelectVendor.Id = fnSelectProfile.VendorId LEFT OUTER JOIN
                         dbo.fnSelectGenerator() AS fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id ON fnSelectLoads.ProfileId = fnSelectProfile.Id LEFT OUTER JOIN
                         dbo.fnSelectDriver() AS fnSelectDriver ON fnSelectLoads.DriverId = fnSelectDriver.Id LEFT OUTER JOIN
                         dbo.fnSelectCustomer() AS fnSelectCustomer ON fnSelectLoads.CustomerId = fnSelectCustomer.Id
WHERE        (fnSelectLoads.ScheduledDate > CONVERT(DATETIME, '2021-07-01 00:00:00', 102))
ORDER BY fnSelectLoads.ScheduledDate, fnSelectLoads.ScheduledTime, [Truck Id]
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTest.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)
* [[dbo].[fnSelectVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectVendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

