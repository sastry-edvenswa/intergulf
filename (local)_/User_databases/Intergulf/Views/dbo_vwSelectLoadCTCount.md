#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadCTCount

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadCTCount]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:56:18 PM Wednesday, October 27, 2010 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| GeneratorId | bigint | 8 |
| CustomerId | bigint | 8 |
| ScheduledDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadCTCount]
AS
SELECT     dbo.Loads.Id, dbo.Profile.GeneratorId, dbo.Loads.CustomerId, dbo.Loads.ScheduledDate
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

