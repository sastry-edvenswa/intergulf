#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwDriver

# ![Views](../../../../Images/View32.png) [dbo].[vwDriver]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:36:33 PM Sunday, February 11, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | numeric(18,0) | 9 |
| DriverId | bigint | 8 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| SsNo | varchar(50) | 50 |
| BirthDate | datetime | 8 |
| LicenseExpirationDate | datetime | 8 |
| Status | varchar(50) | 50 |
| Phone | varchar(50) | 50 |
| Cell | varchar(50) | 50 |
| ShipQualified | int | 4 |
| InTraining | int | 4 |
| NonHazOnly | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwDriver]
AS
SELECT     fnSelectDriver.*
FROM         dbo.fnSelectDriver() fnSelectDriver
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectDriver]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDriver.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

