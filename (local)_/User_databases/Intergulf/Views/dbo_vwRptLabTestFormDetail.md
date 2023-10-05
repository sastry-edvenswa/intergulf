#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLabTestFormDetail

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLabTestFormDetail]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:12:10 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| LabTestId | bigint | 8 |  |
| Phase | varchar(50) | 50 |  |
| Metal | varchar(50) | 50 |  |
| Quantity | numeric(18,2) | 9 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLabTestFormDetail]
AS
SELECT     TOP 100 PERCENT Id, LabTestId, Phase, Metal, Quantity
FROM         dbo.LabTestDetail
WHERE     (Phase = 'Aqueous')
ORDER BY LabTestId, Id, Metal
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTestDetail]](../Tables/dbo_LabTestDetail.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

