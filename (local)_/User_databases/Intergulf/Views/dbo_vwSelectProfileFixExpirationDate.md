#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileFixExpirationDate

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileFixExpirationDate]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:02:48 PM Monday, January 27, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Name | varchar(100) | 100 |
| CreateDate | datetime | 8 |
| EffectiveDate | datetime | 8 |
| ProfileType | varchar(50) | 50 |
| Status | varchar(20) | 20 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfileFixExpirationDate]
AS
SELECT     dbo.Profile.Id, dbo.Generator.Name, dbo.Profile.CreateDate, dbo.Profile.EffectiveDate, dbo.Profile.ProfileType, dbo.Profile.Status
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE     (dbo.Profile.Status = 'Active') AND (dbo.Profile.ProfileType = 'Product' OR
                      dbo.Profile.ProfileType = 'Recycled')

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

