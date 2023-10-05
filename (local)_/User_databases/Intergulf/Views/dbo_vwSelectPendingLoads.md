#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectPendingLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectPendingLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:26:16 PM Monday, January 29, 2007 |
| Last Modified | 5:19:56 PM Wednesday, June 23, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileId | bigint | 8 |
| Profile Number | varchar(50) | 50 |
| LoadType | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ActualDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| ActualTime | datetime | 8 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| VendorId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(100) | 100 |
| DispatchStatus | varchar(50) | 50 |
| ContactName | varchar(100) | 100 |
| ContactPhone | varchar(50) | 50 |
| PickupLocation | varchar(200) | 200 |
| EquipmentType | varchar(50) | 50 |
| VesselTank | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| DestinationDisplay | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectPendingLoads]
AS
SELECT        dbo.Loads.Id, dbo.Loads.ProfileId, dbo.Profile.ProfileNumber AS [Profile Number], dbo.Loads.LoadType, dbo.Loads.ScheduledDate, dbo.Loads.ActualDate, dbo.Loads.ScheduledTime, dbo.Loads.ActualTime, 
                         dbo.Driver.FirstName AS [Driver First Name], dbo.Driver.LastName AS [Driver Last Name], dbo.Profile.ProfileType, dbo.Loads.VendorId, dbo.Generator.Name AS [Generator Name], 
                         dbo.Customer.Name AS [Customer Name], dbo.Loads.DispatchStatus, dbo.Loads.ContactName, dbo.Loads.ContactPhone, dbo.Loads.PickupLocation, dbo.Loads.EquipmentType, dbo.Loads.VesselTank, 
                         dbo.Destination.Name AS Destination, dbo.fnGetDestinationDisplay(dbo.Destination.Name, dbo.Destination.Facility) AS DestinationDisplay
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                         dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Profile INNER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                         dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id
WHERE        (dbo.Loads.DispatchStatus = 'Pending')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[fnGetDestinationDisplay]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnGetDestinationDisplay.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

