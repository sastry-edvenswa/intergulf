#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadDriver

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadDriver]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:46:35 PM Thursday, March 22, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadDriver]
AS
SELECT     dbo.Loads.Id, dbo.Driver.FirstName, dbo.Driver.LastName
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

