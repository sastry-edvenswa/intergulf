#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadRequest

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadRequest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:25:12 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Customer Name | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| Profile Number | varchar(50) | 50 |
| GeneratorId | bigint | 8 |
| VesselTank | varchar(100) | 100 |
| LoadRequestDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE  VIEW [dbo].[vwSelectLoadRequest]
AS
SELECT     TOP 100 PERCENT dbo.LoadRequest.Id, dbo.Customer.Name AS [Customer Name], dbo.Generator.Name AS [Generator Name], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.GeneratorId, dbo.LoadRequest.VesselTank, dbo.LoadRequest.LoadRequestDate
FROM         dbo.Generator RIGHT OUTER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id RIGHT OUTER JOIN
                      dbo.LoadRequest ON dbo.Profile.Id = dbo.LoadRequest.ProfileId
ORDER BY dbo.Generator.Name

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

