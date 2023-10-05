#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptAirPermitLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwRptAirPermitLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:59:25 PM Tuesday, June 23, 2009 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | decimal(18,0) | 9 |
| ScheduledDate | datetime | 8 |
| GeneratorName | varchar(100) | 100 |
| MaterialDescription | varchar(3000) | 3000 |
| Destination | nvarchar(100) | 200 |
| LabTestId | bigint | 8 |
| PcntWater | decimal(18,0) | 9 |
| PcntOil | decimal(18,0) | 9 |
| ReceivedQuantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |
| Tank | varchar(50) | 50 |
| Phase | varchar(50) | 50 |
| Quantity | bigint | 8 |
| Unit | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptAirPermitLoads]
AS
SELECT     TOP 100 PERCENT fnSelectLabTest.LoadId, fnSelectLoads.ScheduledDate, fnSelectGenerator.Name AS GeneratorName, 
                      fnSelectProfile.MaterialDescription, fnSelectDestination.Name AS Destination, fnSelectLabTestDisbursement.LabTestId, fnSelectLabTest.PcntWater, 
                      fnSelectLabTest.PcntOil, fnSelectLabTest.Quantity AS ReceivedQuantity, fnSelectLabTest.Units, fnSelectLabTestDisbursement.Tank, 
                      fnSelectLabTestDisbursement.Phase, fnSelectLabTestDisbursement.Quantity, fnSelectLabTestDisbursement.Unit
FROM         dbo.fnSelectLabTestDisbursement() fnSelectLabTestDisbursement INNER JOIN
                      dbo.fnSelectLabTest() fnSelectLabTest ON fnSelectLabTestDisbursement.LabTestId = fnSelectLabTest.Id INNER JOIN
                      dbo.fnSelectLoads() fnSelectLoads ON fnSelectLabTest.LoadId = fnSelectLoads.Id INNER JOIN
                      dbo.fnSelectProfile() fnSelectProfile ON fnSelectLoads.ProfileId = fnSelectProfile.Id INNER JOIN
                      dbo.fnSelectGenerator() fnSelectGenerator ON fnSelectProfile.GeneratorId = fnSelectGenerator.Id INNER JOIN
                      dbo.fnSelectDestination() fnSelectDestination ON fnSelectLoads.DestinationId = fnSelectDestination.Id
WHERE     (fnSelectLabTestDisbursement.Tank = 'T3A') OR
                      (fnSelectLabTestDisbursement.Tank = 'T3B')
ORDER BY fnSelectLabTestDisbursement.Tank, fnSelectLabTestDisbursement.LabTestId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTest.md)
* [[dbo].[fnSelectLabTestDisbursement]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTestDisbursement.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

