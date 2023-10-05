#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadDriverTimeLog

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadDriverTimeLog]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:40:56 PM Saturday, June 6, 2015 |
| Last Modified | 2:33:40 PM Wednesday, February 26, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| PickupLocation | varchar(200) | 200 |
| ContactName | varchar(100) | 100 |
| ContactPhone | varchar(50) | 50 |
| EquipmentType | varchar(50) | 50 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| EstQuantity | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| SpecialRequirements | varchar(3000) | 3000 |
| GeneratorId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| MaterialCode | nvarchar(50) | 100 |
| Transporter Name | varchar(100) | 100 |
| DocumentType | varchar(50) | 50 |
| Destination Name | nvarchar(100) | 200 |
| Destination Address | nvarchar(50) | 100 |
| Destination City | nvarchar(50) | 100 |
| Destination State | nvarchar(50) | 100 |
| Destination Zip | nvarchar(50) | 100 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| VesselTank | varchar(100) | 100 |
| WashOutRequired | varchar(50) | 50 |
| WeightTicket | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| Name | varchar(100) | 100 |
| Phone | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadDriverTimeLog]
AS
SELECT        dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, dbo.Loads.PickupLocation, dbo.Loads.ContactName, dbo.Loads.ContactPhone, dbo.Loads.EquipmentType, dbo.Loads.TruckId, 
                         dbo.Loads.TrailerId, dbo.Loads.EstQuantity, dbo.Loads.TankNumber, dbo.Loads.DeliveryReleaseNumber, dbo.Loads.SpecialRequirements, dbo.Profile.GeneratorId, dbo.Generator.Name AS [Generator Name], 
                         dbo.MaterialCode.MaterialCode, dbo.Transporter.Name AS [Transporter Name], dbo.Profile.DocumentType, dbo.Destination.Name AS [Destination Name], dbo.Destination.Address AS [Destination Address], 
                         dbo.Destination.City AS [Destination City], dbo.Destination.State AS [Destination State], dbo.Destination.Zip AS [Destination Zip], dbo.Driver.FirstName, dbo.Driver.LastName, dbo.Profile.MaterialDescription, 
                         dbo.Loads.VesselTank, dbo.Loads.WashOutRequired, dbo.Loads.WeightTicket, dbo.Profile.ProfileNumber, dbo.Customer.Name, dbo.Customer.Phone
FROM            dbo.Customer RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Customer.Id = dbo.Loads.CustomerId LEFT OUTER JOIN
                         dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                         dbo.MaterialCode INNER JOIN
                         dbo.Profile ON dbo.MaterialCode.ID = dbo.Profile.MaterialCodeId RIGHT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

