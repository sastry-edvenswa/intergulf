#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadMaterialGeneratorKStarks

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadMaterialGeneratorKStarks]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:31:47 PM Thursday, April 12, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| Generator Name | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| ProfileNumber | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| TruckId | varchar(50) | 50 |
| Profile Billing Department | varchar(100) | 100 |
| Load Billing Department | varchar(50) | 50 |
| ProductCategory | varchar(50) | 50 |
| Load Vessel Tank | varchar(100) | 100 |
| Load Tank Number | varchar(50) | 50 |
| LabTestId | bigint | 8 |
| Tanks | varchar(30) | 30 |
| PcntWater | decimal(18,0) | 9 |
| PcntOil | decimal(18,0) | 9 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |
| PrePetroleumFlashPoint | varchar(5) | 5 |
| PetroleumFlashPoint | decimal(18,0) | 9 |
| PreAqueousFlashPoint | varchar(5) | 5 |
| AqueousFlashPoint | decimal(18,0) | 9 |
| DispatchStatus | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadMaterialGeneratorKStarks]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Generator.Name AS [Generator Name], dbo.Destination.Name AS Destination, 
                      dbo.Profile.ProfileNumber, dbo.Profile.MaterialDescription, dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Loads.TruckId, 
                      dbo.Profile.BillingDepartment AS [Profile Billing Department], dbo.Loads.BillingDepartment AS [Load Billing Department], dbo.Profile.ProductCategory, 
                      dbo.Loads.VesselTank AS [Load Vessel Tank], dbo.Loads.TankNumber AS [Load Tank Number], dbo.Loads.LabTestId, 
                      dbo.fnSelectLoadTanks(dbo.Loads.LabTestId) AS Tanks, dbo.LabTest.PcntWater, dbo.LabTest.PcntOil, dbo.LabTest.Quantity, dbo.LabTest.Units, 
                      dbo.LabTest.PrePetroleumFlashPoint, dbo.LabTest.PetroleumFlashPoint, dbo.LabTest.PreAqueousFlashPoint, dbo.LabTest.AqueousFlashPoint, 
                      dbo.Loads.DispatchStatus, dbo.Loads.SalesPersonId
FROM         dbo.LabTest RIGHT OUTER JOIN
                      dbo.Loads ON dbo.LabTest.Id = dbo.Loads.LabTestId LEFT OUTER JOIN
                      dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                      dbo.Generator INNER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE     (dbo.Generator.Name LIKE '%Intergulf KStarks%')
ORDER BY dbo.Generator.Name, dbo.Destination.Name, dbo.Profile.ProfileNumber, dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[fnSelectLoadTanks]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSelectLoadTanks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

