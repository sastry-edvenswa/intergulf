#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectDriverForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectDriverForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:31:37 PM Thursday, December 15, 2022 |
| Last Modified | 4:31:37 PM Thursday, December 15, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| DriverId | bigint | 8 |  |
| FirstName | varchar(50) | 50 |  |
| LastName | varchar(50) | 50 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectDriverForSaturn]
AS
SELECT        TOP (100) PERCENT Id, DriverId, FirstName, LastName
FROM            dbo.Driver
ORDER BY LastName, FirstName
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Driver]](../Tables/dbo_Driver.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

