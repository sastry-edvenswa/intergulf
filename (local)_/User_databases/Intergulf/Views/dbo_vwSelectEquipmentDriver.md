#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectEquipmentDriver

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectEquipmentDriver]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:57:54 PM Thursday, March 22, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | varchar(50) | 50 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| Type | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectEquipmentDriver]
AS
SELECT     dbo.Equipment.Id, dbo.Driver.FirstName, dbo.Driver.LastName, dbo.Equipment.Type
FROM         dbo.Equipment LEFT OUTER JOIN
                      dbo.Driver ON dbo.Equipment.DriverId = dbo.Driver.Id
WHERE     (dbo.Equipment.Type = 'Truck') OR
                      (dbo.Equipment.Type = 'Outside')
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

