#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadLabVolume

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadLabVolume]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:21:44 PM Friday, May 25, 2018 |
| Last Modified | 9:21:44 PM Friday, May 25, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| Profile Number | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| TruckId | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| DestinationName | nvarchar(100) | 200 |
| LastName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LabTestId | bigint | 8 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |
| PcntWater | decimal(18,2) | 9 |
| PcntOil | decimal(18,2) | 9 |
| PcntSolids | decimal(18,2) | 9 |
| Notes | varchar(5000) | 5000 |
| Disb. Tank | varchar(50) | 50 |
| Disb. Phase | varchar(50) | 50 |
| Disb. Quantity | decimal(18,2) | 9 |
| Disb. Unit | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectExportLoadLabVolume]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], 
                         dbo.Profile.ProfileNumber AS [Profile Number], dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Profile.ProfileType, dbo.Profile.Direction, 
                         dbo.Loads.DispatchStatus, dbo.Loads.TruckId, dbo.Equipment.Description, dbo.Profile.WasteCode, dbo.Destination.Name AS DestinationName, 
                         dbo.UserMaster.LastName, dbo.UserMaster.FirstName, dbo.Loads.LabTestId, dbo.LabTest.Quantity, dbo.LabTest.Units, dbo.LabTest.PcntWater, 
                         dbo.LabTest.PcntOil, dbo.LabTest.PcntSolids, dbo.LabTest.Notes, dbo.LabTestDisbursement.Tank AS [Disb. Tank], 
                         dbo.LabTestDisbursement.Phase AS [Disb. Phase], dbo.LabTestDisbursement.Quantity AS [Disb. Quantity], dbo.LabTestDisbursement.Unit AS [Disb. Unit]
FROM            dbo.LabTest LEFT OUTER JOIN
                         dbo.LabTestDisbursement ON dbo.LabTest.Id = dbo.LabTestDisbursement.LabTestId RIGHT OUTER JOIN
                         dbo.Loads ON dbo.LabTest.Id = dbo.Loads.LabTestId LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.Loads.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Equipment ON dbo.Loads.TruckId = dbo.Equipment.Id LEFT OUTER JOIN
                         dbo.Customer RIGHT OUTER JOIN
                         dbo.Profile ON dbo.Customer.Id = dbo.Profile.CustomerId ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY dbo.Loads.ScheduledDate, dbo.Loads.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[LabTestDisbursement]](../Tables/dbo_LabTestDisbursement.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

