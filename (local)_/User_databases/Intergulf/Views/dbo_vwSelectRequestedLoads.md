#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectRequestedLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectRequestedLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:35:16 PM Sunday, September 17, 2017 |
| Last Modified | 5:18:27 PM Wednesday, June 23, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| LoadRequestDate | datetime | 8 |
| LoadRequestTime | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| ProfileId | bigint | 8 |
| NoLoads | decimal(18,0) | 9 |
| EquipmentType | varchar(50) | 50 |
| ContactName | varchar(50) | 50 |
| ContactPhone | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| CustomerPickupDelivery | varchar(3) | 3 |
| Processed | int | 4 |
| CustomerLoad | varchar(3) | 3 |
| SalesPersonName | varchar(101) | 101 |
| Status | varchar(20) | 20 |
| ExpirationDate | datetime | 8 |
| Destination | nvarchar(100) | 200 |
| DestinationDisplay | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectRequestedLoads]
AS
SELECT        TOP (100) PERCENT dbo.LoadRequest.Id, dbo.LoadRequest.LoadRequestDate, dbo.LoadRequest.LoadRequestTime, dbo.Generator.Name AS [Generator Name], dbo.LoadRequest.ProfileId, 
                         dbo.LoadRequest.NoLoads, dbo.LoadRequest.EquipmentType, dbo.LoadRequest.ContactName, dbo.LoadRequest.ContactPhone, dbo.LoadRequest.VesselTank, dbo.LoadRequest.CustomerPickupDelivery, 
                         dbo.LoadRequest.Processed, dbo.fnLoadRequestForCustomer(dbo.LoadRequest.CustomerPickupDelivery) AS CustomerLoad, dbo.UserMaster.FirstName + ' ' + dbo.UserMaster.LastName AS SalesPersonName, 
                         dbo.Profile.Status, dbo.Profile.EffectiveDate AS ExpirationDate, dbo.Destination.Name AS Destination, dbo.fnGetDestinationDisplay(dbo.Destination.Name, dbo.Destination.Facility) AS DestinationDisplay
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.LoadRequest ON dbo.Destination.Id = dbo.LoadRequest.DestinationId LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.LoadRequest.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                         dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.LoadRequest.ProfileId = dbo.Profile.Id
ORDER BY dbo.LoadRequest.LoadRequestDate, dbo.LoadRequest.LoadRequestTime
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[fnGetDestinationDisplay]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnGetDestinationDisplay.md)
* [[dbo].[fnLoadRequestForCustomer]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnLoadRequestForCustomer.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

