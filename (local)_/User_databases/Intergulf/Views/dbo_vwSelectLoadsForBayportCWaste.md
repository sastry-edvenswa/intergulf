#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsForBayportCWaste

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsForBayportCWaste]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:09:21 AM Wednesday, August 12, 2015 |
| Last Modified | 10:09:21 AM Wednesday, August 12, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| Generator Name | varchar(100) | 100 |  |
| Customer Name | varchar(50) | 50 |  |
| Profile Number | varchar(50) | 50 |  |
| ScheduledDate | datetime | 8 |  |
| ScheduledTime | datetime | 8 |  |
| ActualDate | datetime | 8 |  |
| ActualTime | datetime | 8 |  |
| ProfileType | varchar(50) | 50 |  |
| Direction | varchar(50) | 50 |  |
| DispatchStatus | varchar(50) | 50 |  |
| LoadRequestId | bigint | 8 |  |
| LabTestId | bigint | 8 |  |
| TruckId | varchar(50) | 50 |  |
| Description | varchar(50) | 50 |  |
| WasteCode | varchar(50) | 50 |  |
| DestinationName | nvarchar(100) | 200 |  |
| BlindLoadId | bigint | 8 |  |
| Accountingnotes | varchar(3000) | 3000 |  |
| AccountingStatus | varchar(40) | 40 |  |
| DocumentNumber | varchar(50) | 50 |  |
| DeliveryReleaseNumber | varchar(50) | 50 |  |
| ScheduledTimeSelect1 | varchar(2) | 2 |  |
| ScheduledTimeSelect2 | varchar(2) | 2 |  |
| Tank | varchar(50) | 50 |  |
| LabCheckInDate | datetime | 8 |  |
| LabStartTime | decimal(18,2) | 9 |  |
| LabTestStartTime | decimal(18,2) | 9 |  |
| LabTestEndTime | decimal(18,2) | 9 |  |
| LabEndTime | decimal(18,2) | 9 |  |
| PadCheckInDate | datetime | 8 |  |
| PadStartTime | decimal(18,2) | 9 |  |
| PadPumpStartTime | decimal(18,2) | 9 |  |
| PadPumpStopTime | decimal(18,2) | 9 |  |
| PadEndTime | decimal(18,2) | 9 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsForBayportCWaste]
AS
SELECT     TOP (100) PERCENT dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Loads.ActualDate, dbo.Loads.ActualTime, 
                      dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Loads.DispatchStatus, dbo.Loads.LoadRequestId, dbo.Loads.LabTestId, dbo.Loads.TruckId, 
                      dbo.Equipment.Description, dbo.Profile.WasteCode, dbo.Destination.Name AS DestinationName, dbo.Loads.BlindLoadId, dbo.Loads.Accountingnotes, 
                      dbo.Loads.AccountingStatus, dbo.Loads.DocumentNumber, dbo.Loads.DeliveryReleaseNumber, CONVERT(VARCHAR(2), dbo.Loads.ScheduledTime, 114) 
                      AS ScheduledTimeSelect1, CONVERT(VARCHAR(2), dbo.Loads.ScheduledTime, 114) AS ScheduledTimeSelect2, dbo.LabTestDisbursement.Tank, 
                      dbo.Loads.LabCheckInDate, dbo.Loads.LabStartTime, dbo.Loads.LabTestStartTime, dbo.Loads.LabTestEndTime, dbo.Loads.LabEndTime, dbo.Loads.PadCheckInDate, 
                      dbo.Loads.PadStartTime, dbo.Loads.PadPumpStartTime, dbo.Loads.PadPumpStopTime, dbo.Loads.PadEndTime
FROM         dbo.Destination RIGHT OUTER JOIN
                      dbo.Loads LEFT OUTER JOIN
                      dbo.LabTest INNER JOIN
                      dbo.LabTestDisbursement ON dbo.LabTest.Id = dbo.LabTestDisbursement.LabTestId ON dbo.Loads.LabTestId = dbo.LabTest.Id ON 
                      dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                      dbo.Equipment ON dbo.Loads.TruckId = dbo.Equipment.Id LEFT OUTER JOIN
                      dbo.Customer RIGHT OUTER JOIN
                      dbo.Profile ON dbo.Customer.Id = dbo.Profile.CustomerId ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE     (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2015-06-01 00:00:00', 102)) AND (dbo.Loads.ScheduledDate <= CONVERT(DATETIME, '2015-06-30 00:00:00', 102))
                       AND (CONVERT(VARCHAR(2), dbo.Loads.ScheduledTime, 114) >= '07') AND (CONVERT(VARCHAR(2), dbo.Loads.ScheduledTime, 114) <= '19') AND 
                      (dbo.LabTestDisbursement.Tank = 'T3-4')
ORDER BY dbo.Loads.ScheduledDate

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


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

