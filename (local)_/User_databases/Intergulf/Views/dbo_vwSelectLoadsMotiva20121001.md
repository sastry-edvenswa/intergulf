#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsMotiva20121001

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsMotiva20121001]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:38:57 PM Monday, May 26, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Name | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| WashOutRequired | varchar(50) | 50 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| LabTestId | bigint | 8 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |
| Intergulf Destination | nvarchar(100) | 200 |
| PickupDate | datetime | 8 |
| PickupDepartTime | numeric(18,2) | 9 |
| PickupLocationArrivalTime | numeric(18,2) | 9 |
| PickupLocationDepartTime | numeric(18,2) | 9 |
| DeliveryDate | datetime | 8 |
| DeliveryArrivalTime | numeric(18,2) | 9 |
| DeliveryDepartTime | numeric(18,2) | 9 |
| DeliveryCompleteTime | numeric(18,2) | 9 |
| LegNumber | int | 4 |
| BeginningDate | datetime | 8 |
| LBStartTime | numeric(18,2) | 9 |
| LBPickupLocationArrivalTime | numeric(18,2) | 9 |
| LBPickupLocationDepartTime | numeric(18,2) | 9 |
| LBDeliveryLocationArrivalTime | numeric(18,2) | 9 |
| LBDeliveryLocationDepartTime | numeric(18,2) | 9 |
| EndTime | numeric(18,2) | 9 |
| BillingTime | numeric(18,2) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsMotiva20121001]
AS
SELECT     TOP 100 PERCENT dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, 
                      dbo.Loads.WashOutRequired, dbo.Loads.TruckId, dbo.Loads.TrailerId, dbo.Loads.DispatchStatus, dbo.Loads.LabTestId, dbo.LabTest.Quantity, 
                      dbo.LabTest.Units, dbo.Destination.Name AS [Intergulf Destination], dbo.Loads.PickupDate, dbo.Loads.PickupDepartTime, 
                      dbo.Loads.PickupLocationArrivalTime, dbo.Loads.PickupLocationDepartTime, dbo.Loads.DeliveryDate, dbo.Loads.DeliveryArrivalTime, 
                      dbo.Loads.DeliveryDepartTime, dbo.Loads.DeliveryCompleteTime, dbo.vwSelectLoadsBillingMotiva20121001.LegNumber, 
                      dbo.vwSelectLoadsBillingMotiva20121001.BeginningDate, dbo.vwSelectLoadsBillingMotiva20121001.StartTime AS LBStartTime, 
                      dbo.vwSelectLoadsBillingMotiva20121001.PickupLocationArrivalTime AS LBPickupLocationArrivalTime, 
                      dbo.vwSelectLoadsBillingMotiva20121001.PickupLocationDepartTime AS LBPickupLocationDepartTime, 
                      dbo.vwSelectLoadsBillingMotiva20121001.DeliveryLocationArrivalTime AS LBDeliveryLocationArrivalTime, 
                      dbo.vwSelectLoadsBillingMotiva20121001.DeliveryLocationDepartTime AS LBDeliveryLocationDepartTime, 
                      dbo.vwSelectLoadsBillingMotiva20121001.EndTime, dbo.vwSelectLoadsBillingMotiva20121001.BillingTime
FROM         dbo.vwSelectLoadsBillingMotiva20121001 RIGHT OUTER JOIN
                      dbo.Loads ON dbo.vwSelectLoadsBillingMotiva20121001.LoadId = dbo.Loads.Id LEFT OUTER JOIN
                      dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                      dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                      dbo.Generator INNER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE     (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2012-10-01 00:00:00', 102)) AND (dbo.Profile.ProfileNumber = '05384')
ORDER BY dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[vwSelectLoadsBillingMotiva20121001]](dbo_vwSelectLoadsBillingMotiva20121001.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

