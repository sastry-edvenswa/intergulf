#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadBillingTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadBillingTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:15:29 PM Tuesday, March 6, 2018 |
| Last Modified | 10:15:29 PM Tuesday, March 6, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| LegNumber | int | 4 |
| BeginningDate | datetime | 8 |
| DeliveryLocationArrivalTime | numeric(18,2) | 9 |
| DeliveryLocationDepartTime | numeric(18,2) | 9 |
| TurnTime | numeric(19,2) | 9 |
| DispatchStatus | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadBillingTimes]
AS
SELECT        dbo.Loads.Id, dbo.LoadsBilling.LegNumber, dbo.LoadsBilling.BeginningDate, dbo.LoadsBilling.DeliveryLocationArrivalTime, 
                         dbo.LoadsBilling.DeliveryLocationDepartTime, dbo.LoadsBilling.DeliveryLocationDepartTime - dbo.LoadsBilling.DeliveryLocationArrivalTime AS TurnTime, 
                         dbo.Loads.DispatchStatus
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

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

