#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsByProfileCreateDate

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsByProfileCreateDate]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:18:28 PM Tuesday, June 19, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Customer Name | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| Profile Number | varchar(50) | 50 |
| CreateDate | datetime | 8 |
| ExpirationDate | datetime | 8 |
| ProfileType | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| MaterialClassification | varchar(200) | 200 |
| LoadFrequency | varchar(50) | 50 |
| Status | varchar(20) | 20 |
| LastName | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| PickupLocation | varchar(200) | 200 |
| VesselTank | varchar(100) | 100 |
| Name | nvarchar(100) | 200 |
| EstQuantity | varchar(50) | 50 |
| EquipmentType | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsByProfileCreateDate]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Generator.Name AS [Generator Name], dbo.Customer.Name AS [Customer Name], dbo.Loads.ScheduledDate, 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.CreateDate, dbo.Profile.EffectiveDate AS ExpirationDate, dbo.Profile.ProfileType, 
                      dbo.Profile.WasteCode, dbo.Profile.MaterialDescription, dbo.Profile.MaterialClassification, dbo.Profile.LoadFrequency, dbo.Profile.Status, 
                      dbo.UserMaster.LastName, dbo.UserMaster.FirstName, dbo.Loads.SalesPersonId, dbo.Loads.PickupLocation, dbo.Loads.VesselTank, 
                      dbo.Destination.Name, dbo.Loads.EstQuantity, dbo.Loads.EquipmentType, dbo.Loads.DispatchStatus, dbo.Loads.BillingDepartment
FROM         dbo.Destination INNER JOIN
                      dbo.Profile INNER JOIN
                      dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId INNER JOIN
                      dbo.UserMaster ON dbo.Loads.SalesPersonId = dbo.UserMaster.UserName ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id
WHERE     (dbo.Profile.Status = 'Active')
ORDER BY dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.Profile.CreateDate, dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

