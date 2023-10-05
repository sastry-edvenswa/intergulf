#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:16:52 PM Saturday, February 10, 2007 |
| Last Modified | 11:31:30 AM Sunday, March 15, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| SalesPersonId | varchar(50) | 50 |
| CustomerId | bigint | 8 |
| VendorId | bigint | 8 |
| ProfileId | bigint | 8 |
| LoadType | varchar(50) | 50 |
| TransporterId | bigint | 8 |
| DriverId | bigint | 8 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| ContainerTypeId | bigint | 8 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| ActualDate | datetime | 8 |
| ActualTime | datetime | 8 |
| StartTime | datetime | 8 |
| EndTime | datetime | 8 |
| DocumentNumber | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| Notes | varchar(6000) | 6000 |
| Processed | int | 4 |
| LoadRequestId | bigint | 8 |
| RequestedDate | datetime | 8 |
| RequestedTime | datetime | 8 |
| ContactName | varchar(100) | 100 |
| ContactPhone | varchar(50) | 50 |
| PickupLocation | varchar(200) | 200 |
| VesselTank | varchar(100) | 100 |
| DestinationId | bigint | 8 |
| NoLoads | int | 4 |
| EstQuantity | varchar(50) | 50 |
| EquipmentType | varchar(50) | 50 |
| SubOk | varchar(10) | 10 |
| WashOutRequired | varchar(50) | 50 |
| WeightTicket | varchar(50) | 50 |
| SpecialRequirements | varchar(3000) | 3000 |
| DispatchStatus | varchar(50) | 50 |
| LabTestId | bigint | 8 |
| LabCheckInDate | datetime | 8 |
| LabStartTime | decimal(18,2) | 9 |
| LabTestStartTime | decimal(18,2) | 9 |
| LabTestEndTime | decimal(18,2) | 9 |
| LabEndTime | decimal(18,2) | 9 |
| PadCheckInDate | datetime | 8 |
| PadStartTime | decimal(18,2) | 9 |
| PadPumpStartTime | decimal(18,2) | 9 |
| PadPumpStopTime | decimal(18,2) | 9 |
| PadEndTime | decimal(18,2) | 9 |
| WashOutPerformed | varchar(50) | 50 |
| WashOutTime | decimal(18,2) | 9 |
| PickupDate | datetime | 8 |
| PickupDepartTime | numeric(18,2) | 9 |
| PickupLocationArrivalTime | numeric(18,2) | 9 |
| PickupLocationDepartTime | numeric(18,2) | 9 |
| DeliveryDate | datetime | 8 |
| DeliveryArrivalTime | numeric(18,2) | 9 |
| DeliveryDepartTime | numeric(18,2) | 9 |
| DeliveryCompleteTime | numeric(18,2) | 9 |
| BillingTime | decimal(18,2) | 9 |
| BillingRate | decimal(18,2) | 9 |
| Number | varchar(50) | 50 |
| PackageType | varchar(50) | 50 |
| ShippingWeight | decimal(18,0) | 9 |
| BillingDepartment | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| DriverTimeNotes | varchar(3000) | 3000 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| AccountingStatus | varchar(40) | 40 |
| AccountingPrint | varchar(3) | 3 |
| AccountingAction | varchar(40) | 40 |
| Accountingnotes | varchar(3000) | 3000 |
| PadNotes | varchar(3000) | 3000 |
| BlindLoadId | bigint | 8 |
| ProjectNumber | varchar(50) | 50 |
| ExportedToSteers | varchar(3) | 3 |
| CommissionsPaid | varchar(3) | 3 |
| CreateUser | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| CreateComputer | varchar(50) | 50 |
| CustomerPickupDelivery | varchar(3) | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwLoads]
AS
SELECT        Id, SalesPersonId, CustomerId, VendorId, ProfileId, LoadType, TransporterId, DriverId, TruckId, TrailerId, ContainerTypeId, ScheduledDate, ScheduledTime, ActualDate, ActualTime, StartTime, EndTime, 
                         DocumentNumber, TankNumber, DeliveryReleaseNumber, Notes, Processed, LoadRequestId, RequestedDate, RequestedTime, ContactName, ContactPhone, PickupLocation, VesselTank, DestinationId, NoLoads, 
                         EstQuantity, EquipmentType, SubOk, WashOutRequired, WeightTicket, SpecialRequirements, DispatchStatus, LabTestId, LabCheckInDate, LabStartTime, LabTestStartTime, LabTestEndTime, LabEndTime, 
                         PadCheckInDate, PadStartTime, PadPumpStartTime, PadPumpStopTime, PadEndTime, WashOutPerformed, WashOutTime, PickupDate, PickupDepartTime, PickupLocationArrivalTime, PickupLocationDepartTime, 
                         DeliveryDate, DeliveryArrivalTime, DeliveryDepartTime, DeliveryCompleteTime, BillingTime, BillingRate, Number, PackageType, ShippingWeight, BillingDepartment, BillingStatus, DriverTimeNotes, 
                         UpdateDateTime, UpdateUser, UpdateComputer, AccountingStatus, AccountingPrint, AccountingAction, Accountingnotes, PadNotes, BlindLoadId, ProjectNumber, ExportedToSteers, CommissionsPaid, CreateUser, 
                         CreateDateTime, CreateComputer, CustomerPickupDelivery
FROM            dbo.fnSelectLoads() AS fnSelectLoads
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

