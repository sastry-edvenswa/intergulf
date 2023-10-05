#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadInternalTruckNew

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadInternalTruckNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:48:22 PM Tuesday, November 7, 2017 |
| Last Modified | 1:26:14 PM Wednesday, November 8, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Destination | nvarchar(100) | 200 |
| Transporter | varchar(50) | 50 |
| Tank | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| Id | bigint | 8 |
| GeneratorName | varchar(100) | 100 |
| PickupLocationArrivalTime | numeric(18,2) | 9 |
| PickupLocationDepartTime | numeric(18,2) | 9 |
| DeliveryArrivalTime | numeric(18,2) | 9 |
| DeliveryDepartTime | numeric(18,2) | 9 |
| PickupDepartTime | numeric(18,2) | 9 |
| DeliveryCompleteTime | numeric(18,2) | 9 |
| DispatchStatus | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| BillingTime | numeric(18,2) | 9 |
| BillingRate | numeric(18,0) | 9 |
| UserName | varchar(50) | 50 |
| ProfileId | bigint | 8 |
| LabTestId | bigint | 8 |
| TransporterId | bigint | 8 |
| SalesPersonId | varchar(50) | 50 |
| DriverName | varchar(101) | 101 |
| TimeOnSite | numeric(19,2) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadInternalTruckNew]
AS
SELECT        TOP (100) PERCENT dbo.Destination.Name AS Destination, dbo.Transporter.Name AS Transporter, dbo.Loads.TankNumber AS Tank, dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.Id, 
                         dbo.Generator.Name AS GeneratorName, dbo.Loads.PickupLocationArrivalTime, dbo.Loads.PickupLocationDepartTime, dbo.Loads.DeliveryArrivalTime, dbo.Loads.DeliveryDepartTime, 
                         dbo.Loads.PickupDepartTime, dbo.Loads.DeliveryCompleteTime, dbo.Loads.DispatchStatus, dbo.LoadsBillingSummary.BillingDepartment, dbo.LoadsBillingSummary.BillingStatus, dbo.Loads.VesselTank, 
                         dbo.LoadsBillingSummary.BillingTime, dbo.LoadsBillingSummary.BillingRate, dbo.UserMaster.UserName, dbo.Loads.ProfileId, dbo.Loads.LabTestId, dbo.Loads.TransporterId, dbo.Profile.SalesPersonId,
                             (SELECT        DriverName
                               FROM            dbo.vwSelectLegOneDriverOnSiteTime
                               WHERE        (Id = dbo.Loads.Id) AND (LegNumber = 1)) AS DriverName,
                             (SELECT        TimeOnSite
                               FROM            dbo.vwSelectLegOneDriverOnSiteTime AS vwSelectLegOneDriverOnSiteTime_1
                               WHERE        (Id = dbo.Loads.Id) AND (LegNumber = 1)) AS TimeOnSite
FROM            dbo.LabTest LEFT OUTER JOIN
                         dbo.LabTestDisbursement ON dbo.LabTest.Id = dbo.LabTestDisbursement.LabTestId RIGHT OUTER JOIN
                         dbo.LoadsBillingSummary RIGHT OUTER JOIN
                         dbo.Loads ON dbo.LoadsBillingSummary.LoadId = dbo.Loads.Id LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Transporter LEFT OUTER JOIN
                         dbo.Equipment ON dbo.Transporter.Id = dbo.Equipment.TransporterId ON dbo.Loads.TruckId = dbo.Equipment.Id ON dbo.LabTest.Id = dbo.Loads.LabTestId LEFT OUTER JOIN
                         dbo.Generator RIGHT OUTER JOIN
                         dbo.UserMaster RIGHT OUTER JOIN
                         dbo.Profile ON dbo.UserMaster.UserName = dbo.Profile.SalesPersonId ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE        (dbo.Transporter.Name = 'Intergulf Corporation')
ORDER BY Destination, dbo.Loads.ScheduledDate, dbo.Loads.TruckId
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[LabTestDisbursement]](../Tables/dbo_LabTestDisbursement.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[vwSelectLegOneDriverOnSiteTime]](dbo_vwSelectLegOneDriverOnSiteTime.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

