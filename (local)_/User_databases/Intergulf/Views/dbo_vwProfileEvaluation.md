#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwProfileEvaluation

# ![Views](../../../../Images/View32.png) [dbo].[vwProfileEvaluation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:17:52 AM Saturday, February 10, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | numeric(18,0) | 9 |
| CustomerId | varchar(50) | 50 |
| GeneratorId | varchar(50) | 50 |
| ProfileId | varchar(50) | 50 |
| YesNo | int | 4 |
| PK | int | 4 |
| AD | int | 4 |
| DescriptionId | numeric(18,0) | 9 |
| SortOrder | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwProfileEvaluation]
AS
SELECT     fnSelectProfileEvaluation.*
FROM         dbo.fnSelectProfileEvaluation() fnSelectProfileEvaluation
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectProfileEvaluation]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfileEvaluation.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

