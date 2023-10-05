#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectGeneratorForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectGeneratorForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:17:00 PM Thursday, December 15, 2022 |
| Last Modified | 4:22:16 PM Thursday, December 15, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| Name | varchar(100) | 100 |  |
| Address | varchar(3000) | 3000 |  |
| City | varchar(50) | 50 |  |
| State | varchar(50) | 50 |  |
| Zip | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectGeneratorForSaturn]
AS
SELECT        TOP (100) PERCENT Id, Name, Address, City, State, Zip
FROM            dbo.Generator
ORDER BY Name
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

