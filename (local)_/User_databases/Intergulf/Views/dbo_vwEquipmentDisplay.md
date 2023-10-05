#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwEquipmentDisplay

# ![Views](../../../../Images/View32.png) [dbo].[vwEquipmentDisplay]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:35:13 PM Thursday, August 10, 2017 |
| Last Modified | 3:14:38 PM Tuesday, June 4, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| Status | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| DriverId | bigint | 8 |
| TransporterId | bigint | 8 |
| VinNo | varchar(50) | 50 |
| MakeYear | varchar(50) | 50 |
| Make | varchar(50) | 50 |
| LicensePlate | varchar(50) | 50 |
| Transporter Name | varchar(100) | 100 |
| Driver First Name | varchar(50) | 50 |
| Driver Last Name | varchar(50) | 50 |
| Trailer Description | varchar(50) | 50 |
| Location | varchar(50) | 50 |
| LocationStatus | varchar(50) | 50 |
| TrailerCustomerDescription | varchar(100) | 100 |
| Insulated | varchar(25) | 25 |
| VaporRecovery | varchar(3) | 3 |
| DryBreak | varchar(3) | 3 |
| BellyRear | varchar(25) | 25 |
| MaxTemp | varchar(10) | 10 |
| ThirdPartyTransporter | int | 4 |
| PTLoad | numeric(18,2) | 9 |
| PTHour | numeric(18,2) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwEquipmentDisplay]
AS
SELECT        TOP (100) PERCENT dbo.Equipment.Id, dbo.Equipment.Description, dbo.Equipment.Type, dbo.Equipment.Status, dbo.Equipment.TrailerId, dbo.Equipment.DriverId, dbo.Equipment.TransporterId, 
                         dbo.Equipment.VinNo, dbo.Equipment.MakeYear, dbo.Equipment.Make, dbo.Equipment.LicensePlate, dbo.Transporter.Name AS [Transporter Name], dbo.Driver.FirstName AS [Driver First Name], 
                         dbo.Driver.LastName AS [Driver Last Name], Equipment_1.Description AS [Trailer Description], dbo.Equipment.Location, dbo.Equipment.LocationStatus, dbo.Equipment.TrailerCustomerDescription, 
                         dbo.Equipment.Insulated, dbo.Equipment.VaporRecovery, dbo.Equipment.DryBreak, dbo.Equipment.BellyRear, dbo.Equipment.MaxTemp, dbo.Equipment.ThirdPartyTransporter, dbo.Equipment.PTLoad, 
                         dbo.Equipment.PTHour
FROM            dbo.Equipment LEFT OUTER JOIN
                         dbo.Equipment AS Equipment_1 ON dbo.Equipment.TrailerId = Equipment_1.Id LEFT OUTER JOIN
                         dbo.Driver ON dbo.Equipment.DriverId = dbo.Driver.Id LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Equipment.TransporterId = dbo.Transporter.Id
ORDER BY dbo.Equipment.Type DESC, dbo.Equipment.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

