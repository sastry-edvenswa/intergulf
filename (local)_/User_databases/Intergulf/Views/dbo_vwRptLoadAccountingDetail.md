#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadAccountingDetail

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadAccountingDetail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:48:11 PM Tuesday, July 10, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Load Number | bigint | 8 |
| Salesperson First Name | varchar(50) | 50 |
| Salesperson Last Name | varchar(50) | 50 |
| GeneratorId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Profile Number | varchar(50) | 50 |
| Material Description | varchar(3000) | 3000 |
| Direction | varchar(50) | 50 |
| Profile Type | varchar(50) | 50 |
| Document Type | varchar(50) | 50 |
| HazMat | varchar(50) | 50 |
| Material Code | nvarchar(50) | 100 |
| Customer Name | varchar(50) | 50 |
| Vendor Name | varchar(50) | 50 |
| Transporter Name | varchar(50) | 50 |
| TruckId | varchar(50) | 50 |
| Truck Description | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Trailer Description | varchar(50) | 50 |
| Driver Number | bigint | 8 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| Scheduled Date | datetime | 8 |
| Scheduled Time | datetime | 8 |
| Document Number (Load) | varchar(50) | 50 |
| Delivery Release Number | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| Notes | varchar(6000) | 6000 |
| Dispatch Status | varchar(50) | 50 |
| Load Request Number | bigint | 8 |
| Requested Date | datetime | 8 |
| Requested Time | datetime | 8 |
| Contact Name | varchar(100) | 100 |
| Contact Phone | varchar(50) | 50 |
| Pickup Location | varchar(200) | 200 |
| Vessel Tank | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| Requested No Loads | int | 4 |
| Est Quantity | varchar(50) | 50 |
| Equipment Type | varchar(50) | 50 |
| Sub Ok | varchar(10) | 10 |
| Washout Required | varchar(50) | 50 |
| Weight Ticket Required | varchar(50) | 50 |
| Special Requirements | varchar(3000) | 3000 |
| Lab Test Number | bigint | 8 |
| Document Number (Lab Test) | varchar(50) | 50 |
| Lab Check In Date | datetime | 8 |
| Lab Start Time | datetime | 8 |
| Lab Test Start Time | datetime | 8 |
| Lab Test End Time | datetime | 8 |
| Lab End Time | datetime | 8 |
| Pad Check In Date | datetime | 8 |
| Pad Start Time | datetime | 8 |
| Pad Pump Start Time | datetime | 8 |
| Pad Pump Stop Time | datetime | 8 |
| Pad End Time | datetime | 8 |
| Washout Preformed | varchar(50) | 50 |
| Washout Time | datetime | 8 |
| Pickup Date | datetime | 8 |
| Pickup Depart Time | numeric(18,2) | 9 |
| Pickup Location Arrival Time | numeric(18,2) | 9 |
| Pickup Location Depart Time | numeric(18,2) | 9 |
| Delivery Date | datetime | 8 |
| Delivery Arrival Time | numeric(18,2) | 9 |
| Delivery Depart Time | numeric(18,2) | 9 |
| Delivery Complete Time | numeric(18,2) | 9 |
| Billing Time | decimal(18,2) | 9 |
| Billing Rate | decimal(18,2) | 9 |
| Billing Department | varchar(50) | 50 |
| Billing Status | varchar(50) | 50 |
| Driver Time Notes | varchar(3000) | 3000 |
| Accounting Print | varchar(3) | 3 |
| Accounting Action | varchar(40) | 40 |
| Accounting Status | varchar(40) | 40 |
| Accounting Notes | varchar(3000) | 3000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
Create view [dbo].[vwRptLoadAccountingDetail]
as
SELECT     TOP 100 PERCENT fnSelectLoads.Id AS [Load Number], fnSelectUserMaster.FirstName AS [Salesperson First Name], 
                      fnSelectUserMaster.LastName AS [Salesperson Last Name], fnSelectProfile.GeneratorId, fnSelectGenerator.Name AS [Generator Name], 
                      fnSelectProfile.ProfileNumber AS [Profile Number], fnSelectProfile.MaterialDescription AS [Material Description], fnSelectProfile.Direction, 
                      fnSelectProfile.ProfileType AS [Profile Type], fnSelectProfile.DocumentType AS [Document Type], fnSelectProfile.HazMat, 
                      dbo.MaterialCode.Description AS [Material Code], fnSelectCustomer.Name AS [Customer Name], fnSelectVendor.Name AS [Vendor Name], 
                      fnSelectTransporter.Name AS [Transporter Name], fnSelectLoads.TruckId, fnSelectEquipment.Description AS [Truck Description], 
                      fnSelectLoads.TrailerId, fnSelectEquipment_1.Description AS [Trailer Description], fnSelectLoads.DriverId AS [Driver Number], 
                      fnSelectDriver.FirstName AS [Driver First Name], fnSelectDriver.LastName AS [Driver Last Name], fnSelectLoads.ScheduledDate AS [Scheduled Date], 
                      fnSelectLoads.ScheduledTime AS [Scheduled Time], fnSelectLoads.DocumentNumber AS [Document Number (Load)], 
                      fnSelectLoads.DeliveryReleaseNumber AS [Delivery Release Number], fnSelectLoads.TankNumber, fnSelectLoads.Notes, 
                      fnSelectLoads.DispatchStatus AS [Dispatch Status], fnSelectLoads.LoadRequestId AS [Load Request Number], 
                      fnSelectLoads.RequestedDate AS [Requested Date], fnSelectLoads.RequestedTime AS [Requested Time], 
                      fnSelectLoads.ContactName AS [Contact Name], fnSelectLoads.ContactPhone AS [Contact Phone], fnSelectLoads.PickupLocation AS [Pickup Location], 
                      fnSelectLoads.VesselTank AS [Vessel Tank], fnSelectDestination.Name AS Destination, fnSelectLoads.NoLoads AS [Requested No Loads], 
                      fnSelectLoads.EstQuantity AS [Est Quantity], fnSelectLoads.EquipmentType AS [Equipment Type], fnSelectLoads.SubOk AS [Sub Ok], 
                      fnSelectLoads.WashOutRequired AS [Washout Required], fnSelectLoads.WeightTicket AS [Weight Ticket Required], 
                      fnSelectLoads.SpecialRequirements AS [Special Requirements], fnSelectLoads.LabTestId AS [Lab Test Number], 
                      fnSelectLabTest.DocumentNumber AS [Document Number (Lab Test)], fnSelectLoads.LabCheckInDate AS [Lab Check In Date], 
                      fnSelectLoads.LabStartTime AS [Lab Start Time], fnSelectLoads.LabTestStartTime AS [Lab Test Start Time], 
                      fnSelectLoads.LabTestEndTime AS [Lab Test End Time], fnSelectLoads.LabEndTime AS [Lab End Time], 
                      fnSelectLoads.PadCheckInDate AS [Pad Check In Date], fnSelectLoads.PadStartTime AS [Pad Start Time], 
                      fnSelectLoads.PadPumpStartTime AS [Pad Pump Start Time], fnSelectLoads.PadPumpStopTime AS [Pad Pump Stop Time], 
                      fnSelectLoads.PadEndTime AS [Pad End Time], fnSelectLoads.WashOutPerformed AS [Washout Preformed], 
                      fnSelectLoads.WashOutTime AS [Washout Time], fnSelectLoads.PickupDate AS [Pickup Date], 
                      fnSelectLoads.PickupDepartTime AS [Pickup Depart Time], fnSelectLoads.PickupLocationArrivalTime AS [Pickup Location Arrival Time], 
                      fnSelectLoads.PickupLocationDepartTime AS [Pickup Location Depart Time], fnSelectLoads.DeliveryDate AS [Delivery Date], 
                      fnSelectLoads.DeliveryArrivalTime AS [Delivery Arrival Time], fnSelectLoads.DeliveryDepartTime AS [Delivery Depart Time], 
                      fnSelectLoads.DeliveryCompleteTime AS [Delivery Complete Time], fnSelectLoads.BillingTime AS [Billing Time], 
                      fnSelectLoads.BillingRate AS [Billing Rate], fnSelectLoads.BillingDepartment AS [Billing Department], fnSelectLoads.BillingStatus AS [Billing Status], 
                      fnSelectLoads.DriverTimeNotes AS [Driver Time Notes], fnSelectLoads.AccountingPrint AS [Accounting Print], 
                      fnSelectLoads.AccountingAction AS [Accounting Action], fnSelectLoads.AccountingStatus AS [Accounting Status], 
                      fnSelectLoads.AccountingNotes AS [Accounting Notes]
FROM         dbo.fnSelectDriver() fnSelectDriver RIGHT OUTER JOIN
                      dbo.fnSelectLoads() fnSelectLoads LEFT OUTER JOIN
                      dbo.fnSelectDestination() fnSelectDestination ON fnSelectLoads.DestinationId = fnSelectDestination.Id LEFT OUTER JOIN
                      dbo.fnSelectLabTest() fnSelectLabTest ON fnSelectLoads.LabTestId = fnSelectLabTest.Id LEFT OUTER JOIN
                      dbo.fnSelectEquipment() fnSelectEquipment_1 ON fnSelectLoads.TrailerId = fnSelectEquipment_1.Id LEFT OUTER JOIN
                      dbo.fnSelectEquipment() fnSelectEquipment ON fnSelectLoads.TruckId = fnSelectEquipment.Id ON 
                      fnSelectDriver.Id = fnSelectLoads.DriverId LEFT OUTER JOIN
                      dbo.fnSelectTransporter() fnSelectTransporter ON fnSelectLoads.TransporterId = fnSelectTransporter.Id LEFT OUTER JOIN
                      dbo.fnSelectVendor() fnSelectVendor ON fnSelectLoads.VendorId = fnSelectVendor.Id LEFT OUTER JOIN
                      dbo.fnSelectCustomer() fnSelectCustomer ON fnSelectLoads.CustomerId = fnSelectCustomer.Id LEFT OUTER JOIN
                      dbo.MaterialCode INNER JOIN
                      dbo.fnSelectProfile() fnSelectProfile INNER JOIN
                      dbo.fnSelectGenerator() fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id ON 
                      dbo.MaterialCode.ID = fnSelectProfile.MaterialCodeId ON fnSelectLoads.ProfileId = fnSelectProfile.Id LEFT OUTER JOIN
                      dbo.fnSelectUserMaster() fnSelectUserMaster ON fnSelectLoads.SalesPersonId = fnSelectUserMaster.UserName
ORDER BY fnSelectLoads.Id DESC
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)
* [[dbo].[fnSelectEquipment]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectEquipment.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTest.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)
* [[dbo].[fnSelectTransporter]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectTransporter.md)
* [[dbo].[fnSelectUserMaster]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectUserMaster.md)
* [[dbo].[fnSelectVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectVendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

