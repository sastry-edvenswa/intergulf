#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadsForAccounting

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadsForAccounting]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:43:27 PM Tuesday, August 28, 2018 |
| Last Modified | 4:48:59 PM Monday, August 21, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(100) | 100 |
| Vendor Name | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| Profile Direction | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
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
| ProjectNumber | varchar(50) | 50 |
| PMTote | numeric(18,4) | 9 |
| PMGallon | numeric(18,4) | 9 |
| PMDrum | numeric(18,4) | 9 |
| PMBarrel | numeric(18,4) | 9 |
| PTHour | numeric(18,4) | 9 |
| PTLoad | numeric(18,4) | 9 |
| PTGallon | numeric(18,4) | 9 |
| PTDemurrage | numeric(18,2) | 9 |
| PTFreeTime | numeric(18,0) | 9 |
| PTFuelSerCharge | numeric(18,0) | 9 |
| PTHourMin | numeric(18,2) | 9 |
| PTGallonMin | numeric(18,2) | 9 |
| PMTestType | varchar(50) | 50 |
| PMTestBase | numeric(18,2) | 9 |
| PMTestIncrement | numeric(18,2) | 9 |
| PMTestTote | numeric(18,3) | 9 |
| PMTestGallon | numeric(18,3) | 9 |
| PMTestDrum | numeric(18,3) | 9 |
| PMTestBarrel | numeric(18,2) | 9 |
| PMSolidsTestType | varchar(50) | 50 |
| PMSolidsBase | numeric(18,2) | 9 |
| PMSolidsIncrement | numeric(18,2) | 9 |
| PMSolidsTote | numeric(18,2) | 9 |
| PMSolidsGallon | numeric(18,3) | 9 |
| PMSolidsDrum | numeric(18,3) | 9 |
| PMSolidsBarrel | numeric(18,3) | 9 |
| PMMetals | numeric(18,2) | 9 |
| PMAmmonia | numeric(18,2) | 9 |
| MaxCentrifugeSolidsPcnt | numeric(18,0) | 9 |
| MaxFreePhaseWaterPcnt | numeric(18,0) | 9 |
| MaxFreePhaseOrganicPcnt | numeric(18,0) | 9 |
| MaxWaterByHach | numeric(18,0) | 9 |
| MaxChlordetect | numeric(18,0) | 9 |
| MaxViscosity | numeric(18,0) | 9 |
| MaxTotalAcid | numeric(18,0) | 9 |
| MinAPIGravity | numeric(18,0) | 9 |
| MaxWaterByDistillationPcnt | numeric(18,0) | 9 |
| MaxAshWtPcnt | numeric(18,0) | 9 |
| MaxPPMP | numeric(18,0) | 9 |
| MaxSulfur | numeric(18,0) | 9 |
| MaxSilicone | numeric(18,0) | 9 |
| MaxSodium | numeric(18,0) | 9 |
| MaxVanadium | numeric(18,0) | 9 |
| MaxAluminum | numeric(18,0) | 9 |
| Notes | varchar(5000) | 5000 |
| Status | varchar(20) | 20 |
| IDiscountPcnt | numeric(18,3) | 9 |
| IGallon | numeric(18,3) | 9 |
| IBarrel | numeric(18,3) | 9 |
| NewParkOnly | bit | 1 |
| LandfillOnly | bit | 1 |
| Clordtect | bit | 1 |
| DOTCorrosive | bit | 1 |
| CSUCommercial | bit | 1 |
| CSUOilBearing | bit | 1 |
| CSUUsedOil | bit | 1 |
| VaporPressure | varchar(50) | 50 |
| VaporPressureOther | varchar(50) | 50 |
| Benzene | varchar(50) | 50 |
| BenzeneOther | varchar(50) | 50 |
| Lab Test No | bigint | 8 |
| Lab Test Date | datetime | 8 |
| DocumentNumber | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| Lab Quantity | decimal(18,0) | 9 |
| Lab Units | varchar(50) | 50 |
| PcntWater | decimal(18,2) | 9 |
| PcntOil | decimal(18,2) | 9 |
| PcntSolids | decimal(18,2) | 9 |
| PcntRags | decimal(18,2) | 9 |
| Lab Notes | varchar(5000) | 5000 |
| Lab Status | varchar(50) | 50 |
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
| WashOut | varchar(50) | 50 |
| WashOutPerformed | varchar(50) | 50 |
| WashOutTime | decimal(18,2) | 9 |
| SageCustomerNumber | varchar(20) | 20 |
| TPBillingTime | numeric(18,2) | 9 |
| TPBillingRate | numeric(18,0) | 9 |
| CustomerPoNumber | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportLoadsForAccounting]
AS
SELECT        TOP (100) PERCENT fnSelectLoads.Id, fnSelectGenerator.Name AS [Generator Name], fnSelectCustomer.Name AS [Customer Name], fnSelectVendor.Name AS [Vendor Name], 
                         fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectProfile.Direction AS [Profile Direction], fnSelectLoads.ScheduledDate, fnSelectLoads.ScheduledTime, fnSelectDestination.Name AS [Destination Name], 
                         fnSelectLoads.TruckId AS [Truck Id], fnSelectLoads.TrailerId, fnSelectDriver.FirstName AS [Driver First Name], fnSelectDriver.LastName AS [Driver Last Name], fnSelectLoads.DispatchStatus, 
                         dbo.LoadsBillingSummary.BillingDepartment, dbo.LoadsBillingSummary.BillingTime, dbo.LoadsBillingSummary.BillingRate, dbo.LoadsBillingSummary.BillingStatus, fnSelectLoads.VesselTank, 
                         dbo.Transporter.Name AS Transporter, fnSelectProfile.WasteCode, fnSelectLoads.DeliveryReleaseNumber, fnSelectProfile.SalesPersonId, fnSelectLoads.AccountingPrint, fnSelectLoads.AccountingAction, 
                         fnSelectLoads.AccountingStatus, fnSelectLoads.Accountingnotes, fnSelectLoads.ProjectNumber, fnSelectProfile.PMTote, fnSelectProfile.PMGallon, fnSelectProfile.PMDrum, fnSelectProfile.PMBarrel, 
                         fnSelectProfile.PTHour, fnSelectProfile.PTLoad, fnSelectProfile.PTGallon, fnSelectProfile.PTDemurrage, fnSelectProfile.PTFreeTime, fnSelectProfile.PTFuelSerCharge, fnSelectProfile.PTHourMin, 
                         fnSelectProfile.PTGallonMin, fnSelectProfile.PMTestType, fnSelectProfile.PMTestBase, fnSelectProfile.PMTestIncrement, fnSelectProfile.PMTestTote, fnSelectProfile.PMTestGallon, fnSelectProfile.PMTestDrum, 
                         fnSelectProfile.PMTestBarrel, fnSelectProfile.PMSolidsTestType, fnSelectProfile.PMSolidsBase, fnSelectProfile.PMSolidsIncrement, fnSelectProfile.PMSolidsTote, fnSelectProfile.PMSolidsGallon, 
                         fnSelectProfile.PMSolidsDrum, fnSelectProfile.PMSolidsBarrel, fnSelectProfile.PMMetals, fnSelectProfile.PMAmmonia, fnSelectProfile.MaxCentrifugeSolidsPcnt, fnSelectProfile.MaxFreePhaseWaterPcnt, 
                         fnSelectProfile.MaxFreePhaseOrganicPcnt, fnSelectProfile.MaxWaterByHach, fnSelectProfile.MaxChlordetect, fnSelectProfile.MaxViscosity, fnSelectProfile.MaxTotalAcid, fnSelectProfile.MinAPIGravity, 
                         fnSelectProfile.MaxWaterByDistillationPcnt, fnSelectProfile.MaxAshWtPcnt, fnSelectProfile.MaxPPMP, fnSelectProfile.MaxSulfur, fnSelectProfile.MaxSilicone, fnSelectProfile.MaxSodium, 
                         fnSelectProfile.MaxVanadium, fnSelectProfile.MaxAluminum, fnSelectProfile.Notes, fnSelectProfile.Status, fnSelectProfile.IDiscountPcnt, fnSelectProfile.IGallon, fnSelectProfile.IBarrel, 
                         fnSelectProfile.NewParkOnly, fnSelectProfile.LandfillOnly, fnSelectProfile.Clordtect, fnSelectProfile.DOTCorrosive, fnSelectProfile.CSUCommercial, fnSelectProfile.CSUOilBearing, fnSelectProfile.CSUUsedOil, 
                         fnSelectProfile.VaporPressure, fnSelectProfile.VaporPressureOther, fnSelectProfile.Benzene, fnSelectProfile.BenzeneOther, fnSelectLabTest.Id AS [Lab Test No], fnSelectLabTest.TestDate AS [Lab Test Date], 
                         fnSelectLabTest.DocumentNumber, fnSelectLoads.TankNumber, fnSelectLabTest.Quantity AS [Lab Quantity], fnSelectLabTest.Units AS [Lab Units], fnSelectLabTest.PcntWater, fnSelectLabTest.PcntOil, 
                         fnSelectLabTest.PcntSolids, fnSelectLabTest.PcntRags, fnSelectLabTest.Notes AS [Lab Notes], fnSelectLabTest.Status AS [Lab Status], fnSelectLabTest.PreAqueousCOD, fnSelectLabTest.AqueousCOD, 
                         fnSelectLabTest.PreAqueousAPI, fnSelectLabTest.AqueousAPI, fnSelectLabTest.PreAqueousTemp, fnSelectLabTest.AqueousTemp, fnSelectLabTest.PreAqueousAdjAPI, fnSelectLabTest.AqueousAdjAPI, 
                         fnSelectLabTest.PreAqueousFlashPoint, fnSelectLabTest.AqueousFlashPoint, fnSelectLabTest.PreAqueousPH, fnSelectLabTest.AqueousPH, fnSelectLabTest.PreAqueousAmmonia, 
                         fnSelectLabTest.AqueousAmmonia, fnSelectLabTest.PreAqueousZinc, fnSelectLabTest.AqueousZinc, fnSelectLabTest.PreAqueousCopper, fnSelectLabTest.AqueousCopper, fnSelectLabTest.WashOut, 
                         fnSelectLoads.WashOutPerformed, fnSelectLoads.WashOutTime, fnSelectCustomer.SageCustomerNumber, dbo.LoadsBillingSummary.TPBillingTime, dbo.LoadsBillingSummary.TPBillingRate, 
                         fnSelectLoads.CustomerPoNumber
FROM            dbo.fnSelectLabTest() AS fnSelectLabTest RIGHT OUTER JOIN
                         dbo.Transporter RIGHT OUTER JOIN
                         dbo.fnSelectLoads() AS fnSelectLoads ON dbo.Transporter.Id = fnSelectLoads.TransporterId LEFT OUTER JOIN
                         dbo.LoadsBillingSummary ON fnSelectLoads.Id = dbo.LoadsBillingSummary.LoadId ON fnSelectLabTest.Id = fnSelectLoads.LabTestId LEFT OUTER JOIN
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

