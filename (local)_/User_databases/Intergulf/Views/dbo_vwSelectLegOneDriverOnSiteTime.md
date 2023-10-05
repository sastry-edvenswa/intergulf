#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLegOneDriverOnSiteTime

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLegOneDriverOnSiteTime]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:45:24 PM Wednesday, May 30, 2018 |
| Last Modified | 11:45:24 PM Wednesday, May 30, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| LegNumber | int | 4 |
| BeginningDate | datetime | 8 |
| DriverName | varchar(101) | 101 |
| PickupLocationArrivalTime | numeric(18,2) | 9 |
| PickupLocationDepartTime | numeric(18,2) | 9 |
| PTimeOnSite | numeric(19,2) | 9 |
| DeliveryLocationArrivalTime | numeric(18,2) | 9 |
| DeliveryLocationDepartTime | numeric(18,2) | 9 |
| DTimeOnSite | numeric(19,2) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLegOneDriverOnSiteTime]
AS
SELECT        dbo.Loads.Id, dbo.LoadsBilling.LegNumber, dbo.LoadsBilling.BeginningDate, dbo.Driver.FirstName + ' ' + dbo.Driver.LastName AS DriverName, 
                         dbo.LoadsBilling.PickupLocationArrivalTime, dbo.LoadsBilling.PickupLocationDepartTime, 
                         dbo.LoadsBilling.PickupLocationDepartTime - dbo.LoadsBilling.PickupLocationArrivalTime AS PTimeOnSite, dbo.LoadsBilling.DeliveryLocationArrivalTime, 
                         dbo.LoadsBilling.DeliveryLocationDepartTime, dbo.LoadsBilling.DeliveryLocationDepartTime - dbo.LoadsBilling.DeliveryLocationArrivalTime AS DTimeOnSite
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.LoadsBilling ON dbo.Loads.Id = dbo.LoadsBilling.LoadId LEFT OUTER JOIN
                         dbo.Driver ON dbo.LoadsBilling.DriverId = dbo.Driver.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBilling]](../Tables/dbo_LoadsBilling.md)


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptLoadInternalTruck]](dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](dbo_vwRptLoadInternalTruckNew.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

