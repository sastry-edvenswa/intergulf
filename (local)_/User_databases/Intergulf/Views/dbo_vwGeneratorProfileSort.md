#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwGeneratorProfileSort

# ![Views](../../../../Images/View32.png) [dbo].[vwGeneratorProfileSort]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:23:14 PM Monday, April 18, 2016 |
| Last Modified | 10:23:14 PM Monday, April 18, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Generator Id | numeric(18,0) | 9 |
| Generator Name | varchar(100) | 100 |
| ProfileId | bigint | 8 |
| Profile Number | varchar(50) | 50 |
| Profile Waste Code | varchar(50) | 50 |
| Profile Material Description | varchar(3000) | 3000 |
| Status | varchar(20) | 20 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwGeneratorProfileSort]
AS
SELECT     TOP (100) PERCENT dbo.Generator.Id AS [Generator Id], dbo.Generator.Name AS [Generator Name], dbo.Profile.Id AS ProfileId, 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.Profile.WasteCode AS [Profile Waste Code], dbo.Profile.MaterialDescription AS [Profile Material Description], 
                      dbo.Profile.Status
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
ORDER BY [Generator Name]

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

