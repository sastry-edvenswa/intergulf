#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSaturnTestTank

# ![Views](../../../../Images/View32.png) [dbo].[vwSaturnTestTank]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:15:47 PM Thursday, February 16, 2023 |
| Last Modified | 3:17:08 PM Thursday, February 16, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Description | varchar(50) | 50 |
| Location | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSaturnTestTank]
AS
SELECT        Description, Location
FROM            dbo.Tanks
WHERE        (Description = 'T1B')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Tanks]](../Tables/dbo_Tanks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

