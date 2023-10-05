#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsReadyForAccountingNew

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsReadyForAccountingNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:59:06 PM Tuesday, September 25, 2018 |
| Last Modified | 4:56:38 PM Tuesday, September 12, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Id | bigint | 8 |
| Customer Name | varchar(100) | 100 |
| Vendor Id | bigint | 8 |
| Vendor Name | varchar(50) | 50 |
| Profile Direction | varchar(50) | 50 |
| Generator Facility | varchar(50) | 50 |
| Destination Facility | varchar(50) | 50 |
| Profile Type | varchar(50) | 50 |
| SICCode | varchar(50) | 50 |
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
| LoadType | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| ProjectNumber | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| PetroleumFlashPoint | decimal(18,0) | 9 |
| PetroleumAdjAPI | decimal(18,1) | 9 |
| PetroleumPcntWater | decimal(18,1) | 9 |
| PetroleumChlordetect | decimal(18,0) | 9 |
| PetroleumAsh | decimal(18,4) | 9 |
| PetroleumPour | decimal(18,0) | 9 |
| TransporterId | bigint | 8 |
| Name | varchar(100) | 100 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| WasteClass | varchar(3) | 3 |
| Load Salesperson | varchar(50) | 50 |
| CSRPersonId | varchar(50) | 50 |
| Lab Qty | decimal(18,0) | 9 |
| Lab Units | varchar(50) | 50 |
| Actual Lab Qty | decimal(18,0) | 9 |
| Actual Lab Units | varchar(50) | 50 |
| PcntWater | decimal(18,2) | 9 |
| PcntOil | decimal(18,2) | 9 |
| PcntSolids | decimal(18,2) | 9 |
| PcntRags | decimal(18,2) | 9 |
| Lab Notes | varchar(5000) | 5000 |
| Lab Status | varchar(50) | 50 |
| PreFlashPoint | varchar(5) | 5 |
| FlashPoint | decimal(18,0) | 9 |
| PreAPI | varchar(5) | 5 |
| API | decimal(18,1) | 9 |
| PreTemperature | varchar(50) | 50 |
| Temperature | decimal(18,0) | 9 |
| PreAdjAPI | varchar(5) | 5 |
| AdjAPI | decimal(18,1) | 9 |
| PrePetroleumAPI | varchar(5) | 5 |
| PetroleumAPI | decimal(18,1) | 9 |
| PrePetroleumFlashPoint | varchar(5) | 5 |
| PrePetroleumChlordetect | varchar(5) | 5 |
| PrePetroleumAsh | varchar(5) | 5 |
| PrePetroleumPcntWater | varchar(5) | 5 |
| PrePetroleumPour | varchar(5) | 5 |
| PreAqueousCOD | varchar(5) | 5 |
| AqueousCOD | decimal(18,0) | 9 |
| PreAqueousAPI | varchar(5) | 5 |
| AqueousAPI | decimal(18,1) | 9 |
| PreAqueousTemp | varchar(5) | 5 |
| AqueousTemp | decimal(18,0) | 9 |
| PreAqueousAdjAPI | varchar(5) | 5 |
| AqueousAdjAPI | decimal(18,1) | 9 |
| PreAqueousFlashPoint | varchar(5) | 5 |
| AqueousFlashPoint | decimal(18,0) | 9 |
| PreAqueousPH | varchar(5) | 5 |
| AqueousPH | decimal(18,1) | 9 |
| PreAqueousAmmonia | varchar(5) | 5 |
| AqueousAmmonia | decimal(18,0) | 9 |
| PreAqueousZinc | varchar(5) | 5 |
| AqueousZinc | decimal(18,2) | 9 |
| PreAqueousCopper | varchar(50) | 50 |
| AqueousCopper | decimal(18,2) | 9 |
| PreAqueousToc | varchar(5) | 5 |
| AqueousToc | decimal(18,0) | 9 |
| PrePetroleumTemp | varchar(5) | 5 |
| PetroleumTemp | decimal(18,0) | 9 |
| PrePetroleumAdjAPI | varchar(5) | 5 |
| OwnerId | varchar(50) | 50 |
| DestinationId | bigint | 8 |
| CreateUser | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| CreateComputer | varchar(50) | 50 |
| TPBillingTime | numeric(18,2) | 9 |
| TPBillingRate | numeric(18,0) | 9 |
| SqlQty | decimal(15,0) | 9 |
| Profile SalesPerson | varchar(50) | 50 |
| ProfileId | bigint | 8 |
| PMTote | numeric(18,4) | 9 |
| PMGallon | numeric(18,4) | 9 |
| PMDrum | numeric(18,4) | 9 |
| PMBarrel | numeric(18,4) | 9 |
| PTHour | numeric(18,4) | 9 |
| PTLoad | numeric(18,4) | 9 |
| PTGallon | numeric(18,4) | 9 |
| Material Code | varchar(255) | 255 |
| WashOutRequired | varchar(50) | 50 |
| WashOutPerformed | varchar(50) | 50 |
| WashOut | varchar(50) | 50 |
| AddWashOut | bit | 1 |
| TPAddWashOut | bit | 1 |
| MaterialClassification | varchar(200) | 200 |
| CustomerPoNumber | varchar(50) | 50 |
| GName | varchar(100) | 100 |
| GAddress | varchar(3000) | 3000 |
| GCity | varchar(50) | 50 |
| GState | varchar(50) | 50 |
| GZip | varchar(50) | 50 |
| CName | varchar(100) | 100 |
| CAddress | varchar(3000) | 3000 |
| CCity | varchar(50) | 50 |
| CState | varchar(50) | 50 |
| CZip | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsReadyForAccountingNew]
AS
SELECT        TOP (100) PERCENT fnSelectLoads.Id, fnSelectProfile.GeneratorId AS [Generator Id], fnSelectGenerator.Name AS [Generator Name], fnSelectProfile.CustomerId AS [Customer Id], 
                         fnSelectCustomer.Name AS [Customer Name], fnSelectProfile.VendorId AS [Vendor Id], fnSelectVendor.Name AS [Vendor Name], fnSelectProfile.Direction AS [Profile Direction], 
                         fnSelectGenerator.Facility AS [Generator Facility], fnSelectDestination.Facility AS [Destination Facility], fnSelectProfile.ProfileType AS [Profile Type], fnSelectProfile.SICCode, fnSelectLoads.ScheduledDate, 
                         fnSelectLoads.ScheduledTime, fnSelectDestination.Name AS [Destination Name], fnSelectLoads.TruckId AS [Truck Id], fnSelectLoads.TrailerId, fnSelectDriver.FirstName AS [Driver First Name], 
                         fnSelectDriver.LastName AS [Driver Last Name], fnSelectLoads.DispatchStatus, dbo.LoadsBillingSummary.BillingDepartment, dbo.LoadsBillingSummary.BillingStatus, fnSelectLoads.VesselTank, 
                         fnSelectLabTest.Id AS LabTestId, fnSelectLabTest.TestDate AS LabTestDate, fnSelectLabTest.DocumentNumber, fnSelectLoads.AccountingPrint, fnSelectLoads.AccountingAction, fnSelectLoads.AccountingStatus, 
                         fnSelectLoads.Accountingnotes, dbo.LoadsBillingSummary.BillingTime, dbo.LoadsBillingSummary.BillingRate, fnSelectLoads.LoadType, fnSelectLoads.TankNumber, fnSelectLoads.ProjectNumber, 
                         fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectLabTest.PetroleumFlashPoint, fnSelectLabTest.PetroleumAdjAPI, fnSelectLabTest.PetroleumPcntWater, fnSelectLabTest.PetroleumChlordetect, 
                         fnSelectLabTest.PetroleumAsh, fnSelectLabTest.PetroleumPour, fnSelectLoads.TransporterId, dbo.Transporter.Name, fnSelectLoads.DeliveryReleaseNumber, fnSelectProfile.WasteCode, 
                         fnSelectProfile.WasteClass, fnSelectLoads.SalesPersonId AS [Load Salesperson], dbo.UserMaster.CSRPersonId, fnSelectLabTest.Quantity AS [Lab Qty], fnSelectLabTest.Units AS [Lab Units], 
                         fnSelectLabTest.ActualQuantity AS [Actual Lab Qty], fnSelectLabTest.ActualUnits AS [Actual Lab Units], fnSelectLabTest.PcntWater, fnSelectLabTest.PcntOil, fnSelectLabTest.PcntSolids, fnSelectLabTest.PcntRags, 
                         fnSelectLabTest.Notes AS [Lab Notes], fnSelectLabTest.Status AS [Lab Status], fnSelectLabTest.PreFlashPoint, fnSelectLabTest.FlashPoint, fnSelectLabTest.PreAPI, fnSelectLabTest.API, 
                         fnSelectLabTest.PreTemperature, fnSelectLabTest.Temperature, fnSelectLabTest.PreAdjAPI, fnSelectLabTest.AdjAPI, fnSelectLabTest.PrePetroleumAPI, fnSelectLabTest.PetroleumAPI, 
                         fnSelectLabTest.PrePetroleumFlashPoint, fnSelectLabTest.PrePetroleumChlordetect, fnSelectLabTest.PrePetroleumAsh, fnSelectLabTest.PrePetroleumPcntWater, fnSelectLabTest.PrePetroleumPour, 
                         fnSelectLabTest.PreAqueousCOD, fnSelectLabTest.AqueousCOD, fnSelectLabTest.PreAqueousAPI, fnSelectLabTest.AqueousAPI, fnSelectLabTest.PreAqueousTemp, fnSelectLabTest.AqueousTemp, 
                         fnSelectLabTest.PreAqueousAdjAPI, fnSelectLabTest.AqueousAdjAPI, fnSelectLabTest.PreAqueousFlashPoint, fnSelectLabTest.AqueousFlashPoint, fnSelectLabTest.PreAqueousPH, fnSelectLabTest.AqueousPH, 
                         fnSelectLabTest.PreAqueousAmmonia, fnSelectLabTest.AqueousAmmonia, fnSelectLabTest.PreAqueousZinc, fnSelectLabTest.AqueousZinc, fnSelectLabTest.PreAqueousCopper, fnSelectLabTest.AqueousCopper, 
                         fnSelectLabTest.PreAqueousToc, fnSelectLabTest.AqueousToc, fnSelectLabTest.PrePetroleumTemp, fnSelectLabTest.PetroleumTemp, fnSelectLabTest.PrePetroleumAdjAPI, dbo.LoadsInvoice.OwnerId, 
                         fnSelectLoads.DestinationId, fnSelectLoads.CreateUser, fnSelectLoads.CreateDateTime, fnSelectLoads.CreateComputer, dbo.LoadsBillingSummary.TPBillingTime, dbo.LoadsBillingSummary.TPBillingRate, 
                         dbo.fnLoadQuantityToGallons(fnSelectLabTest.ActualQuantity, fnSelectLabTest.ActualUnits) AS SqlQty, fnSelectProfile.SalesPersonId AS [Profile SalesPerson], fnSelectLoads.ProfileId, fnSelectProfile.PMTote, 
                         fnSelectProfile.PMGallon, fnSelectProfile.PMDrum, fnSelectProfile.PMBarrel, fnSelectProfile.PTHour, fnSelectProfile.PTLoad, fnSelectProfile.PTGallon, 
                         dbo.fnGetMaterialClassificationCode(fnSelectProfile.MaterialClassification) AS [Material Code], fnSelectLoads.WashOutRequired, fnSelectLoads.WashOutPerformed, fnSelectLabTest.WashOut, 
                         dbo.LoadsBillingSummary.AddWashOut, dbo.LoadsBillingSummary.TPAddWashOut, fnSelectProfile.MaterialClassification, fnSelectLoads.CustomerPoNumber, fnSelectGenerator.Name AS GName, 
                         fnSelectGenerator.Address AS GAddress, fnSelectGenerator.City AS GCity, fnSelectGenerator.State AS GState, fnSelectGenerator.Zip AS GZip, fnSelectCustomer.Name AS CName, 
                         fnSelectCustomer.Address AS CAddress, fnSelectCustomer.City AS CCity, fnSelectCustomer.State AS CState, fnSelectCustomer.Zip AS CZip
FROM            dbo.Transporter RIGHT OUTER JOIN
                         dbo.UserMaster RIGHT OUTER JOIN
                         dbo.fnSelectLoads() AS fnSelectLoads ON dbo.UserMaster.UserName = fnSelectLoads.SalesPersonId LEFT OUTER JOIN
                         dbo.LoadsInvoice ON fnSelectLoads.Id = dbo.LoadsInvoice.LoadId ON dbo.Transporter.Id = fnSelectLoads.TransporterId LEFT OUTER JOIN
                         dbo.LoadsBillingSummary ON fnSelectLoads.Id = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                         dbo.fnSelectLabTest() AS fnSelectLabTest ON fnSelectLoads.LabTestId = fnSelectLabTest.Id LEFT OUTER JOIN
                         dbo.fnSelectDestination() AS fnSelectDestination ON fnSelectLoads.DestinationId = fnSelectDestination.Id LEFT OUTER JOIN
                         dbo.fnSelectVendor() AS fnSelectVendor RIGHT OUTER JOIN
                         dbo.fnSelectProfile() AS fnSelectProfile ON fnSelectVendor.Id = fnSelectProfile.VendorId LEFT OUTER JOIN
                         dbo.fnSelectGenerator() AS fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id ON fnSelectLoads.ProfileId = fnSelectProfile.Id LEFT OUTER JOIN
                         dbo.fnSelectDriver() AS fnSelectDriver ON fnSelectLoads.DriverId = fnSelectDriver.Id LEFT OUTER JOIN
                         dbo.fnSelectCustomer() AS fnSelectCustomer ON fnSelectLoads.CustomerId = fnSelectCustomer.Id
ORDER BY fnSelectLoads.ScheduledDate, fnSelectLoads.ScheduledTime, [Truck Id]
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[LoadsInvoice]](../Tables/dbo_LoadsInvoice.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[fnGetMaterialClassificationCode]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnGetMaterialClassificationCode.md)
* [[dbo].[fnLoadQuantityToGallons]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnLoadQuantityToGallons.md)
* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTest.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)
* [[dbo].[fnSelectVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectVendor.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vSelectLoadsForDavid]](dbo_vSelectLoadsForDavid.md)
* [[dbo].[vwSelectLoadsForDavid]](dbo_vwSelectLoadsForDavid.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

