#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsCount

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsCount]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:25:32 AM Wednesday, October 12, 2011 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Name | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| MaterialCode | nvarchar(50) | 100 |
| Description | nvarchar(50) | 100 |
| ScheduledDate | datetime | 8 |
| LoadCount | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsCount]
AS
SELECT     TOP 100 PERCENT dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, dbo.MaterialCode.MaterialCode, 
                      dbo.MaterialCode.Description, dbo.Loads.ScheduledDate, COUNT(dbo.Loads.ScheduledDate) AS LoadCount
FROM         dbo.Loads INNER JOIN
                      dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id INNER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id INNER JOIN
                      dbo.MaterialCode ON dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID
GROUP BY dbo.Loads.ScheduledDate, dbo.Loads.ProfileId, dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.Profile.WasteCode, 
                      dbo.MaterialCode.MaterialCode, dbo.MaterialCode.Description
ORDER BY dbo.Generator.Name, dbo.Loads.ProfileId, dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

