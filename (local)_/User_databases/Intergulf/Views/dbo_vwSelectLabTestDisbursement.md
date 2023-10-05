#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLabTestDisbursement

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLabTestDisbursement]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:37:58 PM Monday, April 9, 2018 |
| Last Modified | 8:37:58 PM Monday, April 9, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Tank | varchar(50) | 50 |
| Phase | varchar(50) | 50 |
| Quantity | decimal(18,2) | 9 |
| Unit | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLabTestDisbursement]
AS
SELECT        dbo.LabTest.Id, dbo.LabTestDisbursement.Tank, dbo.LabTestDisbursement.Phase, dbo.LabTestDisbursement.Quantity, dbo.LabTestDisbursement.Unit
FROM            dbo.LabTest RIGHT OUTER JOIN
                         dbo.LabTestDisbursement ON dbo.LabTest.Id = dbo.LabTestDisbursement.LabTestId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[LabTestDisbursement]](../Tables/dbo_LabTestDisbursement.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

