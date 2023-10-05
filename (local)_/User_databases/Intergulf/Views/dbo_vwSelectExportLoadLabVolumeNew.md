#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadLabVolumeNew

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadLabVolumeNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:03:32 PM Monday, August 6, 2018 |
| Last Modified | 11:05:19 AM Friday, February 8, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Load Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| Generator Facility | varchar(50) | 50 |
| Destination Facility | varchar(50) | 50 |
| Destination | nvarchar(100) | 200 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| DispatchStatus | varchar(50) | 50 |
| TruckId | varchar(50) | 50 |
| Lab Test Id | bigint | 8 |
| Manifest Qty | decimal(18,0) | 9 |
| Manifest Units | varchar(50) | 50 |
| Actual Qty | decimal(18,0) | 9 |
| Actual Units | varchar(50) | 50 |
| PcntWater | decimal(18,2) | 9 |
| PcntOil | decimal(18,2) | 9 |
| PcntSolids | decimal(18,2) | 9 |
| Tank | varchar(50) | 50 |
| Phase | varchar(50) | 50 |
| Quantity | decimal(18,2) | 9 |
| Units | varchar(50) | 50 |
| Notes | varchar(5000) | 5000 |
| Status | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportLoadLabVolumeNew]
AS
SELECT        dbo.Loads.Id AS [Load Id], dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], dbo.Loads.SalesPersonId, dbo.Profile.ProfileNumber, dbo.Profile.ProfileType, 
                         dbo.Profile.Direction, dbo.Generator.Facility AS [Generator Facility], dbo.Destination.Facility AS [Destination Facility], dbo.Destination.Name AS Destination, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, 
                         dbo.Loads.DispatchStatus, dbo.Loads.TruckId, dbo.LabTest.Id AS [Lab Test Id], dbo.LabTest.Quantity AS [Manifest Qty], dbo.LabTest.Units AS [Manifest Units], dbo.LabTest.ActualQuantity AS [Actual Qty], 
                         dbo.LabTest.ActualUnits AS [Actual Units], dbo.LabTest.PcntWater, dbo.LabTest.PcntOil, dbo.LabTest.PcntSolids, dbo.LabTestDisbursement.Tank, dbo.LabTestDisbursement.Phase, 
                         dbo.LabTestDisbursement.Quantity, dbo.LabTestDisbursement.Unit AS Units, dbo.LabTest.Notes, dbo.LabTest.Status
FROM            dbo.Profile INNER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id RIGHT OUTER JOIN
                         dbo.Customer INNER JOIN
                         dbo.Loads ON dbo.Customer.Id = dbo.Loads.CustomerId LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id ON dbo.Profile.Id = dbo.Loads.ProfileId LEFT OUTER JOIN
                         dbo.LabTestDisbursement INNER JOIN
                         dbo.LabTest ON dbo.LabTestDisbursement.LabTestId = dbo.LabTest.Id ON dbo.Loads.LabTestId = dbo.LabTest.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[LabTestDisbursement]](../Tables/dbo_LabTestDisbursement.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

