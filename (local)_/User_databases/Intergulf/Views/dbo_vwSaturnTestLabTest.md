#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSaturnTestLabTest

# ![Views](../../../../Images/View32.png) [dbo].[vwSaturnTestLabTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:22:56 PM Thursday, February 16, 2023 |
| Last Modified | 3:22:56 PM Thursday, February 16, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| LoadId | decimal(18,0) | 9 |  |
| PetroleumAdjAPI | decimal(18,1) | 9 |  |
| ActualQuantity | decimal(18,0) | 9 |  |
| ActualUnits | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSaturnTestLabTest]
AS
SELECT        Id, LoadId, PetroleumAdjAPI, ActualQuantity, ActualUnits
FROM            dbo.LabTest
WHERE        (Id = 378320)
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

