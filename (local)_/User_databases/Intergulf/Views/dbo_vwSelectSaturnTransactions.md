#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectSaturnTransactions

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectSaturnTransactions]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:42:00 PM Saturday, October 8, 2022 |
| Last Modified | 6:52:07 PM Monday, April 24, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadNo | bigint | 8 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| TrackInventory | varchar(3) | 3 |
| ProfileNumber | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| ProfileContractNumber | varchar(20) | 20 |
| LoadContractNumber | varchar(50) | 50 |
| Product | varchar(20) | 20 |
| Product Description | varchar(500) | 500 |
| Vid | bigint | 8 |
| VendorName | varchar(50) | 50 |
| Supplier | varchar(50) | 50 |
| VendorNumber | varchar(50) | 50 |
| CId | numeric(18,0) | 9 |
| Customer | varchar(100) | 100 |
| Customer No | varchar(20) | 20 |
| DestId | int | 4 |
| Destination | nvarchar(100) | 200 |
| LoadType | varchar(50) | 50 |
| EquipmentType | varchar(50) | 50 |
| TransactionType | varchar(20) | 20 |
| From Tank Location | varchar(50) | 50 |
| FromTank | varchar(255) | 255 |
| To Tank Location | varchar(50) | 50 |
| ToTank | varchar(225) | 225 |
| LoadTank | varchar(50) | 50 |
| LabTank | varchar(50) | 50 |
| Phase | varchar(50) | 50 |
| Quantity | decimal(18,2) | 9 |
| Unit | varchar(50) | 50 |
| ActualQuantity | decimal(18,0) | 9 |
| ActualUnits | varchar(50) | 50 |
| SaturnQuantity | decimal(18,0) | 9 |
| SaturnUnits | varchar(255) | 255 |
| LabTestId | bigint | 8 |
| PcntWater | decimal(18,2) | 9 |
| PetroleumAdjAPI | decimal(18,1) | 9 |
| PetroleumFlashPoint | decimal(18,0) | 9 |
| PetroleumAsh | decimal(18,4) | 9 |
| PetroleumSulfurMType | varchar(10) | 10 |
| PetroleumSulfur | decimal(18,2) | 9 |
| PetroleumSeds | decimal(18,2) | 9 |
| PetroleumViscosity | decimal(18,2) | 9 |
| CustomerPickupDelivery | varchar(3) | 3 |
| TId | numeric(19,0) | 9 |
| Transporter | varchar(100) | 100 |
| BillingTime | numeric(18,2) | 9 |
| BillingRate | numeric(18,0) | 9 |
| AddWashOut | bit | 1 |
| DriverTime | numeric(18,2) | 9 |
| TPBillingTime | numeric(18,2) | 9 |
| TPBillingRate | numeric(18,0) | 9 |
| TPDriverTime | numeric(18,2) | 9 |
| TPAddWashOut | bit | 1 |
| L1PickupTime | numeric(19,2) | 9 |
| L1DeliveryTime | numeric(19,2) | 9 |
| L2PickupTime | numeric(19,2) | 9 |
| L2DeliveryTime | numeric(19,2) | 9 |
| LoadDriverId | bigint | 8 |
| Did | numeric(18,0) | 9 |
| DriveId | bigint | 8 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| AccountingStatus | varchar(40) | 40 |
| AccountingAction | varchar(40) | 40 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| DocumentNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| Notes | varchar(6000) | 6000 |
| CustomerPoNumber | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectSaturnTransactions]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id AS LoadNo, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, Tanks_1.TrackInventory, dbo.Profile.ProfileNumber, dbo.Profile.ProfileType, dbo.Profile.Direction, 
                         dbo.Profile.ContractNumber AS ProfileContractNumber, dbo.Loads.ContractNumber AS LoadContractNumber, dbo.Profile.Product, dbo.Product.Description AS [Product Description], dbo.Profile.VendorId AS Vid, 
                         dbo.Vendor.Name AS VendorName, dbo.Vendor.ShortName AS Supplier, dbo.Vendor.Mas90Id AS VendorNumber, dbo.Customer.Id AS CId, dbo.Customer.Name AS Customer, 
                         dbo.Customer.SageCustomerNumber AS [Customer No], dbo.Destination.Id AS DestId, dbo.Destination.Name AS Destination, dbo.Loads.LoadType, trim(dbo.LoadRequest.EquipmentType) AS EquipmentType, 
                         dbo.Loads.TransactionType,
                             (SELECT        Location
                               FROM            dbo.Tanks
                               WHERE        (Description = dbo.fnFromTank(dbo.Loads.TankNumber, dbo.LabTestDisbursement.Tank, dbo.Loads.TransactionType))) AS [From Tank Location], dbo.fnFromTank(dbo.Loads.TankNumber, 
                         dbo.LabTestDisbursement.Tank, dbo.Loads.TransactionType) AS FromTank,
                             (SELECT        Location
                               FROM            dbo.Tanks AS Tanks_2
                               WHERE        (Description = dbo.fnToTank(dbo.Loads.TankNumber, dbo.LabTestDisbursement.Tank, dbo.Loads.TransactionType))) AS [To Tank Location], dbo.fnToTank(dbo.Loads.TankNumber, 
                         dbo.LabTestDisbursement.Tank, dbo.Loads.TransactionType) AS ToTank, dbo.Loads.TankNumber AS LoadTank, dbo.LabTestDisbursement.Tank AS LabTank, dbo.LabTestDisbursement.Phase, 
                         dbo.LabTestDisbursement.Quantity, dbo.LabTestDisbursement.Unit, dbo.LabTest.ActualQuantity, dbo.LabTest.ActualUnits, dbo.fnSaturnQty(dbo.LabTestDisbursement.Quantity, dbo.LabTestDisbursement.Unit, 
                         dbo.LabTest.ActualQuantity, dbo.LabTest.ActualUnits) AS SaturnQuantity, dbo.fnSaturnUnits(dbo.LabTestDisbursement.Quantity, dbo.LabTestDisbursement.Unit, dbo.LabTest.ActualQuantity, 
                         dbo.LabTest.ActualUnits) AS SaturnUnits, dbo.LabTestDisbursement.LabTestId, dbo.LabTest.PcntWater, dbo.LabTest.PetroleumAdjAPI, dbo.LabTest.PetroleumFlashPoint, dbo.LabTest.PetroleumAsh, 
                         dbo.LabTest.PetroleumSulfurMType, dbo.LabTest.PetroleumSulfur, dbo.LabTest.PetroleumSeds, dbo.LabTest.PetroleumViscosity, dbo.Loads.CustomerPickupDelivery, dbo.Transporter.Id AS TId, 
                         TRIM(dbo.Transporter.Name) AS Transporter, dbo.LoadsBillingSummary.BillingTime, dbo.LoadsBillingSummary.BillingRate, dbo.LoadsBillingSummary.AddWashOut, dbo.LoadsBillingSummary.DriverTime, 
                         dbo.LoadsBillingSummary.TPBillingTime, dbo.LoadsBillingSummary.TPBillingRate, dbo.LoadsBillingSummary.TPDriverTime, dbo.LoadsBillingSummary.TPAddWashOut,
                             (SELECT        PickupLocationDepartTime - PickupLocationArrivalTime AS Expr1
                               FROM            dbo.LoadsBilling
                               WHERE        (LoadId = dbo.Loads.Id) AND (LegNumber = 1)) AS L1PickupTime,
                             (SELECT        DeliveryLocationDepartTime - DeliveryLocationArrivalTime AS Expr1
                               FROM            dbo.LoadsBilling AS LoadsBilling_2
                               WHERE        (LoadId = dbo.Loads.Id) AND (LegNumber = 1)) AS L1DeliveryTime,
                             (SELECT        PickupLocationDepartTime - PickupLocationArrivalTime AS Expr1
                               FROM            dbo.LoadsBilling AS LoadsBilling_3
                               WHERE        (LoadId = dbo.Loads.Id) AND (LegNumber = 2)) AS L2PickupTime,
                             (SELECT        DeliveryLocationDepartTime - DeliveryLocationArrivalTime AS Expr1
                               FROM            dbo.LoadsBilling AS LoadsBilling_3
                               WHERE        (LoadId = dbo.Loads.Id) AND (LegNumber = 2)) AS L2DeliveryTime, dbo.Loads.DriverId AS LoadDriverId, dbo.Driver.Id AS Did, dbo.Driver.DriverId AS DriveId, Trim(dbo.Driver.FirstName) 
                         AS [Driver First Name], Trim(dbo.Driver.LastName) AS [Driver Last Name], dbo.Loads.BillingDepartment, dbo.Loads.DispatchStatus, dbo.Loads.AccountingStatus, dbo.Loads.AccountingAction, dbo.Loads.TruckId, 
                         dbo.Loads.TrailerId, dbo.LabTest.DocumentNumber, dbo.Loads.DeliveryReleaseNumber, dbo.fnCleanNotes(dbo.Loads.Notes) AS Notes, dbo.Loads.CustomerPoNumber, 
                         dbo.fnUpdateDateTimeSaturn(dbo.Loads.UpdateDateTime, dbo.LabTest.UpdateDateTime) AS UpdateDateTime
FROM            dbo.Driver RIGHT OUTER JOIN
                         dbo.LoadRequest RIGHT OUTER JOIN
                         dbo.LoadsBilling AS LoadsBilling_1 RIGHT OUTER JOIN
                         dbo.Loads ON LoadsBilling_1.LoadId = dbo.Loads.Id ON dbo.LoadRequest.Id = dbo.Loads.LoadRequestId LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id ON dbo.Driver.Id = dbo.Loads.DriverId LEFT OUTER JOIN
                         dbo.LoadsBillingSummary ON dbo.Loads.Id = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                         dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Vendor RIGHT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.Product ON dbo.Profile.Product = dbo.Product.Product ON dbo.Vendor.Id = dbo.Profile.VendorId ON dbo.Loads.ProfileId = dbo.Profile.Id RIGHT OUTER JOIN
                         dbo.LabTest RIGHT OUTER JOIN
                         dbo.LabTestDisbursement ON dbo.LabTest.Id = dbo.LabTestDisbursement.LabTestId LEFT OUTER JOIN
                         dbo.Tanks AS Tanks_1 ON dbo.LabTestDisbursement.Tank = Tanks_1.Description ON dbo.Loads.LabTestId = dbo.LabTestDisbursement.LabTestId
WHERE        (Tanks_1.TrackInventory = 'Yes') AND (dbo.Loads.ScheduledDate > CONVERT(DATETIME, '2022-12-31 00:00:00', 102)) AND (LoadsBilling_1.LegNumber = 1 OR
                         LoadsBilling_1.LegNumber IS NULL)
ORDER BY dbo.LoadsBillingSummary.TPAddWashOut, LoadNo
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[LabTestDisbursement]](../Tables/dbo_LabTestDisbursement.md)
* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBilling]](../Tables/dbo_LoadsBilling.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[Product]](../Tables/dbo_Product.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Tanks]](../Tables/dbo_Tanks.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[Vendor]](../Tables/dbo_Vendor.md)
* [[dbo].[fnCleanNotes]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnCleanNotes.md)
* [[dbo].[fnFromTank]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnFromTank.md)
* [[dbo].[fnSaturnQty]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSaturnQty.md)
* [[dbo].[fnSaturnUnits]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSaturnUnits.md)
* [[dbo].[fnToTank]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnToTank.md)
* [[dbo].[fnUpdateDateTimeSaturn]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnUpdateDateTimeSaturn.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

