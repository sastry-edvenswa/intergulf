#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadInventoryDetails

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadInventoryDetails]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:50:59 PM Friday, August 24, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| SalesPersonId | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| Generator | varchar(100) | 100 |
| MaterialDescription | varchar(3000) | 3000 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| TransporterName | varchar(50) | 50 |
| BillingTime | decimal(18,2) | 9 |
| BillingDepartment | varchar(50) | 50 |
| GrossWeight | decimal(18,0) | 9 |
| PetroleumAdjAPI | decimal(18,1) | 9 |
| PetroleumFlashPoint | decimal(18,0) | 9 |
| PetroleumPcntWater | decimal(18,1) | 9 |
| PetroleumAsh | decimal(18,4) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadInventoryDetails]
AS
SELECT     dbo.Loads.Id, dbo.Loads.SalesPersonId, dbo.Loads.ScheduledDate, dbo.Generator.Name AS Generator, dbo.Profile.MaterialDescription, 
                      dbo.Loads.TruckId, dbo.Loads.TrailerId, dbo.Transporter.Name AS TransporterName, dbo.Loads.BillingTime, dbo.Loads.BillingDepartment, 
                      dbo.LabTest.GrossWeight, dbo.LabTest.PetroleumAdjAPI, dbo.LabTest.PetroleumFlashPoint, dbo.LabTest.PetroleumPcntWater, 
                      dbo.LabTest.PetroleumAsh
FROM         dbo.LabTest RIGHT OUTER JOIN
                      dbo.Loads INNER JOIN
                      dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id ON dbo.LabTest.Id = dbo.Loads.LabTestId LEFT OUTER JOIN
                      dbo.Generator INNER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

