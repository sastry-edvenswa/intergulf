#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadAccounting

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadAccounting]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:02:18 PM Monday, May 7, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Transporter Name | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| ProfileId | bigint | 8 |
| MaterialCode | nvarchar(50) | 100 |
| PreProperShippingName | nvarchar(100) | 200 |
| ProperShippingName | nvarchar(300) | 600 |
| PostProperShippingName | nvarchar(100) | 200 |
| ProductPlacardNumber | nvarchar(50) | 100 |
| Hazmat | nvarchar(50) | 100 |
| ProductHazardClass | nvarchar(50) | 100 |
| ProductPackingGroup | nvarchar(50) | 100 |
| Number | varchar(50) | 50 |
| Driver FName | varchar(50) | 50 |
| Driver LName | varchar(50) | 50 |
| ContainerType | varchar(50) | 50 |
| ShippingName | varchar(1000) | 1000 |
| IntergulfDescription | nvarchar(50) | 100 |
| ShippingWeight | decimal(18,0) | 9 |
| Name | nvarchar(100) | 200 |
| Address | nvarchar(50) | 100 |
| City | nvarchar(50) | 100 |
| State | nvarchar(50) | 100 |
| Zip | nvarchar(50) | 100 |
| DispatcherFName | varchar(50) | 50 |
| DispatcherLName | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| TestDate | datetime | 8 |
| LabTechId | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadAccounting]
AS
SELECT     dbo.Loads.Id, dbo.Transporter.Name AS [Transporter Name], dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.TrailerId, 
                      dbo.Loads.TankNumber, dbo.Loads.DeliveryReleaseNumber, dbo.Loads.ProfileId, dbo.MaterialCode.MaterialCode, 
                      dbo.MaterialCode.PreProperShippingName, dbo.MaterialCode.ProperShippingName, dbo.MaterialCode.PostProperShippingName, 
                      dbo.MaterialCode.ProductPlacardNumber, dbo.MaterialCode.Hazmat, dbo.MaterialCode.ProductHazardClass, dbo.MaterialCode.ProductPackingGroup, 
                      dbo.Loads.Number, dbo.Driver.FirstName AS [Driver FName], dbo.Driver.LastName AS [Driver LName], dbo.ContainerType.Code AS ContainerType, 
                      dbo.Profile.ShippingName, dbo.MaterialCode.Description AS IntergulfDescription, dbo.Loads.ShippingWeight, dbo.Destination.Name, 
                      dbo.Destination.Address, dbo.Destination.City, dbo.Destination.State, dbo.Destination.Zip, dbo.UserMaster.FirstName AS DispatcherFName, 
                      dbo.UserMaster.LastName AS DispatcherLName, dbo.Profile.ProfileNumber, dbo.LabTest.TestDate, dbo.LabTest.LabTechId
FROM         dbo.Driver RIGHT OUTER JOIN
                      dbo.Destination RIGHT OUTER JOIN
                      dbo.LabTest RIGHT OUTER JOIN
                      dbo.Loads ON dbo.LabTest.LoadId = dbo.Loads.Id LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.Loads.UpdateUser = dbo.UserMaster.UserName ON dbo.Destination.Id = dbo.Loads.DestinationId ON 
                      dbo.Driver.Id = dbo.Loads.DriverId LEFT OUTER JOIN
                      dbo.ContainerType ON dbo.Loads.ContainerTypeId = dbo.ContainerType.Id LEFT OUTER JOIN
                      dbo.MaterialCode RIGHT OUTER JOIN
                      dbo.Profile ON dbo.MaterialCode.ID = dbo.Profile.MaterialCodeId ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ContainerType]](../Tables/dbo_ContainerType.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

