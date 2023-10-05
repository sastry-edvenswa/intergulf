#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectEquipmentLastLoadDescription

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectEquipmentLastLoadDescription]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:38:31 PM Monday, February 4, 2019 |
| Last Modified | 3:59:29 PM Monday, February 4, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| TrailerId | varchar(50) | 50 |
| LastLocationStatus | varchar(50) | 50 |
| TrailerCustomerDescription | varchar(100) | 100 |
| Location | varchar(50) | 50 |
| LocationStatus | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| TrailerLastLoadDescription | varchar(1000) | 1000 |
| DispatchStatus | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectEquipmentLastLoadDescription]
AS
SELECT        TOP (1) dbo.Loads.Id, dbo.Loads.TrailerId, dbo.Equipment.LastLocationStatus, dbo.Equipment.TrailerCustomerDescription, dbo.Equipment.Location, dbo.Equipment.LocationStatus, dbo.Loads.ScheduledDate, 
                         dbo.Loads.ScheduledTime, dbo.Profile.TrailerLastLoadDescription, dbo.Loads.DispatchStatus
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.Equipment ON dbo.Loads.TrailerId = dbo.Equipment.Id LEFT OUTER JOIN
                         dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE        (dbo.Loads.DispatchStatus = 'Scheduled' OR
                         dbo.Loads.DispatchStatus = 'Complete' OR
                         dbo.Loads.DispatchStatus = 'Loaded') AND (LEN(dbo.Loads.TrailerId) > 0)
ORDER BY dbo.Loads.ScheduledDate DESC, dbo.Loads.ScheduledTime DESC
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

