#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwCustomerGeneratorSort

# ![Views](../../../../Images/View32.png) [dbo].[vwCustomerGeneratorSort]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:09:55 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| GeneratorId | bigint | 8 |
| CustomerId | bigint | 8 |
| Customer Name | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwCustomerGeneratorSort]
AS
SELECT DISTINCT 
                      TOP 100 PERCENT dbo.Profile.GeneratorId, dbo.Profile.CustomerId, dbo.Customer.Name AS [Customer Name], 
                      dbo.Generator.Name AS [Generator Name], dbo.Generator.Address AS [Generator Address]
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id
ORDER BY dbo.Profile.CustomerId, dbo.Profile.GeneratorId
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

