#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLabTestAirPermitLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLabTestAirPermitLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:08:01 PM Tuesday, June 23, 2009 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | decimal(18,0) | 9 |
| Id | bigint | 8 |
| TestDate | datetime | 8 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |
| PetroleumAdjAPI | decimal(18,1) | 9 |
| DisbursementTank | varchar(50) | 50 |
| DisbursementPhase | varchar(50) | 50 |
| DisbursementQuantity | bigint | 8 |
| DisbursementUnit | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLabTestAirPermitLoads]
AS
SELECT     TOP 100 PERCENT fnSelectLabTest.LoadId, fnSelectLabTest.Id, fnSelectLabTest.TestDate, fnSelectLabTest.Quantity, fnSelectLabTest.Units, 
                      fnSelectLabTest.PetroleumAdjAPI, fnSelectLabTestDisbursement.Tank AS DisbursementTank, 
                      fnSelectLabTestDisbursement.Phase AS DisbursementPhase, fnSelectLabTestDisbursement.Quantity AS DisbursementQuantity, 
                      fnSelectLabTestDisbursement.Unit AS DisbursementUnit
FROM         dbo.fnSelectLabTest() fnSelectLabTest INNER JOIN
                      dbo.fnSelectLabTestDisbursement() fnSelectLabTestDisbursement ON fnSelectLabTest.Id = fnSelectLabTestDisbursement.LabTestId
WHERE     (fnSelectLabTestDisbursement.Tank = 'T3A') OR
                      (fnSelectLabTestDisbursement.Tank = 'T3B')
ORDER BY fnSelectLabTest.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTest.md)
* [[dbo].[fnSelectLabTestDisbursement]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTestDisbursement.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

