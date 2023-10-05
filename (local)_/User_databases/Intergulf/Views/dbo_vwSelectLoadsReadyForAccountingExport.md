#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsReadyForAccountingExport

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsReadyForAccountingExport]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:58:38 PM Tuesday, February 19, 2019 |
| Last Modified | 12:59:37 PM Wednesday, September 14, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ScheduledDate | datetime | 8 |
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(100) | 100 |
| VesselTank | varchar(100) | 100 |
| Destination Name | nvarchar(100) | 200 |
| BillingDepartment | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| AccountingStatus | varchar(40) | 40 |
| AccountingAction | varchar(40) | 40 |
| Accountingnotes | varchar(3000) | 3000 |
| TankNumber | varchar(50) | 50 |
| BillingTime | numeric(18,2) | 9 |
| ProjectNumber | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| SICCode | varchar(50) | 50 |
| LoadType | varchar(50) | 50 |
| PetroleumAdjAPI | decimal(18,1) | 9 |
| PetroleumPcntWater | decimal(18,1) | 9 |
| PetroleumFlashPoint | decimal(18,0) | 9 |
| PetroleumAsh | decimal(18,4) | 9 |
| PetroleumPour | decimal(18,0) | 9 |
| PetroleumChlordetect | decimal(18,0) | 9 |
| Truck Id | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Transporter Name | varchar(100) | 100 |
| DocumentNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| DestinationId | bigint | 8 |
| ScheduledTime | datetime | 8 |
| OwnerId | varchar(50) | 50 |
| Profile Create Date | datetime | 8 |
| PTHour | numeric(18,4) | 9 |
| PTLoad | numeric(18,4) | 9 |
| PTGallon | numeric(18,4) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsReadyForAccountingExport]
AS
SELECT        TOP (100) PERCENT fnSelectLoads.ScheduledDate, fnSelectLoads.Id, fnSelectGenerator.Name AS [Generator Name], fnSelectCustomer.Name AS [Customer Name], fnSelectLoads.VesselTank, 
                         fnSelectDestination.Name AS [Destination Name], dbo.LoadsBillingSummary.BillingDepartment, fnSelectLoads.DispatchStatus, dbo.LoadsBillingSummary.BillingStatus, fnSelectLoads.AccountingStatus, 
                         fnSelectLoads.AccountingAction, fnSelectLoads.Accountingnotes, fnSelectLoads.TankNumber, dbo.LoadsBillingSummary.BillingTime, fnSelectLoads.ProjectNumber, 
                         fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectProfile.ProfileType, fnSelectProfile.SICCode, fnSelectLoads.LoadType, fnSelectLabTest.PetroleumAdjAPI, fnSelectLabTest.PetroleumPcntWater, 
                         fnSelectLabTest.PetroleumFlashPoint, fnSelectLabTest.PetroleumAsh, fnSelectLabTest.PetroleumPour, fnSelectLabTest.PetroleumChlordetect, fnSelectLoads.TruckId AS [Truck Id], fnSelectLoads.TrailerId, 
                         dbo.Transporter.Name AS [Transporter Name], fnSelectLabTest.DocumentNumber, fnSelectLoads.DeliveryReleaseNumber, fnSelectLoads.SalesPersonId, fnSelectLoads.DestinationId, 
                         fnSelectLoads.ScheduledTime, dbo.LoadsInvoice.OwnerId, fnSelectProfile.CreateDate AS [Profile Create Date], fnSelectProfile.PTHour, fnSelectProfile.PTLoad, fnSelectProfile.PTGallon
FROM            dbo.LoadsBillingSummary RIGHT OUTER JOIN
                         dbo.LoadsInvoice RIGHT OUTER JOIN
                         dbo.fnSelectLoads() AS fnSelectLoads ON dbo.LoadsInvoice.LoadId = fnSelectLoads.Id LEFT OUTER JOIN
                         dbo.Transporter ON fnSelectLoads.TransporterId = dbo.Transporter.Id ON dbo.LoadsBillingSummary.LoadId = fnSelectLoads.Id LEFT OUTER JOIN
                         dbo.fnSelectLabTest() AS fnSelectLabTest ON fnSelectLoads.LabTestId = fnSelectLabTest.Id LEFT OUTER JOIN
                         dbo.fnSelectDestination() AS fnSelectDestination ON fnSelectLoads.DestinationId = fnSelectDestination.Id LEFT OUTER JOIN
                         dbo.fnSelectVendor() AS fnSelectVendor RIGHT OUTER JOIN
                         dbo.fnSelectProfile() AS fnSelectProfile ON fnSelectVendor.Id = fnSelectProfile.VendorId LEFT OUTER JOIN
                         dbo.fnSelectGenerator() AS fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id ON fnSelectLoads.ProfileId = fnSelectProfile.Id LEFT OUTER JOIN
                         dbo.fnSelectDriver() AS fnSelectDriver ON fnSelectLoads.DriverId = fnSelectDriver.Id LEFT OUTER JOIN
                         dbo.fnSelectCustomer() AS fnSelectCustomer ON fnSelectLoads.CustomerId = fnSelectCustomer.Id
ORDER BY fnSelectLoads.ScheduledDate, [Truck Id]
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[LoadsInvoice]](../Tables/dbo_LoadsInvoice.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
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

