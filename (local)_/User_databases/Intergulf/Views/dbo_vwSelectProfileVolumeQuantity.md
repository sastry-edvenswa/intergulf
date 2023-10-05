#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileVolumeQuantity

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileVolumeQuantity]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:52:50 AM Thursday, February 25, 2021 |
| Last Modified | 1:34:56 PM Wednesday, November 3, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileNumber | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |
| TotalQty | decimal(15,0) | 9 |
| ActualUnits | varchar(50) | 50 |
| ActTotalQty | decimal(15,0) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileVolumeQuantity]
AS
SELECT        dbo.Loads.Id, dbo.Profile.ProfileNumber, dbo.Loads.ScheduledDate, dbo.LabTest.Quantity, dbo.LabTest.Units, dbo.fnLoadQuantityToGallons(dbo.LabTest.Quantity, dbo.LabTest.Units) AS TotalQty, 
                         dbo.LabTest.ActualUnits, dbo.fnLoadQuantityToGallons(dbo.LabTest.ActualQuantity, dbo.LabTest.ActualUnits) AS ActTotalQty
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                         dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[fnLoadQuantityToGallons]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnLoadQuantityToGallons.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

