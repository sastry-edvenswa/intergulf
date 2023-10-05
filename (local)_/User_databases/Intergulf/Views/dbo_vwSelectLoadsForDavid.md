#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsForDavid

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsForDavid]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:47:52 PM Friday, June 19, 2020 |
| Last Modified | 5:47:52 PM Friday, June 19, 2020 |


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


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsForDavid]
AS
SELECT        TOP (100) PERCENT Id, [Generator Id], [Generator Name], [Customer Id], [Customer Name], [Vendor Id], [Vendor Name], [Profile Direction], [Generator Facility], [Destination Facility], [Profile Type], SICCode, 
                         ScheduledDate, ScheduledTime, [Destination Name], [Truck Id], TrailerId, [Driver First Name], [Driver Last Name], DispatchStatus, BillingDepartment, BillingStatus, VesselTank, LabTestId, LabTestDate, 
                         DocumentNumber, AccountingPrint, AccountingAction, AccountingStatus, Accountingnotes, BillingTime, BillingRate, LoadType, TankNumber, ProjectNumber, [Profile Number], PetroleumFlashPoint, 
                         PetroleumAdjAPI, PetroleumPcntWater, PetroleumChlordetect, PetroleumAsh, PetroleumPour, TransporterId, Name, DeliveryReleaseNumber, WasteCode, [Load Salesperson], CSRPersonId, [Lab Qty], [Lab Units], 
                         [Actual Lab Qty], [Actual Lab Units], PcntWater, PcntOil, PcntSolids, PcntRags, [Lab Notes], [Lab Status], PreFlashPoint, FlashPoint, PreAPI, API, PreTemperature, Temperature, PreAdjAPI, AdjAPI, PrePetroleumAPI, 
                         PetroleumAPI, PrePetroleumFlashPoint, PrePetroleumChlordetect, PrePetroleumAsh, PrePetroleumPcntWater, PrePetroleumPour, PreAqueousCOD, AqueousCOD, PreAqueousAPI, AqueousAPI, PreAqueousTemp, 
                         AqueousTemp, PreAqueousAdjAPI, AqueousAdjAPI, PreAqueousFlashPoint, AqueousFlashPoint, PreAqueousPH, AqueousPH, PreAqueousAmmonia, AqueousAmmonia, PreAqueousZinc, AqueousZinc, 
                         PreAqueousCopper, AqueousCopper, PreAqueousToc, AqueousToc, PrePetroleumTemp, PetroleumTemp, PrePetroleumAdjAPI, OwnerId, DestinationId, CreateUser, CreateDateTime, CreateComputer, TPBillingTime,
                          TPBillingRate, SqlQty, [Profile SalesPerson]
FROM            dbo.vwSelectLoadsReadyForAccountingNew
WHERE        ([Generator Name] LIKE '%Exxon%') AND (ScheduledDate >= '01/01/2015') OR
                         (ScheduledDate >= '01/01/2015') AND ([Customer Name] LIKE '%Exxon%')
ORDER BY ScheduledDate, ScheduledTime, [Truck Id]
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[vwSelectLoadsReadyForAccountingNew]](dbo_vwSelectLoadsReadyForAccountingNew.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

