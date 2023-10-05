#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectActiveTrucksNew

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectActiveTrucksNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:40:55 PM Friday, February 8, 2019 |
| Last Modified | 2:40:55 PM Friday, February 8, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | varchar(50) | 50 |
| Description | varchar(50) | 50 |
| Type | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Status | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectActiveTrucksNew]
AS
SELECT        TOP (100) PERCENT dbo.Equipment.Id, dbo.Equipment.Description, dbo.Equipment.Type, dbo.Equipment.TrailerId, dbo.Equipment.Status, dbo.Driver.FirstName, dbo.Driver.LastName
FROM            dbo.Equipment LEFT OUTER JOIN
                         dbo.Driver ON dbo.Equipment.DriverId = dbo.Driver.Id
WHERE        (dbo.Equipment.Type = 'Truck' OR
                         dbo.Equipment.Type = 'Outside') AND (dbo.Equipment.Status = 'Active' OR
                         dbo.Equipment.Status = 'In Repair')
ORDER BY dbo.Equipment.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Equipment]](../Tables/dbo_Equipment.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

