#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSaturnTestLabTextDisbursement

# ![Views](../../../../Images/View32.png) [dbo].[vwSaturnTestLabTextDisbursement]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:17:52 PM Thursday, February 16, 2023 |
| Last Modified | 3:17:52 PM Thursday, February 16, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| LabTestId | bigint | 8 |  |
| Tank | varchar(50) | 50 |  |
| Phase | varchar(50) | 50 |  |
| Quantity | decimal(18,2) | 9 |  |
| Unit | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSaturnTestLabTextDisbursement]
AS
SELECT        Id, LabTestId, Tank, Phase, Quantity, Unit
FROM            dbo.LabTestDisbursement
WHERE        (LabTestId = 378320)
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTestDisbursement]](../Tables/dbo_LabTestDisbursement.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

